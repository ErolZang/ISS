<p>Introduction to information security:</p>
<ul>
<li>Evolution of ICT systems and the security problem</li>
<li>problems and vocabulary of ICT security</li>
<li>technological attacks (sniffing, spoofing, ...)</li>
<li>non-technological attacks (social engineering)</li>
</ul>
<p>In analysis we have to identify the asset, listing the
vulnerabilities and looking at the threats, and finally we get the list
of the risks, we need to manage those risks, we have to select
countermeasures to limit the impact of the threat, we have to implement
countermeasures, and we need to “audit” it, we need to check if the
countermeasures are implemented, if they work; the testing is performed
by different engineering different from who has implemented it.</p>
<p>First axiom of engineering: The more complex a system is, the more
difficult its correctness verification will be (implementation,
management, operation) Example: The number of bugs in program is
proportional to its number of lines of code The complexity of the
current information systems is in favor of the attackers that can find
attack paths increasingly ingenious and unforeseen by the defenders.
It's better to write 10 programs with 1000LOC rather than a single
problem with 10000LOC because it's better to find and fix bugs.</p>
<ul>
<li><h3 id="personal-devices">"Personal" devices</h3>
<ul>
<li>Desktop, laptop, tablet, smartphone, ...</li>
<li>Smart TV, fridge, car, ...</li>
</ul></li>
<li><h3 id="communication-networks">Communication networks</h3>
<ul>
<li>Data-only networks (no separate analogic phone network)</li>
<li>Wired and wireless networks</li>
<li>Mobility</li>
</ul></li>
<li><h3 id="distributed-services">Distributed services</h3>
<ul>
<li>Outsourcing, hosting, farming, cloud, IoT</li>
<li>Both for the computation functions and storage ones</li>
</ul></li>
<li><h3 id="programming-increasingly-complex">Programming increasingly
complex</h3>
<ul>
<li>Stratification, frameworks, language mix, ...</li>
</ul></li>
</ul>
<p>Nowadays, everything is data, the calls too, we have a lot of
benefits for speed, but it is a threat for security. It's more
comfortable to use wireless, but wired connection is mush safer than
wireless. It's stupid to use wireless connection if we have to protect a
lot of data, we need to use cable to be more safe.</p>
<ul>
<li><h3 id="financial-loss">Financial loss</h3>
<ul>
<li>Direct (e.g. found transfer, bank attack)</li>
<li>Indirect (e.g. value of share, fine by privacy authority)</li>
</ul></li>
<li><h3 id="recovery-cost">Recovery cost</h3>
<ul>
<li>Take the system back to normal operations</li>
<li>Improve the system to avoid new attacks</li>
</ul></li>
<li><h3 id="productivity-loss">Productivity loss</h3>
<ul>
<li>Processes are stopped or delayed</li>
</ul></li>
<li><h3 id="business-disruption">Business disruption</h3>
<ul>
<li>Customers may look for alternative suppliers</li>
</ul></li>
<li><h3 id="reputation-damage">Reputation damage</h3>
<ul>
<li>Difficult to regain trust</li>
</ul></li>
</ul>
<p>If you didn't suffer from financial costs, you may have to spend
money to recover the damage. You also have to fix the problem which
caused the exploit. Business disruption: for example it can be attacked
the tracking service of Amazon, and it can cause problems for
customers.</p>
<p>This diagram shows some relations about threats, vulnerabilities and
security risks, blue parts are good for security, red one are bad for
security, black ones are the assets security control is an element or
component placed in our system to increase the secure (not to control
it).</p>
<pre class="mermaid"><code>flowchart TD

A[Security control] --&gt;|Protect against| B(Threats)
A --&gt;|Reduce| C(Security risks)
A --&gt;|Meet by| D(Security requirements)
B --&gt;|Exploit| E(Vulnerabilities)
B --&gt;|Increase| C
C --&gt;|Devalue| F(Assets)
C --&gt;|Indicate| D
C --&gt;|Increase| G(Assets values and potential impacts)
D --&gt;|Underwrite| G
E --&gt;|Increase| C
E --&gt;|Expose| F
F --&gt;|Have| G
style A fill:#00F 
style D fill:#00F
style B fill:#F00 
style C fill:#F00
style E fill:#F00 
style F fill:#000
style G fill:#000 </code></pre>
<p>We have to understand which is the risk before creating something, we
should learn how to estimate risk. We need to protect something as a
network service, it is important to identify which things are important
to offer that service:</p>
<ul>
<li>ICT resources: computers, networks etc.</li>
<li>Data: we have to protect physical and logical stuffs</li>
<li>Human resources: we have to be careful about them, because if a
single person knows the system he can be a threat for the entire system,
he could be an attacker.</li>
<li>Location: it is important the location where we use an element. For
example if I connect an USB to a malicious PC, and then I share the USB
with other computers.</li>
</ul>
<p>Vulnerabilities: a vulnerability can be a real threat, it depends on
the situation and on the environment where it is used.</p>
<p>We can find a lot of threats of our system, but is difficult to know
all of them. We have to do a ranking of threats considering the impact
of them, but also we have to consider the probability of that threat to
happen. Likewise, we are going to use a table to view the impact and the
probability. The product of them is the risk:</p>
<table>
<thead>
<tr class="header">
<th>Impact/Probability</th>
<th>Low</th>
<th>Medium</th>
<th>High</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Low</td>
<td>S</td>
<td>S</td>
<td>S</td>
</tr>
<tr class="even">
<td>Medium</td>
<td>S</td>
<td>M</td>
<td>H</td>
</tr>
<tr class="odd">
<td>High</td>
<td>H</td>
<td>H</td>
<td>H</td>
</tr>
</tbody>
</table>
<p>Security has to be in all the pass of the lifecycle of a software. We
have to respect all the passages of the lifecycle to make the system
safe. When we have to test the system we have to test different inputs,
we have to test with different semantic of input. Ex: testing 2 rather
than two. We have test to the good and to the bad case too. When I
implement the security system we have to set up security, then after
release the security is not finished, we have to manage security day by
day because there are attacks developed every day.</p>
<ul>
<li><h3 id="incident">Incident</h3>
<ul>
<li>A security event that compromises the integrity, confidentiality, or
availability of a information asset</li>
<li>an incident may create breach or data breach disclosure means that
the data come out, and they are probably exposed to anyone.</li>
</ul></li>
<li><h3 id="data-breach">(Data) Breach</h3>
<ul>
<li>An incident that results in the disclosure of potential exposure of
data</li>
</ul></li>
<li><h3 id="data-disclosure">(Data) Disclosure</h3>
<ul>
<li>A breach for which it was confirmed that data was actually disclosed
(not just exposed) to an unauthorized party</li>
</ul></li>
<li><p>ASSET = the set of goods, data, and people needed for an IT
service.</p></li>
<li><p>VULNERABILITY = intrinsic weakness of an asset</p></li>
<li><p>THREAT = possible deliberate action / accidental event that can
produce the loss of a security property by exploiting a
vulnerability</p></li>
<li><p>ATTACK = threat occurrence (deliberate action)</p></li>
<li><p>(NEGATIVE) EVENT = threat occurrence (accidental event)</p></li>
</ul>
<h3 id="kiss--keep-it-simple-stupid">KISS → Keep It Simple, Stupid</h3>
<p>Security is an important issue today because attackers can attack a
system in every place in the world. The second important point is
"money". Nowadays, all segments use internet and if an attacker exploits
a system, customers could lose money.</p>
<pre class="chart"><code>type: line
labels: [New vulnerability discovered, Exploit, Vulnerability is made public, Vendor informed of Vulnerability, Vendor notifies its customer, Security tools are updated, Patch is published, Patch is widely known, Patch is installed ]
series:
  - title: Window
    data: [100, 110, 120, 200, 210, 180, 150, 100, 0]
  - title: Exploit
    data: [0, 110, 0, 0, 0, 0, 0, 0, 0]
tension: 0.2
width: 80%
labelColors: false
fill: true
beginAtZero: true
bestFit: false
bestFitTitle: undefined
bestFitNumber: 0</code></pre>
<p>Let’s imagine that we are in t0(it’s not means that the risk is 0).
At some point someone discovered a vulnerability, and it can try to
exploit it. After the attack the vulnerability is made public, sometimes
companies inform us of the vulnerabilities, but while the companies are
trying to fix the issue we have to try to protect us from attacks, we
can use an IDS (intrusion detection system) to track the signature of
that vulnerability. After some time, company develops patch but until we
don’t install the patches we have exposed to the risk.</p>
<h4
id="the-total-time-passed-from-discovery-to-installation-is-called-windows-of-exposure">The
total time passed from discovery to installation is called windows of
exposure.</h4>
