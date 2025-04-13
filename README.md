# CBT834
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 834 is from Alexander I. Vasilenko and contains an edit   *   FILE 834
//*           macro which helps you allocate datasets from one      *   FILE 834
//*           system to another system, and it preserves all the    *   FILE 834
//*           allocation attributes.  You supply a list of datasets *   FILE 834
//*           to the macro and edit them on the sending system.     *   FILE 834
//*           The macro then runs LISTDSI and fills in all the      *   FILE 834
//*           dataset attributes on the right side of the file.     *   FILE 834
//*           (The file has to be at least LRECL=131.)  On the      *   FILE 834
//*           sending system, you invoke the macro as:              *   FILE 834
//*                                                                 *   FILE 834
//*                MIGRATE REQ       (This puts attributes into     *   FILE 834
//*                                   the file list of datasets.)   *   FILE 834
//*                                                                 *   FILE 834
//*           On the receiving system, you edit the same (modified) *   FILE 834
//*           file that was produced by the MIGRATE REQ command     *   FILE 834
//*           on the sending system.  This time, you invoke:        *   FILE 834
//*                                                                 *   FILE 834
//*                MIGRATE ALLOC                                    *   FILE 834
//*                                                                 *   FILE 834
//*           and the macro will allocate all the datasets, with    *   FILE 834
//*           their proper attributes, on the receiving system.     *   FILE 834
//*                                                                 *   FILE 834
//*           Sample "before" and "after" dataset lists are         *   FILE 834
//*           provided in XMIT format as member SAMPLES.  After     *   FILE 834
//*                TSO RECEIVE INDS(this.pds(SAMPLES))              *   FILE 834
//*           you will get a pds with LRECL=133 that shows the      *   FILE 834
//*           "before REQ" and "after REQ" dataset lists.           *   FILE 834
//*                                                                 *   FILE 834
//*           email: Alexander.I.Vasilenko@boeing.com               *   FILE 834
//*                  Ali_vas@mail.ru                                *   FILE 834
//*                                                                 *   FILE 834
//*           --------------------------------------------------    *   FILE 834
//*                                                                 *   FILE 834
//*    >>>    This file now contains some other edit macros from    *   FILE 834
//*    >>>    Alexander Vasilenko.  Alex has made a new shipment    *   FILE 834
//*    >>>    of his MIGRATE macro, but I have preserved the old    *   FILE 834
//*    >>>    version of this file in IEBUPDTE SYSIN format (or     *   FILE 834
//*    >>>    actually PDSLOAD format) as member OLD834, just in    *   FILE 834
//*    >>>    case somebody would like to refer to Alex's older     *   FILE 834
//*    >>>    work.                                                 *   FILE 834
//*                                                                 *   FILE 834
//*    This PDS now contains some more REXX procedures.             *   FILE 834
//*                                                                 *   FILE 834
//*    Needed for MIGRATE:                                          *   FILE 834
//*                                                                 *   FILE 834
//*    1. DELDUP   - macro to delete duplicate lines.               *   FILE 834
//*    2. EXTRDISP - macro to extract DSN and DISP from             *   FILE 834
//*                  SRCHFOR file.                                  *   FILE 834
//*    3. GDGALLOC - requests and defines GDG.                      *   FILE 834
//*    4. MIGRATE  - requests and allocated PDS/PDSE and PS.        *   FILE 834
//*    5. QDS      - determines DS type.                            *   FILE 834
//*    6. LIST#UG  - desribes how to prepare DSN list from          *   FILE 834
//*                  JCL.                                           *   FILE 834
//*    7. MIRG#UG  - describes how to use migrate macros.           *   FILE 834
//*                                                                 *   FILE 834
//*    Some other macros and commands.                              *   FILE 834
//*                                                                 *   FILE 834
//*       COMMENT  - this EDIT macro allows comment and             *   FILE 834
//*                  uncomment.                                     *   FILE 834
//*       MARK     - convenient EDIT macro to mark edited           *   FILE 834
//*                  lines with certain label in 73-80              *   FILE 834
//*                  positions.                                     *   FILE 834
//*       MARKC    - similar as MARK but performs marking           *   FILE 834
//*                  base on COMPARE result.                        *   FILE 834
//*       SETREPL  - CLIST procedure to change ZMCREP ISPF          *   FILE 834
//*                  variable, responsible to replacement of        *   FILE 834
//*                  member in COPY/MOVE operation. You may         *   FILE 834
//*                  perform it from ISRUDSM panel.                 *   FILE 834
//*       VIEWPOOL - simple REXX to view variable pools.            *   FILE 834
//*       WHATCHA  - EDIT macro to see which lines were             *   FILE 834
//*                  changed and how.                               *   FILE 834
//*                                                                 *   FILE 834
```
