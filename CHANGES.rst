==========
What's New
==========

0.3.post2 (2017-09-20)
======================

* Add input-schema.yaml file to installer

0.3.post1 (2017-09-20)
======================

* Add LICENSE to manifest

0.3 (2017-09-20)
================

* **ESPEI input is now described by a file.** This change is breaking. Old command line arguments are not supported. See `Writing input files <http://espei.org/en/latest/writing_input.html>`_ for a full description of all the inputs.
* New input options are supported, including modifying the number of chains and standard deviation from the mean
* ESPEI is now available on conda-forge
* TinyDB 2 support is dropped in favor of TinyDB 3 for conda-forge deployment
* Allow for restarting previous mcmc calculations with a trace file
* Add Cu-Mg example to documentation

0.2.1 (2017-08-17)
==================

Fixes to the 0.2 release plotting interface

* ``multiplot`` is renamed from ``multi_plot``, as in docs.
* Fixed an issue where phases in datasets, but not in equilibrium were not plotted by dataplot and raised an error.

0.2 (2017-08-15)
==================

* New ``multiplot`` interface for convienent plotting of phase diagrams + data. ``dataplot`` function underlies key data plotting features and can be used with ``eqplot``. See their API docs for examples. Will break existing code using multiplot.
* MPI support for local/HPC runs. Only single node runs are explictly supported currently. Use ``--scheduler='MPIPool'`` command line option. Requires ``mpi4py``.
* Default debug reporting of acceptance ratios
* Option (and default) to output the log probability array matching the trace. Use ``--probfile`` option to control.
* Optimal parameters are now chosen based on lowest error in chain.
* Bug fixes including
   
   - py2/3 compatibiltiy
   - unicode datasets
   - handling of singular matrix errors from pycalphad's ``equilibrium``
   - reporting of failed conditions

0.1.5 (2017-08-02)
==================

* Significant error checking of JSON inputs.
* Add new ``--check-datasets`` option to check the datasets at path. It should be run before you run ESPEI fittings. All errors must be resolved before you run.
* Move the espei script module from ``fit.py`` to ``run_espei.py``.
* Better docs building with mocking
* Google docstrings are now NumPy docstrings

0.1.4 (2017-07-24)
==================

* Documentation improvements for usage and API docs
* Fail fast on JSON errors

0.1.3 (2017-06-23)
==================

* Fix bad version pinning in setup.py
* Explicitly support Python 2.7

0.1.2 (2017-06-23)
==================

* Fix dask incompatibilty due to new API usage

0.1.1 (2017-06-23)
==================

* Fix a bug that caused logging to raise if bokeh isn't installed

0.1 (2017-06-23)
==================

ESPEI is now a package! New features include

* Fork https://github.com/richardotis/pycalphad-fitting
* Use emcee for MCMC fitting rather than pymc
* Support single-phase only fitting
* More control options for running ESPEI from the command line
* Better support for incremental saving of the chain
* Control over output with logging over printing
* Significant code cleanup
* Better usage documentation

