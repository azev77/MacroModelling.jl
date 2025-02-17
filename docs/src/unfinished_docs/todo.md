# Todo list:
## High priority:
- [x] Get functions: get_output, get_moments
- [x] estimation, IRF matching, system priors
- [x] check derivative tests with finite diff
- [ ] clean up printouts/reporting
- [ ] release first version
- [ ] clean up function inputs and harmonise AD and standard commands
- [ ] figure out combinations for inputs (parameters and variables in different formats for get_irf for example) 
- [ ] write documentation/docstrings
- [ ] revisit optimizers for SS
- [ ] write tests and documentation for solution, estimation... making sure results are consistent
- [ ] figure out licenses
- [ ] add more models
- [ ] symbolic derivatives
- [ ] use @assert for errors or maybe argcheck
- [ ] print SS dependencies, show SS solver
- [ ] an and schorfheide estimation
- [ ] SS: replace variables in log() with auxilliary variable which must be positive to help solver
- [ ] plot multiple solutions or models - multioptions in one graph
- [ ] add correlation, autocorrelation, and variance decomposition

## Not high priority:
- [x] implement blockdiag with julia package instead of python
- [ ] estimation codes with missing values (adopt kalman filter)
- [ ] whats a good error measure for higher order solutions (taking whole dist of future shock into account)? use mean error for n number of future shocks
- [ ] implement global solution methods
- [ ] more options for IRFs, pass on shock vector, simulate only certain shocks
- [ ] improve redundant calculations of SS and other parts of solution
- [ ] find way to recover from failed SS solution which is written to init guess
- [ ] restructure functions and containers so that compiler knows what types to expect
- [ ] use RecursiveFactorization and TriangularSolve to solve, instead of MKL or OpenBLAS
- [ ] fix SnoopCompile with generated functions
- [ ] rewrite first order with riccati equation MatrixEquations.jl
- [ ] exploit variable incidence and compression for derivatives
- [ ] for estimation use CUDA with st order: linear time iteration starting from last 1st order solution and then LinearSolveCUDA solvers for higher orders. this should bring benefits for large models and HANK models
- [ ] test on highly nonlinear model (https://www.sciencedirect.com/science/article/pii/S0165188917300970)
- [ ] pull request in StatsFuns to have norminv... accept type numbers and add translation from matlab: norminv to StatsFuns norminvcdf
- [ ] conditions for when to use which solution. if solution is outdated redo all solutions which have been done so far and use smart starting points
- [ ] more informative errors when declaring equations/ calibration
- [ ] unit equation errors
- [ ] implenent reduced linearised system solver + nonlinear
- [ ] implement HANK
- [ ] implement automatic problem derivation (gEcon)
- [ ] write to dynare
- [ ] print legend for algorithm in last subplot of plot only
- [ ] conditional forecasting
- [ ] speed up 2nd moment calc for large models. maybe its only the derivatives but its slow for SW03
- [ ] redo ugly solution for selecting parameters to differentiate for
- [ ] select variables for moments

- [x] Revise 2,3 pert codes to make it more intuitive 
- [x] Pretty print linear solution
- [x] write function to get_irfs
- [x] Named arrays for irf
- [x] write state space function for solution
- [x] Status print for model container
- [x] implenent 2nd + 3rd order perturbation
- [x] implement fuctions for distributions
- [x] try speedmapping.jl - no improvement
- [x] moment matching
- [x] write tests for higher order pert and standalone function
- [x] add compression back in
- [x] FixedPointAcceleration didnt improve on iterative procedure
- [x] add exogenous variables in lead or lag
- [x] regex in parser of SS and exo
- [x] test SS solver on SW07
- [x] change calibration, distinguish SS/dyn parameters
- [x] plot multiple solutions at same time (save them in separate constructs)
- [x] implement bounds in SS finder
- [x] map pars + vars impacting SS
- [x] check bounds when putting in new calibration
- [x] Save plot option
- [x] Add shock to plot title
- [x] print model name
