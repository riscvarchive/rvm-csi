# RVM-CSI Spec Version 1 Task Group: Charter

RVM-CSI (RISC-V eMbedded - Common Software Interface) aims to specify a source-level portability layer providing a simplified transition path between different microcontrollers based on RISC-V. It may define programming interfaces in multiple programming languages, derived from a single source of truth which determines common function and macro names and descriptions across all implemented languages.

The RVM-CSI Version 1 TG (Task Group) is responsible for defining and ratifying the first version of the RVM-CSI specification, under the oversight of the RVM-CSI SIG.  It will also demonstrate a reference implementation of the API for an example platform.  The test harness for this reference implementation will form a compatibility test suite for other implementations.

Only a C API will be considered for this version of the specification.  However, the specification is written in YAML, conforming to a schema defined by the RVM-CSI SIG.  From this YAML, parsers will auto-generate C header files and documentation.  This leaves open the option of later generating implementations in other languages from the same SSoT (Single Source of Truth).

The specification will be constructed in accordance with the aims and requirements identified in the [gap analysis document](../gap-analysis.md).

As a minimum, the following areas should be covered by version 1 of the run-time API:
- Interrupt and timer sub-system
- Discovery of fixed platform characteristics (the TG will determine a useful set of such characteristics)
- CSR and peripheral register access (including enumeration of the registers and bit-fields present and their indices / addresses / bit-masks)
- Cache maintenance operations
- PMP operations
- Processor trace control
- UART control
- “Console” output for text, redirecting to UART / semihosting / circular buffer etc. according to build options

The specification should also include:
- Guidelines on the provision of platform-specific low-level startup code.
- The format of board support packages which will provide HAL implementation code for a specific platform, along with meta-data encapsulating other information about that platform as might be required by toolkits and integrated development environments.

Other areas of functionality may also be covered, with the approval of the RVM-CSI SIG.
