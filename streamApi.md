* Introduce in java 1.8
* Pipelining: output of one operation become input to another operation
* Lazy evaluation: intermediate operation are not executed until the terminal operation are not invoked, this avoids unnecessary computation
* Parallel processing:
```
Stream.of(1, 2, 3, 4, 5)          // Stream source
  .filter(x -> x % 2 == 0)      // Intermediate operation
  .collect(Collectors.toList()) // Terminal operation
```
## intermediate operation:
These operation return a stream as output and that will not executed until we perform any terminal operation
* filter(Predicate interface lambda function to return boolean value)
* map(value -> value * 10(write a lambda function to perform any operation)
* sorted()
* distinct()returns a stream consisting of distinct elements of the stream
* peek()
* limit()
* skip()
## Terminal Operations
* forEach()
* forEachOrdered()
* Collector->collect(Collectors.toList());
* count()->returns the total number of elements in the stream
* reduce(): The reduce() method performs a reduction on the elements of the stream and returns the value.
*  toArray() method returns an array that contains the elements of the stream
* Stream.builder()
  Stream.builder() returns a builder (a design pattern that allows us to construct an object step-by-step) that can be used to add objects to the stream. The objects are added to the builder using the add() method. Calling build() method on the builder creates an instance of the Stream. This implementation of Stream creation is based on the famous Builder Design Pattern.
* Stream.of()
  Stream.of() method creates a stream with the specified values. This method accepts both single and multiple values. It does the work of declaring and initializing a stream.
*Arrays.stream()
  Arrays.stream() method creates a stream instance from an existing array. The resulting stream instance will have all the elements of the array.
*Parallel Stream
  By default, all stream operations are sequential in Java unless explicitly specified as parallel. Parallel streams are created in Java in two ways.

Calling the parallel() method on a sequential stream.
Calling parallelStream() method on a collection.
Parallel streams are useful when we have many independent tasks that can be processed simultaneously to minimize the running time of the program.

parallel()
parallel() method is called on the existing sequential stream to make it parallel.

## upcasting and down casting