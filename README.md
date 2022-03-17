# HashMap2
Complete view on HashMap
import java.util.*;
public class Main
{
    public static void main(String args[])
    {
        Scanner g=new Scanner(System.in);
        HashMap<Integer,Integer> q=new HashMap<Integer,Integer>();
        q.put(1,9);
        q.put(2,12);
        q.put(3,44);
        for(Map.Entry m:q.entrySet())
        {
            System.out.println(m.getKey()+ " "+ m.getValue());
        }
        q.putIfAbsent(4,23);
        q.putIfAbsent(2,33);
        System.out.println("after invoking putIfAbsent method in java");
        //second statement is not added to map because already that key is present in thath
         for(Map.Entry m:q.entrySet())
        {
            System.out.println(m.getKey()+ " "+ m.getValue());
        }
        //create another HashMap and add it to the old HashMap
        HashMap<Integer,Integer> ne=new HashMap<Integer,Integer>();
        ne.put(20,200);
        ne.put(21,210);
        q.putAll(ne);
        System.out.println("\nafter using putAll method ");
         for(Map.Entry m:q.entrySet())
        {
            System.out.println(m.getKey()+ " "+ m.getValue());
        }
        //different wayes to remove elements in HashMap 
        q.remove(1);//reomoving based on key
        q.remove(4,23);//removing both value and keybased
        System.out.println("\nafter using remove methods ");
        for(Map.Entry m:q.entrySet())
        {
            System.out.println(m.getKey()+ " "+ m.getValue());
        }
        q.replace(2,34);
        q.replace(3,44,88);
        System.out.println("\nafter invoking different replace mthodss");
        for(Map.Entry m:q.entrySet())
        {
            System.out.println(m.getKey()+ " "+ m.getValue());
        }
        System.out.println("\n after invoking replace  All method with 40");
        
        q.replaceAll((k,v)->40);
        for(Map.Entry m:q.entrySet())
        {
            System.out.println(m.getKey()+ " "+ m.getValue());
        }
    }
}
