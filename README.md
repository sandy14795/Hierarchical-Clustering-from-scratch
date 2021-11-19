# Hierarchical-Clustering-from-scratch

Tie Breaking Rule for selecting next clusters -

Generally, when choosing the next two clusters to merge, we pick the pair having the smallest euclidean distance. In the case that multiple pairs have the same distance, we need additional criteria to pick between them. We do this with a tie-breaking rule on indices as follows:  

Suppose (𝑖1,𝑗1),...,(𝑖ℎ,𝑗ℎ)
are pairs of cluster indices with equal distance, i.e., 𝑑(𝑖1,𝑗1)=...=𝑑(𝑖ℎ,𝑗ℎ), and assume that 𝑖𝑡<𝑗𝑡 for all t (so each tuple is sorted). The first tie-breaking strategy, is to pick the pair with smallest index. Since each pair is sorted, this is the same as choosing the pair with the smallest first index, 𝑖. Now, if there are multiple pairs having first index 𝑖, we need to further distinguish between them. Say these pairs are (𝑖,𝑡1),(𝑖,𝑡2),... and so on. To tie-break between them, we will pick the pair with the smallest second index, i.e., the smallest 𝑡 value in these pairs. Note after the second phase of tie-breaking there will be only one pair remaining, a third phase isn't needed.
