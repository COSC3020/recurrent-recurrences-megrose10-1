# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

1. T(n) = T(n/13) + 5
T(n/13) = T(n/13/13) + 5
T(n) = T(n/13^2) + 5 +5
T(n/13^2)  = T(n/13/13^2) + 5
T(n) = T(n/13^3) +5 +5+5
T(n) = T(n/13^i) + 5i, i = log(base 13)n
T(n) = T(1) + 5log(base13)n ∈ Θ(logn)

2. T(n) = 13T(n/13) + 5
T(n/13) = 13T(n/13/13) + 5
T(n) = 13^2T(n/13^2) + 5 +5
T(n/13^2)  = 13^2T(n/13/13^2) + 5
T(n) = 13^3T(n/13^3) +5 +5+5
T(n) = 13^iT(n/13^i) + 5i, i = log(base 13)n
T(n) = nT(1) + 5log(base13)n ∈ Θ(logn)

3. T(n) = 13T(n/13) + 2n 
T(n/13) = 13T(n/13/13) + 2n
T(n) = 13^2T(n/13^2) + 2n + 2n
T(n/13^2)  = 13^2T(n/13/13^2) + 4n
T(n) = 13^3T(n/13^3) + 4n + 2n
T(n) = 13^iT(n/13^i) + 2in, i = log(base 13)n
T(n) = nT(1) + 2log(base13)n * n ∈ Θ(nlogn)

I used the lecture slides that are within the sorting lecture as well as my repository on recurrence relation to review the material further.
I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
