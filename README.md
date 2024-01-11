<h1>Risk Management using Quantitative Analysis</h1>

<h2>Description</h2>
This lab provided real world examples of how a Cybersecurity Engineer could respond to and manage risk by quantifying whether a safeguard or control implementation is cost effective for the organization.<br/>

Three scenarios are presented graphically that will answer the following questions and give the data necessary to calculate if the proposed safeguard is cost effective: 
<i>
 - What is the asset?
 - What is the relative risk to this asset?
 - What is the value of the asset in dollars?
 - What is the Exposure Factor, as a percentage?
 - What is the Annual Rate of Occurrence?
 - What is the type of safeguard to mitigate the risk?
 - What is the cost of this safeguard?
 - What is the Exposure Factor after implementing this safeguard? 
 - Is this Safeguard cost effective to implement?
</i>
   <br /> <br />

For a cybersecurity engineer to respond to risk, a decision has to be made about whether they will <u>avoid, transfer, mitigate or accept a risk to an asset</u>. One option is to use a framework to assess the risk, such as <b>NIST SP 800-30</b>, which provides a system to frame, assess, analyze and respond to risks. This project will demonstrate a process to quantitatively respond to risks based on hypothetical business scenarios. We'll need a few <b>definitions</b> of acronyms to help explain what is going on: <br /><br />

<b>Single Loss Expectancy (SLE)</b> is the loss incurred due to the realization of a threat represented as a monetary value.<br /><br />
<b>Asset Value (AV)</b> is the monetary valuation of an asset.<br /><br />
<b>Exposure Factor (EF)</b> is the percentage of loss a realized threat can cause to an asset.<br /><br />
<b>Annualized Loss Expectancy (ALE)</b> is the loss the company expects to lose per year due to the threat.<br /><br />
<b>Annualised Rate of Occurrence (ARO)</b> is the expected number of times this threat is realized yearly, i.e., frequency per year.<br /><br />

<br />

<b>How do we actually use these classifications?</b><br />

To calculate Single Loss Expectancy: SLE = AV x EF

To calculate Annualized Loss Expectancy: ALE = SLE x ARO

To calculate Value of Safeguard: VSG = ALEBeforeSafeguard - ALEAfterSafeguard - AnnualCostOfSafeguard

If the final calculation is positive, the safeguard is a benefit and should be implemented, if the final calculation is negative the safeguard is a loss and shouldn’t be implemented. 



<h2>Languages and Utilities Used</h2>

- <b>None</b> 

<h2>Environments Used </h2>

- <b>TryHackMe Lab Environment</b> 

<h2>Project walk-through:</h2>

<p align="center">
  
<h3>Example 1</h3>
<br />
<img src="https://i.imgur.com/KAa0op0.png" height="80%" width="80%" alt="Risk Management"/>
ALEBefore<br/>
= SLE x ARO<br />
= (10000)(0.25)(0.35)<br />
= 875 <br />
 <br />
ALEAfter<br />
= SLE x ARO<br />
= (10000)(0.0)(0.35)<br />
= 0<br />
<br />
ValueOfSafeguard<br />    
= 875 - 0 - 400<br />
= <b>475</b><br />

In this scenario, the risk to a server is a power supply failure which can be mitigated by a Hot Standby. The overall value of the safeguard is calculated to be <b>$475</b>, implement the safeguard.
<br />
<br />

<h3>Example 2</h3>
<br />
<img src="https://i.imgur.com/uDyhdp2.png" height="80%" width="80%" alt="Risk Management"/>
ALEBefore<br />
= SLE x ARO<br />
= (2000)(1.0)(0.5)<br />
= 1000<br />
 <br />
ALEAfter<br />
= SLE x ARO<br />
= (2000)(0.5)(0.5)<br />
= 500<br />
<br />
ValueOfSafeguard 	<br />
= 1000 - 500 - 20<br />
= <b>480</b><br />
<br />
In this scenario, the risk to a laptop is a physical theft outside the office which can be mitigated by a encryption. The overall value of the safeguard is calculated to be <b>$480</b>, implement the safeguard.
<br />
<br />

<h3>Example 3</h3>
<br />
<img src="https://i.imgur.com/clsiXmp.png" height="80%" width="80%" alt="Risk Management"/>
ALEBefore<br /> 		
= SLE x ARO<br /> 
= (2000)(0.5)(0.25)<br /> 
= 250<br /> 
 <br /> 
ALEAfter<br />  
= SLE x ARO<br /> 
= (2000)(0.1)(0.25)<br /> 
= 50<br /> 
<br /> 
ValueOfSafeguard<br />  	
= 250 - 50 - 1500<br /> 
= <b>-1300</b><br /> 
<br /> 
In this scenario, the risk to a laptop is physical damage from falling which can be mitigated by a rugged design. The overall value of the safeguard is calculated to be <b>-$1300</b>, the safeguard cost outweighs the potential risk, do not implement the safeguard.
<br />
<br />

</p>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
