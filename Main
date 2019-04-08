package benchmark;

import java.util.*;

public class Benchmark {

    public static void main(String[] args) {

        final int size = 1000000;

        ArrayList<Person> arrayList = new ArrayList<>();
        for (int i = 0; i < size; i++) {
            arrayList.add(new Person("Jimmy", i));
        }
        LinkedList<Person> linkedList = new LinkedList<>();
        for (int i = 0; i < size; i++) {
            linkedList.add(new Person("John", i));
        }

        HashMap<Integer, Person> hashMap = new HashMap<>();
        for (int i = 0; i < size; i++) {
            hashMap.put(i, new Person("Valentin", i));
        }

        TreeMap<Integer, Person> treeMap = new TreeMap<>();
        for (int i = 0; i < size; i++) {
            treeMap.put(i, new Person("Vladimir Putin", i));
        }

        LinkedHashMap<Integer, Person> linkedHashMap = new LinkedHashMap<>();
        for (int i = 0; i < size; i++) {
            linkedHashMap.put(i, new Person("Vladimir Putin", i));
        }

        HashSet<Person> hashSet = new HashSet<>();
        for (int i = 0; i < size; i++) {
            hashSet.add(new Person("jim", i));
        }

        LinkedHashSet<Person> linkedHashSet = new LinkedHashSet<>();
        for (int i = 0; i < size; i++) {
            linkedHashSet.add(new Person("jim", i));
        }

        TreeSet<Person> treeSet = new TreeSet<>((o1, o2) -> Integer.compare(o2.getAge(), o1.getAge()));
        for (int i = 0; i < size; i++) {
            treeSet.add(new Person("jim", i));
        }

        testList(arrayList, linkedList);
        testMap(hashMap, treeMap, linkedHashMap);
        testSet(hashSet, linkedHashSet, treeSet);
    }

    private static void testList(ArrayList<Person> arrayList, LinkedList<Person> linkedList) {
        //add
        System.out.println("Вставка 5000 элементов в ArrayList: " + add(arrayList) + " ms");
        System.out.println("Вставка 5000 элементов в LinkedList: " + add(linkedList) + " ms\n");

        //remove
        System.out.println("Удаление 5000 элементов в ArrayList: " + remove(arrayList) + " ms");
        System.out.println("Удаление 5000 элементов в LinkedList: " + remove(linkedList) + " ms\n");
    }

    private static long add(List<Person> list) {
        long start = System.currentTimeMillis();
        for (int i = 395000; i < 400000; i++) {
            list.add(i, new Person("jim", i));
        }
        long end = System.currentTimeMillis();
        return end - start;
    }

    private static long remove(List<Person> list) {
        long start = System.currentTimeMillis();
        for (int i = 295000; i < 300000; i++) {
            list.remove(i);
        }
        long end = System.currentTimeMillis();
        return end - start;
    }

    private static void testMap(HashMap<Integer, Person> hashMap, TreeMap<Integer, Person> treeMap, LinkedHashMap<Integer, Person> linkedHashMap) {
        //add
        System.out.println("Вставка 300k элементов в HashMap: " + add(hashMap) + "ms");
        System.out.println("Вставка 300k элементов в TreeMap: " + add(treeMap) + "ms");
        System.out.println("Вставка 300k элементов в LinkedHashMap: " + add(linkedHashMap) + "ms\n");

        //remove
        System.out.println("Удаление 300k элементов в HashMap: " + remove(hashMap) + "ms");
        System.out.println("Удаление 300k элементов в TreeMap: " + remove(treeMap) + "ms");
        System.out.println("Удаление 300k элементов в LinkedHashMap: " + remove(linkedHashMap) + "ms\n");
    }

    private static long add(Map<Integer, Person> map) {
        long start = System.currentTimeMillis();
        for (int i = 200000; i < 600000; i++) {
            map.put(i, new Person("jim", i));
        }
        long end = System.currentTimeMillis();
        return end - start;
    }

    private static long remove(Map<Integer, Person> map) {
        long start = System.currentTimeMillis();
        for (int i = 350000; i < 650000; i++) {
            map.remove(i);
        }
        long end = System.currentTimeMillis();
        return end - start;
    }

    private static long add(Set<Person> set) {
        long start = System.currentTimeMillis();
        for (int i = 1000001; i < 1300000; i++) {
            set.add(new Person("jim", i));
        }
        long end = System.currentTimeMillis();
        return end - start;
    }

    private static long remove(Set<Person> set) {
        long start = System.currentTimeMillis();
        for (int i = 350000; i < 650000; i++) {
            set.remove(new Person("jim", i));
        }
        long end = System.currentTimeMillis();
        return end - start;
    }

    private static void testSet(HashSet<Person> hashSet, LinkedHashSet<Person> linkedHashSet, TreeSet<Person> treeSet) {
        //add
        System.out.println("Вставка 300k элементов в HashSet: " + add(hashSet) + "ms");
        System.out.println("Вставка 300k элементов в TreeSet: " + add(treeSet) + "ms");
        System.out.println("Вставка 300k элементов в LinkedHashSet: " + add(linkedHashSet) + "ms\n");

        //remove
        System.out.println("Удаление 300k элементов в HashSet: " + remove(hashSet) + "ms");
        System.out.println("Удаление 300k элементов в TreeSet: " + remove(treeSet) + "ms");
        System.out.println("Удаление 300k элементов в LinkedHashSet: " + remove(linkedHashSet) + "ms\n");
    }
}
