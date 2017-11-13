# Release 0.3 Info

This file contains the exit criteria, schedule, and work list for release 0.3.

## Release Goals

* Establish and document the model we will use for ONNX releases going forward.
* Establish and document the versioning rules for this and subsequent ONNX releases.
* Provide a stable (yet not final) version of ONNX that the community can engineer against and early products can ship against.
* Produce a 1.0.0 of the IR and focus future innovation on operators/algorithms.
* Define the minimal pre-1.0.0 operator set that will unblock key early software releases.  
* Add support for non-DNN operators in ONNX models (a.k.a., ONNX-ML).

## Exit Criteria

* This release SHOULD NOT have functionality that isn't needed to satisfy the release goals above.
* This release MUST define IR_VERSION 1.0.0 to slow down churn on the abstract model and protobuf format.
* This release MUST NOT define operators with 1.0.0 or later to avoid premature calcification. 
* This release MUST define the following operators as "production":
    * **TBD**: *eta for first draft 2017-11-3, finalize by 11-10*
* This release MUST NOT define any operators as "production" that are not in the list above.
* This release MAY define a small number of "experimental" operators that conformant implementations MAY elect to not implement. 
* This release MUST have an IR that provides sufficient functionality to support non-DNN ML operators naturally. 

## Schedule

| Date | Outcome |
| --- | --- |
| 2017-11-11 | IR_VERSION is 0.0.4. Critical bug fix only. |
| 2017-11-13 | Release artifacts posted with 0.3.0-beta tag. |
| 2017-11-14 | Production operator list is locked. |
| 2017-11-15 | IR_VERSION is 1.0.0. |
| 2017-11-17 | Production operator signatures and semantics are locked. |
| 2017-11-20 | 0.3.0-rc build. Critical bug fixes only after this point.  |
| 2017-12-01 | Final 0.3.0 build. All fixes beyond this are patches and subject to ONNX versioning rules.  IR_VERSION is 1.0.0, operator versions are 0.n.n. |


## Work Items

The following list of work needs to get done to complete the release.  Because *the pen only writes one name* we indicate a 
single person to be directly responsible for getting the right outcome, which typically 
involves working well with others.  

| Assigned To | Due Date | Status | Description |
| --- | --- | --- | --- |
| dbox        | 2017-11-05 | Active | ONNX: Versioning policy for changing wire-compatible data types undefined. |
| edward      | 2017-11-05 | Active | ONNX: Versioning impact of transitive dependencies undefined. |
| stuart      | 2017-11-05 | Active | Operator inventory list needs to be defined. |
| stuart      | 2017-11-05 | Active | Operator signatures and semantics needs to be defined. |
 
