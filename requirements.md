> WIP
> Information on efficient Requirements elication & creation, combined with Requirements Quality Management (to avoid defects) for future Claude Skills

# Requirements

Very often, you have system requirements, worded in the language of the application domain.
Example: SYS1: „The system prevents the user from entering a ski slope that is too difficult for him/her“.

The system requirements are broken down into requirements specifications, worded in the language of the product.
Examples:
SPEC1: „Using the speed sensor, the system collects data about near accidents of the user: A rapid drop in
speed (-20 km/h in < 1 sec) followed by a standstill that lasts at least 30 minutes is counted as a near
accident.“
SPEC2: „Using the GPS sensor, the system collects data about the total number of skiing kilometers.“

The breakdown of system requirements into specifications rests on assumptions:
Examples:
AS1: „The speed sensor is working.“
AS2: „The GPS sensor is working.“
AS3: „A near accident can be detected by a rapid drop in speed (-20 km/h in < 1 sec) followed by a
standstill that lasts at least 30 minutes.“

Note the following connections: If some of the assumptions are wrong, then the requirements specification does not fulfil the system requirements.

1. Try to implement the requirements first that have the highest
probability of turning out to be impossible to implement,
because if they are, you still have time to change the architecture or
even stop the project („fail early“).
2. Try to implement the requirements first that have the most
customer value.
A combination of 1) and 2) is perfectly risk-based.

# Traceability

What makes software easily repairable?
Major drivers are
- traceability – without it, we cannot find the part to repair
- defect management – without it, we are not able to organize the removal of larger numbers of defects
- architecture – without it, each change creates new defects.

As the purpose of the project is to fulfil the requirements, everything in the project must be traceable to the requirements.
„Everything“ encompasses both 
- software engineering artifacts (packages, test cases, ...) and
- project management artifacts (work packages, risks, ...).
- 
Traceability typically is represented as a matrix or as links.

e.g. for each package there must be requirements that would be incompletely fulfilled without that package. If that were not the case the package would contribute nothing to the fulfilment of the requirements. 
The package, therefore, would be superfluous. So for each package, there are requirements the package contributes to. 
It is a good idea to document those connections (e.g. as comments in the package or in a separate spreadsheet or as hyperlinks in the requirements management tool or ...).
