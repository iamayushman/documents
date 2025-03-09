# OOPC
- Objects - Entity with state & Behavior
- Class - Bluepring of object
- Inheritance - inherits properties from parents
- Polymorphism - method overloading / overriding
- Abstraction - Abstract/interface to hide details
- Encapsulation - wrapping data into single unit
## OOPs Terms
- Coupling - Knowledge of another class or dependency
- Cohesion - single well defined task
- Association - One to One, One to Many, Many to One and Many to Many
- Aggregation - has-a or is part of relation between classes
- Composition - class contains another class as its state

# SOLID Principals
- S - Single Responsibility Principal
- O - Open-close Principal
- L - Liskov Substitution method (can be replaced with base class)
- I - Interface Segregation Principal (have as many interface)
- D - Dependency Inversion Principal(depend on inface not concrete class)

# Collections
- Collection
  - List
    - ArrayList
    - LinkedList
    - Vector
    - Stack
  - Queue
    - Dequeue
      - ArrayDeque
    - PriorityQueue
  - Set
    - HashSet
    - LinkedHashSet
    - SortedSet
      - TreeSet
- Map
  - HashMap
  - Hastable
  - TreeMap

# Data Structures
- Liner
  - Array
    - 1d
    - 2d
    - 3d
  - Stack - LIFO
  - Queue - FIFO
- Non-linear
  - Tree
  - Graphs
  - Sets
# Algo
- Bubble sort
  
# Java 8

## Generics
  - Generics means parameterized types
  ```java
    class Test<T> {
        T obj;
        Test(T o) {
            this.obj = o;
        }
        public T get(){
            return this.obj;
        }

        //Uses
        Test<Integer> iObj = new Test<Integer>(15);
   }
  ```

## Lambda
 - short block of code which takes in parameters and returns a value
    ```java
    parameter -> expression
    (parameter1, parameter2) -> expression
    (parameter1, parameter2) -> { code block }
    ```
## Functional Interfaces
 - contains only one abstract method
 - `@FunctionalInterface`
    ```java
    new Thread(new Runnable() {
        @Override
        public void run() {
            System.out.println("asas");
        }
    });
    ```
  - Consumer - Takes value(1/2)  returns nothing
    - Bi-consumer
    ```java
        Consumer<Integer> consumer = (value) -> System.out.println(value);
        Consumer<Integer,String> consumer = (val1, val2) -> System.out.println(val2 + val1 );
    ```
  - Predicate - Retuns boolean
    - Bi-predicate
    ```java
        Predicate<Integer> isGreaterThanZero = (val) -> val > 0;
        Predicate<Integer, Integer> isGreaterThan = (val1, val2) -> val1 > val2;

        // Uses
        isGreaterThanZero.test(100);
    ```
  - Function 
    - Bi-function
    ```java
    @FunctionalInterface
    public interface BiFunction<T, U, R> 
    {
        R apply(T t, U u);
    }
    ```
  - Supplier
    ```java
        @FunctionalInterface
        public interface Supplier<T>{
            T.get();
        }
    ```
## Optional
    ```java
    Optional<String> empty = Optional.empty();
    Optional<String> opt = Optional.of(name);
    opt.isPresent()
    Optional<String> opt = Optional.ofNullable(name);
    Optional<String> opt = Optional.of("ayu");
    opt.ifPresent(name -> System.out.println(name.length()));
    String nullName = null;
    String name = Optional.ofNullable(nullName).orElse("john");
    ```
## Streams
  ```java
  Stream<String> streamEmpty = Stream.empty();
  Stream<String> stream = Stream.of(list);
  Stream.iterate(40, n -> n + 2).limit(20);
  Stream.generate(() -> "element").limit(10);
  IntStream.range(1, 3);
  ```

# Design patterns
  - Creational Patterns
    - Factory design pattern
      - Creation logic is hidden
      - One class is responsible to create objects of different types
    - Builder design
      - static Builder class
    - Prototype design
    - Singleton design
  - Structural Patterns
    - Adaptor design 
      - lets incompatible objects collaborate
    - Facade design
    - Proxy design
      - represents functionality of another class
  - Behavioural Patterns
    - Command pattern
    - Iterator pattern
    - Observer pattern
    - Strategy pattern
# Multithreding
  ## Executor Framework
  ## Fork and Join
# Messaging Queue
# Database
  ## Data Modeling
  ## Database Isolation
# Profiler - Java
# Garbage Collection
# JVM
# Logical Views
# Sequential Views
# Application Layring
# NFR- Non functional Requirement
  - Performance
  - Latency
  - Avalability
  - Depoyment time
  - etc
# Testing(Unit testing tools, TTD)
# Quality Plugin
  - Sonarcube
# Jenkins
  - 
# Docker
  - 
# Kubernaties
  - 
# Logging Tools
  - E = Elasticsearch
    - Log everthing, json based search, indexing
  - L = Logstash
    - Data aggregation and processing
  - K = Kibana
    - Analysis & visualization
# Cloud
  ## Serverless
    - AWS Lambda
  ## Storage Services
    - AWS s3
    - Azureit
  ## Events
  ## Notifictions
# Microservices
  ## API Gateway
  ## API Security
  ## Authentication
  ## REST Pricipals
  ## OAS Consumers/Producers
  ## Error Handling
  ## Filteration
  ## Patterns(Euraka, Netflix, Zuul, Circuit Breaking)
  ## Memcaching
  ## Elastic search
