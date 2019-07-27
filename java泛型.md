- 泛型作用
 
	参数化类型
  
----------

1. 使用泛型写出更加灵活通用的代码
1. 泛型将代码安全性检查(保证类型安全问题)提前到编译期
1. 泛型能省去类型强制转换

----------
泛型是语法糖
泛型擦除

类型边界


协变 向上转型
逆变 强制类型转换

PECS原则，Producer-Extend,Customer-Super，也就是泛型代码是生产者，使用Extend，泛型代码作为消费者Super

泛型擦除地点---边界

    static <T> T[] toArray(T... args) {
    	return args;
    }
    
    static <T> T[] pickTwo(T a, T b, T c) {

   		switch(ThreadLocalRandom.current().nextInt(3)) {
	    case 0: return toArray(a, b);
    	case 1: return toArray(a, c);
    	case 2: return toArray(b, c);
    	}
    	throw new AssertionError(); // Can't get here
    }
    
    public static void main(String[] args) {
    
    	String[] attributes = pickTwo("Good", "Fast", "Cheap");
    }

基类劫持:

    public interface Playable<T>  {
		T play();
    }
    
    public class Base implements  Playable<Integer> {
	    @Override
	    public Integer play() {
	   	 return 4;
	    }
    }
    
    public class Derived extend Base implements Playable<String>{
   		 ...
    }

自限定类型:
   将泛型的类型限制为自己以及自己的子类。最常见的在于实现Compareable接口的时候
