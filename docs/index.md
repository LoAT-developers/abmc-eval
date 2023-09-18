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
      This is the empirical evaluation of the paper <a href="???"><i>Accelerated Bounded Model Checking</i></a>.
    </p>

    <h1>Getting LoAT</h1>

    <p>
      We provide a <a href="https://github.com/LoAT-developers/LoAT/releases/tag/???">pre-compiled binary of LoAT (Linux, 64 bit)</a>.
      Moreover, you can find the source code of LoAT at <a href="https://github.com/loat-developers/LoAT/tree/???">GitHub</a>.
    </p>
    <p>We refer to the <a href="https://loat-developers.github.io/LoAT/">general LoAT website</a> for further information.</p>

    <h1>Evaluation</h1>

    <h2>Examples</h2>

    <p>
      The examples that we used for our evaluation can be found <a href="https://github.com/chc-comp/chc-comp22-benchmarks/tree/main/LIA-Lin">here</a> and <a href="https://github.com/chc-comp/chc-comp23-benchmarks/tree/main/LIA-lin">here</a>.
    </p>

    <h2>Results</h2>

    Below we provide tables with the detailed results of our benchmarks:
    <ul>
      <li>Examples from the CHC competition 2022</li>
      <ul>
        <li><a href="./abmc_block_22.html">LoAT ABMC with blocking clauses</a></li>
        <ul>
          <li>invocation: <tt>loat-static --mode reachability --format horn --engine abmc $INPUT</tt></li>
        </ul>
        <li><a href="./abmc_non_block_22.html">LoAT ABMC without blocking clauses</a></li>
        <ul>
          <li>invocation: <tt>loat-static --mode reachability --format horn --engine abmc --abmc::blocking_clauses false $INPUT</tt></li>
        </ul>
        <li><a href="./bmc_22.html">LoAT BMC</a></li>
        <ul>
          <li>invocation: <tt>loat-static --mode reachability --format horn --engine bmc $INPUT</tt></li>
        </ul>
        <li><a href="./adcl_22.html">LoAT ADCL</a></li>
        <ul>
          <li>invocation: <tt>loat-static --mode reachability --format horn --engine adcl $INPUT</tt></li>
        </ul>
        <li><a href="./z3_bmc_22.html">Z3 BMC</a></li>
        <ul>
          <li>invocation: <tt>z3 fp.engine=bmc $INPUT</tt></li>
        </ul>
        <li><a href="./spacer_22.html">Spacer</a></li>
        <ul>
          <li>invocation: <tt>z3 fp.engine=spacer $INPUT</tt></li>
        </ul>
        <li><a href="./golem_tpa_22.html">Golem TPA</a></li>
        <ul>
          <li>invocation: <tt>golem -l QF_LIA -e split-tpa $INPUT</tt></li>
        </ul>
        <li><a href="./golem_bmc_22.html">Golem BMC</a></li>
        <ul>
          <li>invocation: <tt>golem -l QF_LIA -e bmc $INPUT</tt></li>
        </ul>
        <li><a href="./eld_22.html">Eldarica</a></li>
        <ul>
          <li>invocation: <tt>eld $INPUT</tt></li>
        </ul>
      </ul>
      <li>Examples from the CHC competition 2023</li>
      <ul>
        <li><a href="./abmc_block_23.html">LoAT ABMC with blocking clauses</a></li>
        <li><a href="./abmc_non_block_23.html">LoAT ABMC without blocking clauses</a></li>
        <li><a href="./bmc_23.html">LoAT BMC</a></li>
        <li><a href="./adcl_23.html">LoAT ADCL</a></li>
        <li><a href="./z3_bmc_23.html">Z3 BMC</a></li>
        <li><a href="./spacer_23.html">Spacer</a></li>
        <li><a href="./golem_tpa_23.html">Golem TPA</a></li>
        <li><a href="./golem_bmc_23.html">Golem BMC</a></li>
        <li><a href="./eld_23.html">Eldarica</a></li>
      </ul>
    </ul>

  </body>
</html>
