- An ARM emulator that executes native ARM assembly code on run-time
- Performance measurements comparing native C and ARM execution time versus emulated execution time.
- Cache Emulation for Direct Mapped, Fully Associative and 4 way Set-Associative with size 8, 32, 128 & 1024 byte size
- Dynamic Analysis of the ARM instructions/ cache used

> Source code hidden for `confidentiality` reasons. Please contact at `ayusharora009@gmail.com` for view request

## Project Objective:
Create a C program that can execute ARM machine code by emulating the register state of an ARM CPU and emulating the execution of ARM instructions.

## Executing the result program

```
==========================================================================================================
quadratic - Case 1

quadratic_c(2, 3, 4, 5) =  25           Time taken: 9 (microseconds) | 0.01 (seconds)
quadratic_s(2, 3, 4, 5) =  25           Time taken: 7 (microseconds) | 0.01 (seconds)
quadratic_e(2, 3, 4, 5) =  25           Time taken: 1375 (microseconds) | 1.38 (seconds)

\* ------------------------ Instructions (Total : 9) ------------------------ *\ 

DP : 8 (88.89 %)| Mem : 0 (0.00 %)| Branch : 1 (11.11 %)        [ Taken : 1 (100.00 %)| NOT Taken : 0 (0.00 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Direct Mapped : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9

**********************************************************************************************************
quadratic - Case 2

quadratic_c(2, 1, -4, 4) =  0           Time taken: 8 (microseconds) | 0.01 (seconds)
quadratic_s(2, 1, -4, 4) =  0           Time taken: 7 (microseconds) | 0.01 (seconds)
quadratic_e(2, 1, -4, 4) =  0           Time taken: 1377 (microseconds) | 1.38 (seconds)

\* ------------------------ Instructions (Total : 9) ------------------------ *\ 

DP : 8 (88.89 %)| Mem : 0 (0.00 %)| Branch : 1 (11.11 %)        [ Taken : 1 (100.00 %)| NOT Taken : 0 (0.00 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Direct Mapped : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9

**********************************************************************************************************
quadratic - Case 3

quadratic_c(4, 1, -4, 4) =  4           Time taken: 8 (microseconds) | 0.01 (seconds)
quadratic_s(4, 1, -4, 4) =  4           Time taken: 5 (microseconds) | 0.01 (seconds)
quadratic_e(4, 1, -4, 4) =  4           Time taken: 1366 (microseconds) | 1.37 (seconds)

\* ------------------------ Instructions (Total : 9) ------------------------ *\ 

DP : 8 (88.89 %)| Mem : 0 (0.00 %)| Branch : 1 (11.11 %)        [ Taken : 1 (100.00 %)| NOT Taken : 0 (0.00 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Direct Mapped : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9

**********************************************************************************************************
quadratic - Case 4

quadratic_c(1, 1, 0, 4) =  5            Time taken: 7 (microseconds) | 0.01 (seconds)
quadratic_s(1, 1, 0, 4) =  5            Time taken: 6 (microseconds) | 0.01 (seconds)
quadratic_e(1, 1, 0, 4) =  5            Time taken: 1415 (microseconds) | 1.42 (seconds)

\* ------------------------ Instructions (Total : 9) ------------------------ *\ 

DP : 8 (88.89 %)| Mem : 0 (0.00 %)| Branch : 1 (11.11 %)        [ Taken : 1 (100.00 %)| NOT Taken : 0 (0.00 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Direct Mapped : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Fully Assoc.  : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:9 (100.00 %), R:9            | (Size 32) H:0 (0.00 %), M:9 (100.00 %), R:9
• Set Assoc.    : (Size 128) H:0 (0.00 %), M:9 (100.00 %), R:9          | (Size 1024) H:0 (0.00 %), M:9 (100.00 %), R:9

==========================================================================================================
sum_array - Case 1

sum_array_c({1,2,3 .... 998,999,1000}, 1000) = 500500           Time taken: 49 (microseconds) | 0.05 (seconds)
sum_array_s({1,2,3 .... 998,999,1000}, 1000) = 500500           Time taken: 25 (microseconds) | 0.03 (seconds)
sum_array_e({1,2,3 .... 998,999,1000}, 1000) = 500500           Time taken: 575485 (microseconds) | 575.49 (seconds)

\* ------------------------ Instructions (Total : 7006) ------------------------ *\ 

DP : 4004 (57.15 %)| Mem : 1000 (14.27 %)| Branch : 2002 (28.58 %)      [ Taken : 1002 (50.05 %)| NOT Taken : 1000 (49.95 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Direct Mapped : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006

**********************************************************************************************************
sum_array - Case 2

sum_array_c({-500,-499,-498 .... 497,498,499}, 1000) = -500             Time taken: 51 (microseconds) | 0.05 (seconds)
sum_array_s({-500,-499,-498 .... 497,498,499}, 1000) = -500             Time taken: 20 (microseconds) | 0.02 (seconds)
sum_array_e({-500,-499,-498 .... 497,498,499}, 1000) = -500             Time taken: 574692 (microseconds) | 574.69 (seconds)

\* ------------------------ Instructions (Total : 7006) ------------------------ *\ 

DP : 4004 (57.15 %)| Mem : 1000 (14.27 %)| Branch : 2002 (28.58 %)      [ Taken : 1002 (50.05 %)| NOT Taken : 1000 (49.95 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Direct Mapped : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006

**********************************************************************************************************
sum_array - Case 3

sum_array_c({0,2,4 .... 1994,1996,1998}, 1000) = 999000         Time taken: 51 (microseconds) | 0.05 (seconds)
sum_array_s({0,2,4 .... 1994,1996,1998}, 1000) = 999000         Time taken: 32 (microseconds) | 0.03 (seconds)
sum_array_e({0,2,4 .... 1994,1996,1998}, 1000) = 999000         Time taken: 575726 (microseconds) | 575.73 (seconds)

\* ------------------------ Instructions (Total : 7006) ------------------------ *\ 

DP : 4004 (57.15 %)| Mem : 1000 (14.27 %)| Branch : 2002 (28.58 %)      [ Taken : 1002 (50.05 %)| NOT Taken : 1000 (49.95 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Direct Mapped : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006

**********************************************************************************************************
sum_array - Case 4

sum_array_c({0,4,8 .... 3988,3992,3996}, 1000) = 1998000                Time taken: 49 (microseconds) | 0.05 (seconds)
sum_array_s({0,4,8 .... 3988,3992,3996}, 1000) = 1998000                Time taken: 30 (microseconds) | 0.03 (seconds)
sum_array_e({0,4,8 .... 3988,3992,3996}, 1000) = 1998000                Time taken: 575207 (microseconds) | 575.21 (seconds)

\* ------------------------ Instructions (Total : 7006) ------------------------ *\ 

DP : 4004 (57.15 %)| Mem : 1000 (14.27 %)| Branch : 2002 (28.58 %)      [ Taken : 1002 (50.05 %)| NOT Taken : 1000 (49.95 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Direct Mapped : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Fully Assoc.  : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 8) H:6995 (99.84 %), M:11 (0.16 %), R:7006              | (Size 32) H:6995 (99.84 %), M:11 (0.16 %), R:7006
• Set Assoc.    : (Size 128) H:6995 (99.84 %), M:11 (0.16 %), R:7006            | (Size 1024) H:6995 (99.84 %), M:11 (0.16 %), R:7006

==========================================================================================================
find_max - Case 1

find_max_c({0,4,8 .... 3988,3992,3996}, 1000) = 3996            Time taken: 65 (microseconds) | 0.07 (seconds)
find_max_s({0,4,8 .... 3988,3992,3996}, 1000) = 3996            Time taken: 29 (microseconds) | 0.03 (seconds)
find_max_e({0,4,8 .... 3988,3992,3996}, 1000) = 3996            Time taken: 748182 (microseconds) | 748.18 (seconds)

\* ------------------------ Instructions (Total : 9005) ------------------------ *\ 

DP : 5002 (55.55 %)| Mem : 1001 (11.12 %)| Branch : 3002 (33.34 %)      [ Taken : 2001 (66.66 %)| NOT Taken : 1001 (33.34 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:1003 (11.14 %), M:8002 (88.86 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Direct Mapped : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 8) H:5 (0.06 %), M:9000 (99.94 %), R:9005               | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 8) H:3998 (44.40 %), M:5007 (55.60 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005

**********************************************************************************************************
find_max - Case 2

find_max_c({-500,-499,-498 .... 497,498,499}, 1000) = 499               Time taken: 63 (microseconds) | 0.06 (seconds)
find_max_s({-500,-499,-498 .... 497,498,499}, 1000) = 499               Time taken: 25 (microseconds) | 0.03 (seconds)
find_max_e({-500,-499,-498 .... 497,498,499}, 1000) = 499               Time taken: 744625 (microseconds) | 744.62 (seconds)

\* ------------------------ Instructions (Total : 9005) ------------------------ *\ 

DP : 5002 (55.55 %)| Mem : 1001 (11.12 %)| Branch : 3002 (33.34 %)      [ Taken : 2001 (66.66 %)| NOT Taken : 1001 (33.34 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:1003 (11.14 %), M:8002 (88.86 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Direct Mapped : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 8) H:5 (0.06 %), M:9000 (99.94 %), R:9005               | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 8) H:3998 (44.40 %), M:5007 (55.60 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005

**********************************************************************************************************
find_max - Case 3

find_max_c({0,2,4 .... 1994,1996,1998}, 1000) = 1998            Time taken: 65 (microseconds) | 0.07 (seconds)
find_max_s({0,2,4 .... 1994,1996,1998}, 1000) = 1998            Time taken: 29 (microseconds) | 0.03 (seconds)
find_max_e({0,2,4 .... 1994,1996,1998}, 1000) = 1998            Time taken: 746451 (microseconds) | 746.45 (seconds)

\* ------------------------ Instructions (Total : 9005) ------------------------ *\ 

DP : 5002 (55.55 %)| Mem : 1001 (11.12 %)| Branch : 3002 (33.34 %)      [ Taken : 2001 (66.66 %)| NOT Taken : 1001 (33.34 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:1003 (11.14 %), M:8002 (88.86 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Direct Mapped : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 8) H:5 (0.06 %), M:9000 (99.94 %), R:9005               | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 8) H:3998 (44.40 %), M:5007 (55.60 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005

**********************************************************************************************************
find_max - Case 4

find_max_c({0,4,8 .... 3988,3992,3996}, 1000) = 3996            Time taken: 64 (microseconds) | 0.06 (seconds)
find_max_s({0,4,8 .... 3988,3992,3996}, 1000) = 3996            Time taken: 22 (microseconds) | 0.02 (seconds)
find_max_e({0,4,8 .... 3988,3992,3996}, 1000) = 3996            Time taken: 746890 (microseconds) | 746.89 (seconds)

\* ------------------------ Instructions (Total : 9005) ------------------------ *\ 

DP : 5002 (55.55 %)| Mem : 1001 (11.12 %)| Branch : 3002 (33.34 %)      [ Taken : 2001 (66.66 %)| NOT Taken : 1001 (33.34 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:1003 (11.14 %), M:8002 (88.86 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Direct Mapped : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 8) H:5 (0.06 %), M:9000 (99.94 %), R:9005               | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Fully Assoc.  : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 8) H:3998 (44.40 %), M:5007 (55.60 %), R:9005           | (Size 32) H:8989 (99.82 %), M:16 (0.18 %), R:9005
• Set Assoc.    : (Size 128) H:8989 (99.82 %), M:16 (0.18 %), R:9005            | (Size 1024) H:8989 (99.82 %), M:16 (0.18 %), R:9005

==========================================================================================================
fib_iter - Case 1

fib_iter_c(2) =                                 1               Time taken: 19 (microseconds) | 0.02 (seconds)
fib_iter_s(2) =                                 1               Time taken: 14 (microseconds) | 0.01 (seconds)
armemu(fib_iter_e(len, 2, 0, 0)) =              1               Time taken: 2281 (microseconds) | 2.28 (seconds)

\* ------------------------ Instructions (Total : 17) ------------------------ *\ 

DP : 12 (70.59 %)| Mem : 0 (0.00 %)| Branch : 5 (29.41 %)       [ Taken : 3 (60.00 %)| NOT Taken : 2 (40.00 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:2 (11.76 %), M:15 (88.24 %), R:17          | (Size 32) H:2 (11.76 %), M:15 (88.24 %), R:17
• Direct Mapped : (Size 128) H:2 (11.76 %), M:15 (88.24 %), R:17                | (Size 1024) H:2 (11.76 %), M:15 (88.24 %), R:17
• Fully Assoc.  : (Size 8) H:2 (11.76 %), M:15 (88.24 %), R:17          | (Size 32) H:2 (11.76 %), M:15 (88.24 %), R:17
• Fully Assoc.  : (Size 128) H:2 (11.76 %), M:15 (88.24 %), R:17                | (Size 1024) H:2 (11.76 %), M:15 (88.24 %), R:17
• Set Assoc.    : (Size 8) H:2 (11.76 %), M:15 (88.24 %), R:17          | (Size 32) H:2 (11.76 %), M:15 (88.24 %), R:17
• Set Assoc.    : (Size 128) H:2 (11.76 %), M:15 (88.24 %), R:17                | (Size 1024) H:2 (11.76 %), M:15 (88.24 %), R:17

**********************************************************************************************************
fib_iter - Case 2

fib_iter_c(10) =                                55              Time taken: 16 (microseconds) | 0.02 (seconds)
fib_iter_s(10) =                                55              Time taken: 20 (microseconds) | 0.02 (seconds)
armemu(fib_iter_e(len, 10, 0, 0)) =             55              Time taken: 7253 (microseconds) | 7.25 (seconds)

\* ------------------------ Instructions (Total : 73) ------------------------ *\ 

DP : 52 (71.23 %)| Mem : 0 (0.00 %)| Branch : 21 (28.77 %)      [ Taken : 11 (52.38 %)| NOT Taken : 10 (47.62 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:58 (79.45 %), M:15 (20.55 %), R:73         | (Size 32) H:58 (79.45 %), M:15 (20.55 %), R:73
• Direct Mapped : (Size 128) H:58 (79.45 %), M:15 (20.55 %), R:73               | (Size 1024) H:58 (79.45 %), M:15 (20.55 %), R:73
• Fully Assoc.  : (Size 8) H:58 (79.45 %), M:15 (20.55 %), R:73         | (Size 32) H:58 (79.45 %), M:15 (20.55 %), R:73
• Fully Assoc.  : (Size 128) H:58 (79.45 %), M:15 (20.55 %), R:73               | (Size 1024) H:58 (79.45 %), M:15 (20.55 %), R:73
• Set Assoc.    : (Size 8) H:58 (79.45 %), M:15 (20.55 %), R:73         | (Size 32) H:58 (79.45 %), M:15 (20.55 %), R:73
• Set Assoc.    : (Size 128) H:58 (79.45 %), M:15 (20.55 %), R:73               | (Size 1024) H:58 (79.45 %), M:15 (20.55 %), R:73

**********************************************************************************************************
fib_iter - Case 3

fib_iter_c(19) =                                4181            Time taken: 17 (microseconds) | 0.02 (seconds)
fib_iter_s(19) =                                4181            Time taken: 21 (microseconds) | 0.02 (seconds)
armemu(fib_iter_e(len, 19, 0, 0)) =             4181            Time taken: 12577 (microseconds) | 12.58 (seconds)

\* ------------------------ Instructions (Total : 136) ------------------------ *\ 

DP : 97 (71.32 %)| Mem : 0 (0.00 %)| Branch : 39 (28.68 %)      [ Taken : 20 (51.28 %)| NOT Taken : 19 (48.72 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:121 (88.97 %), M:15 (11.03 %), R:136               | (Size 32) H:121 (88.97 %), M:15 (11.03 %), R:136
• Direct Mapped : (Size 128) H:121 (88.97 %), M:15 (11.03 %), R:136             | (Size 1024) H:121 (88.97 %), M:15 (11.03 %), R:136
• Fully Assoc.  : (Size 8) H:121 (88.97 %), M:15 (11.03 %), R:136               | (Size 32) H:121 (88.97 %), M:15 (11.03 %), R:136
• Fully Assoc.  : (Size 128) H:121 (88.97 %), M:15 (11.03 %), R:136             | (Size 1024) H:121 (88.97 %), M:15 (11.03 %), R:136
• Set Assoc.    : (Size 8) H:121 (88.97 %), M:15 (11.03 %), R:136               | (Size 32) H:121 (88.97 %), M:15 (11.03 %), R:136
• Set Assoc.    : (Size 128) H:121 (88.97 %), M:15 (11.03 %), R:136             | (Size 1024) H:121 (88.97 %), M:15 (11.03 %), R:136

**********************************************************************************************************
==========================================================================================================
fib_rec - Case 1

fib_rec_c(2) =                          1               Time taken: 21 (microseconds) | 0.02 (seconds)
fib_rec_s(2) =                          1               Time taken: 18 (microseconds) | 0.02 (seconds)
armemu(fib_rec_e(len, 2, 0, 0)) =               1               Time taken: 4729 (microseconds) | 4.73 (seconds)

\* ------------------------ Instructions (Total : 36) ------------------------ *\ 

DP : 17 (47.22 %)| Mem : 11 (30.56 %)| Branch : 8 (22.22 %)     [ Taken : 7 (87.50 %)| NOT Taken : 1 (12.50 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:6 (16.67 %), M:30 (83.33 %), R:36          | (Size 32) H:12 (33.33 %), M:24 (66.67 %), R:36
• Direct Mapped : (Size 128) H:12 (33.33 %), M:24 (66.67 %), R:36               | (Size 1024) H:12 (33.33 %), M:24 (66.67 %), R:36
• Fully Assoc.  : (Size 8) H:2 (5.56 %), M:34 (94.44 %), R:36           | (Size 32) H:12 (33.33 %), M:24 (66.67 %), R:36
• Fully Assoc.  : (Size 128) H:12 (33.33 %), M:24 (66.67 %), R:36               | (Size 1024) H:12 (33.33 %), M:24 (66.67 %), R:36
• Set Assoc.    : (Size 8) H:2 (5.56 %), M:34 (94.44 %), R:36           | (Size 32) H:12 (33.33 %), M:24 (66.67 %), R:36
• Set Assoc.    : (Size 128) H:12 (33.33 %), M:24 (66.67 %), R:36               | (Size 1024) H:12 (33.33 %), M:24 (66.67 %), R:36

**********************************************************************************************************
fib_rec - Case 2

fib_rec_c(10) =                                 55              Time taken: 23 (microseconds) | 0.02 (seconds)
fib_rec_s(10) =                                 55              Time taken: 17 (microseconds) | 0.02 (seconds)
armemu(fib_rec_e(len, 10, 0, 0)) =              55              Time taken: 222444 (microseconds) | 222.44 (seconds)

\* ------------------------ Instructions (Total : 2646) ------------------------ *\ 

DP : 1148 (43.39 %)| Mem : 968 (36.58 %)| Branch : 530 (20.03 %)        [ Taken : 442 (83.40 %)| NOT Taken : 88 (16.60 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:780 (29.48 %), M:1866 (70.52 %), R:2646            | (Size 32) H:2622 (99.09 %), M:24 (0.91 %), R:2646
• Direct Mapped : (Size 128) H:2622 (99.09 %), M:24 (0.91 %), R:2646            | (Size 1024) H:2622 (99.09 %), M:24 (0.91 %), R:2646
• Fully Assoc.  : (Size 8) H:374 (14.13 %), M:2272 (85.87 %), R:2646            | (Size 32) H:2622 (99.09 %), M:24 (0.91 %), R:2646
• Fully Assoc.  : (Size 128) H:2622 (99.09 %), M:24 (0.91 %), R:2646            | (Size 1024) H:2622 (99.09 %), M:24 (0.91 %), R:2646
• Set Assoc.    : (Size 8) H:374 (14.13 %), M:2272 (85.87 %), R:2646            | (Size 32) H:2622 (99.09 %), M:24 (0.91 %), R:2646
• Set Assoc.    : (Size 128) H:2622 (99.09 %), M:24 (0.91 %), R:2646            | (Size 1024) H:2622 (99.09 %), M:24 (0.91 %), R:2646

**********************************************************************************************************
fib_rec - Case 3

fib_rec_c(19) =                                 4181            Time taken: 628 (microseconds) | 0.63 (seconds)
fib_rec_s(19) =                                 4181            Time taken: 458 (microseconds) | 0.46 (seconds)
armemu(fib_rec_e(len, 19, 0, 0)) =              4181            Time taken: 4007052 (microseconds) | 4007.05 (seconds)

\* ------------------------ Instructions (Total : 202926) ------------------------ *\ 

DP : 87936 (43.33 %)| Mem : 74404 (36.67 %)| Branch : 40586 (20.00 %)   [ Taken : 33822 (83.33 %)| NOT Taken : 6764 (16.67 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:60262 (29.70 %), M:142664 (70.30 %), R:202926              | (Size 32) H:202902 (99.99 %), M:24 (0.01 %), R:202926
• Direct Mapped : (Size 128) H:202902 (99.99 %), M:24 (0.01 %), R:202926                | (Size 1024) H:202902 (99.99 %), M:24 (0.01 %), R:202926
• Fully Assoc.  : (Size 8) H:29026 (14.30 %), M:173900 (85.70 %), R:202926              | (Size 32) H:202902 (99.99 %), M:24 (0.01 %), R:202926
• Fully Assoc.  : (Size 128) H:202902 (99.99 %), M:24 (0.01 %), R:202926                | (Size 1024) H:202902 (99.99 %), M:24 (0.01 %), R:202926
• Set Assoc.    : (Size 8) H:29026 (14.30 %), M:173900 (85.70 %), R:202926              | (Size 32) H:202902 (99.99 %), M:24 (0.01 %), R:202926
• Set Assoc.    : (Size 128) H:202902 (99.99 %), M:24 (0.01 %), R:202926                | (Size 1024) H:202902 (99.99 %), M:24 (0.01 %), R:202926

**********************************************************************************************************
==========================================================================================================
strlen - Case 1

strlen_c("This is a test string with length 36")                = 36            Time taken: 12 (microseconds) | 0.01 (seconds)
strlen_s("This is a test string with length 36")                = 36            Time taken: 8 (microseconds) | 0.01 (seconds)
strlen_e("This is a test string with length 36", 0, 0, 0)       = 36            Time taken: 18937 (microseconds) | 18.94 (seconds)

\* ------------------------ Instructions (Total : 222) ------------------------ *\ 

DP : 111 (50.00 %)| Mem : 37 (16.67 %)| Branch : 74 (33.33 %)   [ Taken : 38 (51.35 %)| NOT Taken : 36 (48.65 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:213 (95.95 %), M:9 (4.05 %), R:222         | (Size 32) H:213 (95.95 %), M:9 (4.05 %), R:222
• Direct Mapped : (Size 128) H:213 (95.95 %), M:9 (4.05 %), R:222               | (Size 1024) H:213 (95.95 %), M:9 (4.05 %), R:222
• Fully Assoc.  : (Size 8) H:213 (95.95 %), M:9 (4.05 %), R:222         | (Size 32) H:213 (95.95 %), M:9 (4.05 %), R:222
• Fully Assoc.  : (Size 128) H:213 (95.95 %), M:9 (4.05 %), R:222               | (Size 1024) H:213 (95.95 %), M:9 (4.05 %), R:222
• Set Assoc.    : (Size 8) H:213 (95.95 %), M:9 (4.05 %), R:222         | (Size 32) H:213 (95.95 %), M:9 (4.05 %), R:222
• Set Assoc.    : (Size 128) H:213 (95.95 %), M:9 (4.05 %), R:222               | (Size 1024) H:213 (95.95 %), M:9 (4.05 %), R:222

**********************************************************************************************************
strlen - Case 2

strlen_c("the quick fox jumps over lazy dog")           = 33            Time taken: 9 (microseconds) | 0.01 (seconds)
strlen_s("the quick fox jumps over lazy dog")           = 33            Time taken: 7 (microseconds) | 0.01 (seconds)
strlen_e("the quick fox jumps over lazy dog", 0, 0, 0)  = 33            Time taken: 17535 (microseconds) | 17.54 (seconds)

\* ------------------------ Instructions (Total : 204) ------------------------ *\ 

DP : 102 (50.00 %)| Mem : 34 (16.67 %)| Branch : 68 (33.33 %)   [ Taken : 35 (51.47 %)| NOT Taken : 33 (48.53 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:195 (95.59 %), M:9 (4.41 %), R:204         | (Size 32) H:195 (95.59 %), M:9 (4.41 %), R:204
• Direct Mapped : (Size 128) H:195 (95.59 %), M:9 (4.41 %), R:204               | (Size 1024) H:195 (95.59 %), M:9 (4.41 %), R:204
• Fully Assoc.  : (Size 8) H:195 (95.59 %), M:9 (4.41 %), R:204         | (Size 32) H:195 (95.59 %), M:9 (4.41 %), R:204
• Fully Assoc.  : (Size 128) H:195 (95.59 %), M:9 (4.41 %), R:204               | (Size 1024) H:195 (95.59 %), M:9 (4.41 %), R:204
• Set Assoc.    : (Size 8) H:195 (95.59 %), M:9 (4.41 %), R:204         | (Size 32) H:195 (95.59 %), M:9 (4.41 %), R:204
• Set Assoc.    : (Size 128) H:195 (95.59 %), M:9 (4.41 %), R:204               | (Size 1024) H:195 (95.59 %), M:9 (4.41 %), R:204

**********************************************************************************************************
strlen - Case 3

strlen_c("She sells sea shells on the sea shore")               = 37            Time taken: 10 (microseconds) | 0.01 (seconds)
strlen_s("She sells sea shells on the sea shore")               = 37            Time taken: 7 (microseconds) | 0.01 (seconds)
strlen_e("She sells sea shells on the sea shore", 0, 0, 0)      = 37            Time taken: 19716 (microseconds) | 19.72 (seconds)

\* ------------------------ Instructions (Total : 228) ------------------------ *\ 

DP : 114 (50.00 %)| Mem : 38 (16.67 %)| Branch : 76 (33.33 %)   [ Taken : 39 (51.32 %)| NOT Taken : 37 (48.68 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:219 (96.05 %), M:9 (3.95 %), R:228         | (Size 32) H:219 (96.05 %), M:9 (3.95 %), R:228
• Direct Mapped : (Size 128) H:219 (96.05 %), M:9 (3.95 %), R:228               | (Size 1024) H:219 (96.05 %), M:9 (3.95 %), R:228
• Fully Assoc.  : (Size 8) H:219 (96.05 %), M:9 (3.95 %), R:228         | (Size 32) H:219 (96.05 %), M:9 (3.95 %), R:228
• Fully Assoc.  : (Size 128) H:219 (96.05 %), M:9 (3.95 %), R:228               | (Size 1024) H:219 (96.05 %), M:9 (3.95 %), R:228
• Set Assoc.    : (Size 8) H:219 (96.05 %), M:9 (3.95 %), R:228         | (Size 32) H:219 (96.05 %), M:9 (3.95 %), R:228
• Set Assoc.    : (Size 128) H:219 (96.05 %), M:9 (3.95 %), R:228               | (Size 1024) H:219 (96.05 %), M:9 (3.95 %), R:228

**********************************************************************************************************
strlen - Case 4

strlen_c("Betty bought some butter, but the butter was bitter, so Betty bought some more butter to make the bitter butter better")  = 118            Time taken: 11 (microseconds) | 0.01 (seconds)
strlen_s("Betty bought some butter, but the butter was bitter, so Betty bought some more butter to make the bitter butter better")  = 118            Time taken: 145 (microseconds) | 0.14 (seconds)
strlen_e("Betty bought some butter, but the butter was bitter, so Betty bought some more butter to make the bitter butter better", 0, 0, 0)  = 118           Time taken: 59302 (microseconds) | 59.30 (seconds)

\* ------------------------ Instructions (Total : 714) ------------------------ *\ 

DP : 357 (50.00 %)| Mem : 119 (16.67 %)| Branch : 238 (33.33 %) [ Taken : 120 (50.42 %)| NOT Taken : 118 (49.58 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:705 (98.74 %), M:9 (1.26 %), R:714         | (Size 32) H:705 (98.74 %), M:9 (1.26 %), R:714
• Direct Mapped : (Size 128) H:705 (98.74 %), M:9 (1.26 %), R:714               | (Size 1024) H:705 (98.74 %), M:9 (1.26 %), R:714
• Fully Assoc.  : (Size 8) H:705 (98.74 %), M:9 (1.26 %), R:714         | (Size 32) H:705 (98.74 %), M:9 (1.26 %), R:714
• Fully Assoc.  : (Size 128) H:705 (98.74 %), M:9 (1.26 %), R:714               | (Size 1024) H:705 (98.74 %), M:9 (1.26 %), R:714
• Set Assoc.    : (Size 8) H:705 (98.74 %), M:9 (1.26 %), R:714         | (Size 32) H:705 (98.74 %), M:9 (1.26 %), R:714
• Set Assoc.    : (Size 128) H:705 (98.74 %), M:9 (1.26 %), R:714               | (Size 1024) H:705 (98.74 %), M:9 (1.26 %), R:714

==========================================================================================================
sort - Case 1

sort_c({-10,-9,-8 .... -3,-2,-1}, 10) = {-1,-2,-3 .... -8,-9,-10}}                      Time taken: 14 (microseconds) | 0.01 (seconds)
sort_s({-10,-9,-8 .... -3,-2,-1}, 10) = {-1,-2,-3 .... -8,-9,-10}}                      Time taken: 9 (microseconds) | 0.01 (seconds)
sort_e({-10,-9,-8 .... -3,-2,-1}, 10) = {-1,-2,-3 .... -8,-9,-10}}                      Time taken: 101010 (microseconds) | 101.01 (seconds)

\* ------------------------ Instructions (Total : 1152) ------------------------ *\ 

DP : 510 (44.27 %)| Mem : 385 (33.42 %)| Branch : 257 (22.31 %) [ Taken : 157 (61.09 %)| NOT Taken : 100 (38.91 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:51 (4.43 %), M:1101 (95.57 %), R:1152              | (Size 32) H:840 (72.92 %), M:312 (27.08 %), R:1152
• Direct Mapped : (Size 128) H:1099 (95.40 %), M:53 (4.60 %), R:1152            | (Size 1024) H:1099 (95.40 %), M:53 (4.60 %), R:1152
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:1152 (100.00 %), R:1152              | (Size 32) H:718 (62.33 %), M:434 (37.67 %), R:1152
• Fully Assoc.  : (Size 128) H:1099 (95.40 %), M:53 (4.60 %), R:1152            | (Size 1024) H:1099 (95.40 %), M:53 (4.60 %), R:1152
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:1152 (100.00 %), R:1152              | (Size 32) H:768 (66.67 %), M:384 (33.33 %), R:1152
• Set Assoc.    : (Size 128) H:1099 (95.40 %), M:53 (4.60 %), R:1152            | (Size 1024) H:1099 (95.40 %), M:53 (4.60 %), R:1152

**********************************************************************************************************
sort - Case 2

sort_c({-7,-6,-5 .... 5,6,7}, 15) = {7,6,5 .... -5,-6,-7}}                      Time taken: 16 (microseconds) | 0.02 (seconds)
sort_s({-7,-6,-5 .... 5,6,7}, 15) = {7,6,5 .... -5,-6,-7}}                      Time taken: 11 (microseconds) | 0.01 (seconds)
sort_e({-7,-6,-5 .... 5,6,7}, 15) = {7,-7,-6 .... 2,1,0}}                       Time taken: 204668 (microseconds) | 204.67 (seconds)

\* ------------------------ Instructions (Total : 2367) ------------------------ *\ 

DP : 1109 (46.85 %)| Mem : 779 (32.91 %)| Branch : 479 (20.24 %)        [ Taken : 306 (63.88 %)| NOT Taken : 173 (36.12 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:47 (1.99 %), M:2320 (98.01 %), R:2367              | (Size 32) H:1861 (78.62 %), M:506 (21.38 %), R:2367
• Direct Mapped : (Size 128) H:2314 (97.76 %), M:53 (2.24 %), R:2367            | (Size 1024) H:2314 (97.76 %), M:53 (2.24 %), R:2367
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:2367 (100.00 %), R:2367              | (Size 32) H:1682 (71.06 %), M:685 (28.94 %), R:2367
• Fully Assoc.  : (Size 128) H:2314 (97.76 %), M:53 (2.24 %), R:2367            | (Size 1024) H:2314 (97.76 %), M:53 (2.24 %), R:2367
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:2367 (100.00 %), R:2367              | (Size 32) H:1727 (72.96 %), M:640 (27.04 %), R:2367
• Set Assoc.    : (Size 128) H:2314 (97.76 %), M:53 (2.24 %), R:2367            | (Size 1024) H:2314 (97.76 %), M:53 (2.24 %), R:2367

**********************************************************************************************************
sort - Case 3

sort_c({500,501,502 .... 507,508,509}, 10) = {509,508,507 .... 502,501,500}}                    Time taken: 13 (microseconds) | 0.01 (seconds)
sort_s({500,501,502 .... 507,508,509}, 10) = {509,508,507 .... 502,501,500}}                    Time taken: 9 (microseconds) | 0.01 (seconds)
sort_e({500,501,502 .... 507,508,509}, 10) = {509,508,507 .... 502,501,500}}                    Time taken: 101085 (microseconds) | 101.08 (seconds)

\* ------------------------ Instructions (Total : 1152) ------------------------ *\ 

DP : 510 (44.27 %)| Mem : 385 (33.42 %)| Branch : 257 (22.31 %) [ Taken : 157 (61.09 %)| NOT Taken : 100 (38.91 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:51 (4.43 %), M:1101 (95.57 %), R:1152              | (Size 32) H:840 (72.92 %), M:312 (27.08 %), R:1152
• Direct Mapped : (Size 128) H:1099 (95.40 %), M:53 (4.60 %), R:1152            | (Size 1024) H:1099 (95.40 %), M:53 (4.60 %), R:1152
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:1152 (100.00 %), R:1152              | (Size 32) H:718 (62.33 %), M:434 (37.67 %), R:1152
• Fully Assoc.  : (Size 128) H:1099 (95.40 %), M:53 (4.60 %), R:1152            | (Size 1024) H:1099 (95.40 %), M:53 (4.60 %), R:1152
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:1152 (100.00 %), R:1152              | (Size 32) H:768 (66.67 %), M:384 (33.33 %), R:1152
• Set Assoc.    : (Size 128) H:1099 (95.40 %), M:53 (4.60 %), R:1152            | (Size 1024) H:1099 (95.40 %), M:53 (4.60 %), R:1152

**********************************************************************************************************
sort - Case 4

sort_c({0,4,8 .... 3988,3992,3996}, 1000) = {3996,3992,3988 .... 8,4,0}}                        Time taken: 17572 (microseconds) | 17.57 (seconds)
sort_s({0,4,8 .... 3988,3992,3996}, 1000) = {3996,3992,3988 .... 8,4,0}}                        Time taken: 8040 (microseconds) | 8.04 (seconds)
sort_e({0,4,8 .... 3988,3992,3996}, 1000) = {3996,3992,3988 .... 8,4,0}}                        Time taken: 778300 (microseconds) | 778.30 (seconds)

\* ------------------------ Instructions (Total : 7787007) ------------------------ *\ 

DP : 3515505 (45.15 %)| Mem : 2513500 (32.28 %)| Branch : 1758002 (22.58 %)     [ Taken : 1005502 (57.20 %)| NOT Taken : 752500 (42.80 %)]

\* -------------- Cache REPORT (H = Hits, M = Misses, R = `Refs`) -------------- *\ 

• Direct Mapped : (Size 8) H:500001 (6.42 %), M:7287006 (93.58 %), R:7787007            | (Size 32) H:7757985 (99.63 %), M:29022 (0.37 %), R:7787007
• Direct Mapped : (Size 128) H:7786954 (100.00 %), M:53 (0.00 %), R:7787007             | (Size 1024) H:7786954 (100.00 %), M:53 (0.00 %), R:7787007
• Fully Assoc.  : (Size 8) H:0 (0.00 %), M:7787007 (100.00 %), R:7787007                | (Size 32) H:7744498 (99.45 %), M:42509 (0.55 %), R:7787007
• Fully Assoc.  : (Size 128) H:7786954 (100.00 %), M:53 (0.00 %), R:7787007             | (Size 1024) H:7786954 (100.00 %), M:53 (0.00 %), R:7787007
• Set Assoc.    : (Size 8) H:0 (0.00 %), M:7787007 (100.00 %), R:7787007                | (Size 32) H:7750488 (99.53 %), M:36519 (0.47 %), R:7787007
• Set Assoc.    : (Size 128) H:7786954 (100.00 %), M:53 (0.00 %), R:7787007             | (Size 1024) H:7786954 (100.00 %), M:53 (0.00 %), R:7787007
```
