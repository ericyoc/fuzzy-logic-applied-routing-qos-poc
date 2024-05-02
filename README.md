# Fuzzy Logic Enhanced Network Traffic Routing with QoS

This Python code demonstrates the application of fuzzy logic to enhance network traffic routing with Quality of Service (QoS) considerations. The code simulates a network scenario and compares the performance of conventional routing (no fuzzy logic applied) with fuzzy logic enhanced routing.

## Features

- Generation of a routing dataset with configurable number of devices and congestion probability
- Implementation of fuzzy logic rules for intelligent routing decisions based on network conditions
- Simulation of routing before and after optimization using conventional and fuzzy logic enhanced approaches
- Calculation of performance metrics such as total throughput, low priority load, high priority load, elapsed time, and congestion percentage
- Generation of pretty tables to present the simulation results for each trial and average values
- Explanation of why fuzzy logic applied with QoS outperforms the scenario without fuzzy logic

## Fuzzy Logic Rules

The code defines a set of fuzzy logic rules based on input terms (number of packets, change in number of packets, and clear rate) and output terms (routing actions). These rules are generated dynamically based on the input and output term combinations.

Example rule:
```python
if 'Very_High' in [n_term, clr_term] or 'Positive_Big' in dn_term:
    action = 1  # Strong_Discard
```

## Simulation Results

The code simulates network traffic routing for a specified number of trials and generates tables to present the results. The tables compare the performance of conventional routing (no fuzzy logic applied) with fuzzy logic enhanced routing.

![](https://github.com/ericyoc/fuzzy-logic-applied-routing-qos/blob/main/fuzzy_logic_applied_with_and_without_qos.jpg)

## Explanation

Based on the findings within the tables, fuzzy logic applied with QoS outperforms the scenario without fuzzy logic for the following reasons:

1. **Total Throughput**: Fuzzy logic applied with QoS achieves higher average total throughput (in packets) and total throughput percentage compared to no fuzzy logic applied with QoS. This indicates that fuzzy logic enables more efficient routing and allows a higher volume of packets to be processed.

2. **Elapsed Time**: The average elapsed time is significantly lower with fuzzy logic applied, suggesting that fuzzy logic optimizes the routing process, resulting in faster packet delivery and reduced latency.

3. **Congestion**: Fuzzy logic effectively manages congestion by making intelligent routing decisions based on network conditions, resulting in a lower average congestion percentage compared to the scenario without fuzzy logic.

4. **Low Priority and High Priority Load**: The average low priority and high priority load (in packets) remain the same in both scenarios, demonstrating that fuzzy logic maintains fairness in packet distribution while improving overall performance.

In summary, fuzzy logic applied with QoS outperforms the scenario without fuzzy logic by increasing throughput, reducing elapsed time, minimizing congestion, and maintaining fair packet distribution. The fuzzy logic rules enable intelligent and adaptive routing decisions based on real-time network conditions, resulting in superior performance compared to the conventional approach.

## Acknowledgments

This code is inspired by the concepts of fuzzy logic and its application in network traffic routing with QoS considerations. The implementation is based on the principles and techniques discussed in various research papers and literature on fuzzy logic and network optimization.

## License

This code is released under the [MIT License](LICENSE).
