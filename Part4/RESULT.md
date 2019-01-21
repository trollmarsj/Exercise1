### What happened:
python: returns a different magic number every time
go: returns a different magic number every time
c: returns a different magic number sometimes, the rate of result being 0 is much more higher (about half of the time I get 0).

### Why:
Even though it looks like i will first increase to 1000000 and then decrease back to 0 again, but since the process of i++ and i-- involves read, modify and store, when two threads are running concurrently the process would get interrupted and run in different order, and thus produce random results other than 0.
