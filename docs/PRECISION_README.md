The following is a list of find/replace commands to convert Pyranda's Fortran code from double to single. You should exclude the following two files from the find/replace: nrutil.f90, nrtype.f90

Type definitions of variables:
    real(kind=8) -> real(kind=4)
    REAL(c_double) -> real(kind=4)
    real(kind=c_double) -> real(kind=4)
    DOUBLE PRECISION -> REAL
    MPI_DOUBLE_PRECISION -> MPI_REAL
Function converting values to double/single:
    DBLE( -> SNGL(
Type specification of numbers defined in the code:
    _8 -> _4
    D0 -> E0
    D([+-]\d+) -> E$1       (using regex)