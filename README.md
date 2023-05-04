Download Link: https://assignmentchef.com/product/solved-cs411-homework3
<br>
<ol>

 <li> Consider GF(2<sup>8</sup>) used in AES with the irreducible polynomial p(x) = x<sup>8</sup>+x<sup>4</sup>+x<sup>3</sup>+x+1. You are expected to query the server “cryptlygos.pythonanywhere.com/poly/<em>&lt;your_id&gt;</em>”, which will send you two binary polynomials a(x) and b(x) in GF(2<sup>8</sup>). Polynomials are expressed as bit strings of their coefficients. For example, p(x) is expressed as ‘100011011’. You can use the Python code “<strong>py</strong>” given in the assignment package to communicate with the server.</li>

 <li> You are expected to perform c(x) = a(x)×b(x) in GF(2<sup>8</sup>) and return c(x) as bit string.</li>

 <li> You are expected to compute the multiplicative inverse of a(x) in GF(2<sup>8</sup>) and return a<sup>-1</sup>(x).</li>

 <li> Consider the Geffe generator of three LFRSs (LFSR<sub>1</sub>, LFSR<sub>2</sub>, and LFSR<sub>3</sub>) with the following connection polynomials:</li>

</ol>

C<sub>1</sub>(x) = x<sup>14</sup> + x<sup>5</sup> + 1

C<sub>2</sub>(x) = x<sup>17</sup> + x<sup>3</sup> + 1

C<sub>3</sub>(x) = x<sup>11</sup>+ x<sup>2</sup> + 1

You also observed the following output sequence of the Geffe generator:

z = [0, 1, 1, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 0, 1, 1, 0, 1, 0, 1, 0, 0, 1, 0, 0, 1, 1, 0, 1, 0, 0, 1, 0, 0, 0, 1, 0, 0, 1, 0, 0, 0, 1, 0, 0, 1, 0, 1, 0, 1, 1, 1, 1, 0, 1, 1, 0, 1, 0, 0, 1, 0, 1, 0, 0, 1, 1, 0, 0, 1, 0, 0, 1, 1, 1, 0, 0, 1, 1, 0, 0, 1, 0, 0, 0, 1, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 0, 0, 1, 0, 1, 1, 1, 0, 1, 1, 1, 1, 1, 1]

Can you find the initial states of LFSR<sub>1</sub>, LFSR<sub>2</sub>, and LFSR<sub>3</sub>?

<ol start="3">

 <li> Consider the combining function given in the following table, that is used to combine the outputs of three <strong>maximum-length</strong> LFSR sequences:</li>

</ol>

F(x<sub>1</sub>, x<sub>2</sub>, x<sub>3</sub>) = x<sub>1</sub>x<sub>2</sub> Å x<sub>1</sub>x<sub>3</sub> Å x<sub>2</sub>x<sub>3</sub> Å x<sub>1</sub>x<sub>2</sub>x<sub>3</sub>.

<ol>

 <li>The lengths of LFSRs are 79, 85, and 97, respectively. Compute the linear complexity and the period of the output sequence.</li>

 <li> Analyze the function F in terms of three criteria:</li>

</ol>

<ul>

 <li>Nonlinearity degree</li>

 <li>Balance</li>

 <li>Correlation</li>

</ul>

Is this a good combining function? Explain your answer.

<ol start="4">

 <li> Consider a modified AES without ShiftRow and Mixcolumn layers, where the secret key length is 128-bit. Show that with moderate effort you can break it.</li>

 <li> The cipher block chaining (CBC) mode has the property that it recovers from the errors (corruption, deletion, and insertion) in ciphertext blocks. Its encryption schemes are given as follows</li>

</ol>

Encryption primitive: C<sub>i</sub> = E<sub>K</sub>(P<sub>i </sub>Å C<sub>i-1</sub>)

Decryption primitive: P<sub>i</sub> = D<sub>K</sub>(C<sub>i</sub>) Å C<sub>i-1</sub>

How many blocks decrypt incorrectly if the ciphertext block C<sub>i</sub> is corrupted during transmission? Show which plaintext blocks are corrupted.




<strong>Exercise for Rainbow Tables (Non-credit question)</strong>




Consider ten digests in the attached file “<strong>rainbow_table.py</strong>”, each of which is the hash of a six-character password. Your mission is to find those passwords using the rainbow table given in the attached file “<strong>rainbowtable.txt</strong>”. Complete and submit the Python code in the file “<strong>rainbow_table.py</strong>” such that it finds and prints out the ten passwords corresponding to the digests.











