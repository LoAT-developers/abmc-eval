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
      This is the empirical evaluation of the implementation of our techniques from the paper <a href="https://arxiv.org/abs/2401.09973"><i>Accelerated Bounded Model Checking</i></a> in our tool LoAT.
    </p>

    <h1>Getting LoAT</h1>

    <p>
      We provide a <a href="https://github.com/LoAT-developers/LoAT/releases/tag/v0.7.0">pre-compiled binary of LoAT (Linux, 64 bit)</a>.
      Moreover, you can find the source code of LoAT at <a href="https://github.com/loat-developers/LoAT/tree/v0.7.0">GitHub</a>.
    </p>
    <p>We refer to the <a href="https://loat-developers.github.io/LoAT/">general LoAT website</a> for further information.</p>

    <h1>Evaluation</h1>

    <h2>Examples</h2>

    <p>
      We used the examples from the category LIA-Lin (linear CHCs with linear integer arithmetic) from the <a href="https://chc-comp.github.io/2023/">CHC competition</a> 2023.
      They can be found <a href="https://github.com/chc-comp/chc-comp23-benchmarks/tree/main/LIA-lin">here</a>.
    </p>

    <h2>Tools</h2>

    In our evaluation, we considered the following tools and configurations:
    <ul>
      <li>LoAT 0.7.0</li>
      <ul>
        <li>Accelerated Bounded Model Checking with blocking clauses (LoAT ABMC_b)</li>
        <ul>
          <li><tt>loat-static --mode reachability --format horn --engine abmc $INPUT</tt></li>
        </ul>
        <li>Accelerated Bounded Model Checking without blocking clauses (LoAT ABMC)</li>
        <ul>
          <li><tt>loat-static --mode reachability --format horn --engine abmc --abmc::blocking_clauses false $INPUT</tt></li>
        </ul>
        <li>Bounded Model Checking (LoAT BMC)</li>
        <ul>
          <li><tt>loat-static --mode reachability --format horn --engine bmc $INPUT</tt></li>
        </ul>
        <li>Acceleration Driven Clause Learning (LoAT ADCL)</li>
        <ul>
          <li><tt>loat-static --mode reachability --format horn --engine adcl $INPUT</tt></li>
        </ul>
      </ul>
      <li><a href="https://github.com/Z3Prover/z3">Z3</a> 4.13.0</li>
      <ul>
        <li>the Spacer algorithm (Spacer)</li>
        <ul>
          <li><tt>z3 fp.engine=spacer $INPUT</tt></li>
        </ul>
        <li>Bounded Model Checking (Z3 BMC)</li>
        <ul>
          <li><tt>z3 fp.engine=bmc $INPUT</tt></li>
        </ul>
      </ul>
      <li><a href="https://github.com/usi-verification-and-security/golem">Golem</a> 0.5.0</li>
      <ul>
        <li>Transition Power Abstraction (Golem TPA)</li>
        <ul>
          <li><tt>golem -l QF_LIA -e split-tpa $INPUT</tt></li>
        </ul>
        <li>Bounded Model Checking (Golem BMC)</li>
        <ul>
          <li><tt>golem -l QF_LIA -e bmc $INPUT</tt></li>
        </ul>
      </ul>
      <li><a href="https://github.com/uuverifiers/eldarica">Eldarica</a> 2.1.0</li>
      <ul>
        <li>CEGAR with acceleration as preprocessing</li>
        <ul>
          <li><tt>eld -splitClauses:1 -abstract:off -stac $INPUT</tt></li>
        </ul>
        <li>Symbolic Execution</li>
        <ul>
          <li><tt>eld -splitClauses:1 -sym $INPUT</tt></li>
        </ul>
      </ul>
    </ul>

    <h2>Results</h2>

    <a href="./2023.html">Here</a> you can find a table with the detailed results of our benchmarks.

  </body>
</html>
