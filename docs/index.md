<html>
  <head>
    <meta http-equiv="Content-Type" content="text/html;charset=utf-8" >
    <title>Accelerated Bounded Model Checking</title>
    <style>
      table, th, td {border: 1px solid black;}
      td {text-align: center;}
      p {text-align: justify;}
    </style>
  </head>
  <body>

    <p>
      This is the empirical evaluation of the implementation of our techniques from the paper <a href="./main.pdf"><i>Accelerated Bounded Model Checking</i></a> in the tool LoAT.
    </p>

    <h1>Getting LoAT</h1>

    <p>
      We provide a <a href="https://github.com/LoAT-developers/LoAT/releases/tag/v0.7.0">pre-compiled binary of LoAT (Linux, 64 bit)</a>.
      Moreover, you can find the source code of LoAT at <a href="https://github.com/loat-developers/LoAT/tree/v0.7.0">GitHub</a>.
    </p>
    <!--p>We refer to the <a href="https://loat-developers.github.io/LoAT/">general LoAT website</a> for further information.</p-->

    <h1>Evaluation</h1>

    <h2>Examples</h2>

    <p>
      The examples that we used for our evaluation can be found <a href="https://github.com/chc-comp/chc-comp22-benchmarks/tree/main/LIA-Lin">here</a> and <a href="https://github.com/chc-comp/chc-comp23-benchmarks/tree/main/LIA-lin">here</a>.
    </p>

    <h2>Tools</h2>

    In our evaluation, we considered the following tools and configurations:
    <ul>
      <li>LoAT v0.7.0</li>
      <ul>
        <li>LoAT's implementation of Accelerated Bounded Model Checking with blocking clauses (LoAT ABMC_block)</li>
        <li>LoAT's implementation of Accelerated Bounded Model Checking without blocking clauses (ABMC)</li>
        <li>LoAT's implementation of Bounded Model Checking (BMC)</li>
        <li>LoAT's implementation of Acceleration Driven Clause Learning (ADCL)</li>
      </ul>
      <li><a href="https://github.com/Z3Prover/z3">Z3</a> 4.12.2</li>
      <ul>
        <li>Z3's implementation of the Spacer algorithm (Spacer)</li>
        <li>Z3's implementation of Bounded Model Checking (Z3 BMC)</li>
      </ul>
      <li><a href="https://github.com/usi-verification-and-security/golem">Golem</a> 0.4.3</li>
      <ul>
        <li>Golem's implementation of Transition Power Abstraction (Golem TPA)</li>
        <li>Golem's implementation of Bounded Model Checking (Golem BMC)</li>
      </ul>
      <li><a href="https://github.com/uuverifiers/eldarica">Eldarica</a> 2.0.9 in its default configuration</li>
    </ul>

    <h2>Results</h2>

    We provide tables with the detailed results of our benchmarks:
    <ul>
      <li><a href="./2022.html">Examples from the CHC competition 2022</a></li>
      <li><a href="./2023.html">Examples from the CHC competition 2023</a></li>
    </ul>

  </body>
</html>
