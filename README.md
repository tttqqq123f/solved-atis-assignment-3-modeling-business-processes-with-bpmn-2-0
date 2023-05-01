Download Link: https://assignmentchef.com/product/solved-atis-assignment-3-modeling-business-processes-with-bpmn-2-0
<br>
We practice our understanding of the semantics of BPMN 2.0. Remember the following assumptions made for a BPMN process model as discussed in the lecture:

<ul>

 <li>When a task starts upon arrival of a token, it will finish at some point and release the token when it is finished.</li>

 <li>In an XOR branching gateway, exactly one outgoing branch is activated. For an XOR merging gateway, every arriving token will be sent on by the gateway.</li>

</ul>







<strong>Task 1</strong>: Decide if the following statements about process models are true or false and give a short justification for your answer. The models abstract from specific conditions specified at an XOR gateway. This means, exactly one outgoing branch will be activated, but you do not which one.




Simply write your answers below the statement.







<ol>

 <li>a)</li>

</ol>













<ol>

 <li>b)</li>

</ol>

C is executed after A or B have finished.

C is executed exactly two times.







D is executed exactly once in c) each instance.




<strong> </strong>

<strong> </strong>

C is executed several times

<ol>

 <li>d) in some instances.</li>

</ol>

<strong> </strong>

<strong> </strong>

<ul>

 <li>The process never ends.</li>

</ul>

<ol>

 <li>e)</li>

</ol>







<ul>

 <li>When the process starts, either A or B are executed. Subsequently, C is executed.</li>

</ul>

<strong><sup>           </sup></strong>

<strong> </strong>

<strong> </strong>

<ol>

 <li>f)</li>

</ol>

<strong> </strong>A can never be executed.

<strong> </strong>

<strong> </strong>

<ol>

 <li>g)</li>

</ol>

A is executed infinitely often.

<strong> </strong>




Any model with only AND gateways and no cyclic paths is sound.

(The picture on the left illustrates one possible example model.)

<strong> </strong>

<strong> </strong>

Any model with only XOR gateways, but cyclic paths cannot contain a Lack of Synchronization error. i)

<strong>  </strong>

<strong> </strong>

<strong>Task 2</strong>: Create a BPMN 2.0 model for a Mortgage Approval process, which is used by a bank to decide whether a customer request for a mortgage loan can be granted. Use pools for the customer and the bank. Add message flows between the pools. Within the customer and bank processes use events, tasks, and XOR or AND gateways. Use other gateways only if necessary. Remember to name all elements in the model.




The process proceeds as follows:

A customer needs a loan to finance a house. The customer fills in an application form for a mortgage and prepares all necessary documents. Then, the customer sends the filled-in application to the bank. The customer waits for the response from the bank. This response comes as a letter and can contain one of the following 3 possible answers:




<h2>Architectural Thinking for Intelligent Systems</h2>




<ol>

 <li>The documents were not correctly filled in by the customer and are therefore returned by the bank. In this case, the customer needs to rework the documents and resubmit again. This process can repeat several times until the application is accepted by the bank.</li>

</ol>




<ol>

 <li>The bank declines the application. The customer process ends.</li>

</ol>







<ol>

 <li>The bank accepts the application and sends an offer for the mortgage. The customer reviews this offer and decides to accept or reject it. If the customer accepts the offer, she signs and returns the offer to the bank. Otherwise, the customer process ends.</li>

</ol>




When an application for a mortgage loan arrives, the “Mortgage Loan Request” process is triggered at the bank. The application is first reviewed for completeness. If it is incomplete, the documents must be returned to the customer to add missing information. If the application is complete, the bank reviews the application. In an assessment subprocess, two conditions are checked:

<ul>

 <li>The customer’s credit history is checked automatically by a system.</li>

 <li>The appraisal of the property is carried out by a property appraiser.</li>

</ul>

Once both, the risk assessment and the property appraisal have been performed, a loan officer can assess the applicant’s eligibility. If the applicant is not eligible, the application is rejected, otherwise the acceptance pack is prepared. The loan officer sends the response of the bank to the customer and waits to hear from the customer again within 4 weeks.




If the customer does not reply within the 4 weeks, the process at the bank ends. If the customer replies and accepts the offer, the loan officer opens an account, and the bank process ends.

<strong>Task 3:  </strong>What states do you propose for the application business object? Draw its lifecycle.