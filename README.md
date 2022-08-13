# CS_Fundamentals

1. Thread vs process: https://people.cs.rutgers.edu/~pxk/416/notes/05-threads.html
2. overcommiting: 
   1) https://redis.io/docs/getting-started/faq/#background-saving-fails-with-a-fork-error-under-linux-even-if-i-have-a-lot-of-free-ram
   2) https://www.kernel.org/doc/Documentation/vm/overcommit-accounting
   3) https://serverfault.com/questions/606185/how-does-vm-overcommit-memory-work/606193#606193
   4) What happens if memory gets overcommitted?
      Suppose the pages being actively used by the current threads don't all fit in physical memory.
      Each page fault causes one of the active pages to be moved to disk, so another page fault will occur soon.
      Just run another thread?
      The system will spend all its time reading and writing pages, and won't get much work done.
      This situation is called thrashing; it was a serious problem in early demand paging systems.
