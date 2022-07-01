**Multi-programming_Operating_System-MOS-_Phase2**

#ASSUMPTIONS:

    1. Jobs may have program errors

    2. PI interrupt for program errors introduced

    3. No physical separation between jobs

    4. Job outputs separated in output file by 2 blank lines

    5. Paging introduced, page table stored in real memory

    6. Program pages allocated one of 30 memory block using random number generator

    7. Load and run one program at a time

    8. Time limit, line limit, out-of-data errors introduced

    9. TI interrupt for time-out error introduced

    10. 2-line messages printed at termination

**#Errors*

        0    No Error
        
        1    Out of Data
        
        2    Line Limit Exceeded
        
        3    Time Limit Exceeded
        
        4    Operation Code Error
        
        5    Operand Error
        
        6    Invalid Page Fault

#**NOTATIONS**
        
        M: memory
        
        IR: Instruction Register (4 bytes)
        
        IR [1, 2]: Bytes 1, 2 of IR/Operation Code
        
        IR [3, 4]: Bytes 3, 4 of IR/Operand Address
        
        M[&]: Content of memory location 
        
        IC: Instruction Counter Register (2 bytes)
        
        R: General Purpose Register (4 bytes)
        
        C: Toggle (1 byte)
        
        PTR: Page Table Register (4 bytes)
        
        PCB: Process Control Block (data structure)
        
        VA: Virtual Address
        
        RA: Real Address
        
        TTC: Total Time Counter
        
        LLC: Line Limit Counter
        
        TTL: Total Time Limit
        
        TLL: Total Line Limit
        
        EM: Error Message
        
        
#**INTERRUPT VALUES**
        SI = 1 on GD
        
           = 2 on PD
           
           = 3 on H
           
        TI = 2 on Time Limit Exceeded
        
        PI = 1 Operation Error
        
           = 2 Operand Error
           
           = 3 Page Fault
        
