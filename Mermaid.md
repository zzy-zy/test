
flowchart TD
    st[Start] --> in1[Input T]
    in1 --> while{T > 0}
    while --> in2[Input x]
    in2 --> calc_a_b[Calculate a and b]
    calc_a_b --> condition1{Is x == 1?}
    condition1 -->|Yes| store_m1[Store m = 3 in x_arr]
    condition1 -->|No| condition2{Is b == 0?}
    condition2 -->|Yes| store_m2[Store m = (a + 1) * 4 + 1 in x_arr]
    condition2 -->|No| condition3{Is b == 1?}
    condition3 -->|Yes| store_m3[Store m = (a + 1) * 4 + 3 in x_arr]
    condition3 -->|No| store_m4[Store m = (a + 1) * 4 + 4 in x_arr]
    store_m1 --> while
    store_m2 --> while
    store_m3 --> while
    store_m4 --> while
    while --> out1[Output x_arr]
    out1 --> e[End]
