# Tutorial Pemrograman Lanjut
## Nayla Farah Nida - 2306213426

### Module 5
<details>
  <summary>Endpoint /all-student</summary>
  
  Before optimizing:
  ![](images/all-student_testResult_before_optimize.png)
  ![](images/all-student_JMeter_before_optimize.png)
  ![](images/all-student_before_optimize.png)
    
  After optimizing:
  ![](images/all-student_JMeter_after_optimize.png)
  ![](images/all-student_after_optimize.png)
  
    
  **CPU TIME**
  
  Before : ```9356 ms```
  
  After  : ```612 ms```
  
  Improvement :  **93.46%**
    
</details>

<details>
  <summary>Endpoint /all-student-name</summary>
  
  Before optimizing:
  ![](images/all-student-name_testResult_before_optimize.png)
  ![](images/all-student-name_JMeter_before_optimize.png)
  ![](images/all-student-name_before_optimize.png)
    
  After optimizing:
  ![](images/all-student-name_JMeter_after_optimize.png)
  ![](images/all-student-name_after_optimize.png)
  
    
  **CPU TIME**
  
  Before : ```879 ms```
  
  After  : ```225 ms```
  
  Improvement :  **74.40%**
    
</details>

<details>
  <summary>Endpoint /highest-gpa</summary>
  
  Before optimizing:
  ![](images/highest-gpa_testResult_before_optimize.png)
  ![](images/highest-gpa_JMeter_before_optimize.png)
  ![](images/highest-gpa_before_optimize.png)
    
  After optimizing:
  ![](images/highest-gpa_JMeter_after_optimize.png)
  ![](images/highest-gpa_after_optimize.png)
  
    
  **CPU TIME**
  
  Before : ```238 ms```
  
  After  : ```84 ms```
  
  Improvement :  **64.71%**
    
</details>

**Conclusion**

The performance profiling and optimization resulted in significant improvements across all tested endpoints. For the /all-student endpoint, the CPU time was reduced by 93.46%, from 9356 ms to 612 ms. The /all-student-name endpoint saw a 74.40% improvement, reducing from 879 ms to 225 ms, while the /highest-gpa endpoint improved by 64.71%, from 238 ms to 84 ms.

### Reflection

**1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?**

JMeter focuses on external performance testing by simulating real-world traffic and load, while IntelliJ Profiler focuses on internal performance analysis by tracking how the code is executed at a deeper level. For example, in this tutorial, we use JMeter to detect the slow endpoint ```all-student``` and Intellij Profiler identifies the root cause which in this case is the line ```studentCourseRepository.findByStudentId()```.

**2. How does the profiling process help you in identifying and understanding the weak points in your application?**

Profiling helps me identifies the most time consuming methods, monitors my CPU and Memory usage, and gives me overall visual representation of performance, making it faster and more efficient doing performance improvements.

**3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?**

Yes, for me, Intellij Profiler is effective in helping me reduce CPU time and improving overall system performance.

**4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?**

For me, the difficult part is trying to interpret JMeter Results, response time graphs and throughput metrics can be complex. Also, finding a way to optimize the code is also quite challenging.

**5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?**

I think the main benefits from using Intellij Profiler is that it gives me a visual representation of performance issues, and provides deep insights into the root cause of performance issues.

**6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?**

I did not find (or perhaps did not notice) any inconsistencies between JMeter and IntelliJ Profiler because I use them for different purposes. JMeter is for identifying performance under high traffic load, while IntelliJ Profiler is for pinpointing which method or SQL query is slow.

**7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?**

I did some refactoring and reduce unnecessary loops or switch to stream-based operations for better performance, then I use IntelliJ Profiler to confirm CPU and memory usage are reduced. To ensure that no functionality is broken, I use Postman to manually check critical endpoints.
