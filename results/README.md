# Results

Tables from the paper are reproduced in the `tables.ipynb` notebook.

## `as-hegemony`

Analysis results based on AS Hegemony data.

- `downstream-dependency-ip-version.csv`: Base of Table 2. Downstream dependency
by IP version and IP capability.
- `dual-stack-downstreams-upstream-relationships.csv`: Base of Table 4.
Relationship of upstream sets for dual-stack downstreams.

## `as-pairs`

### `as-hegemony`

AS pairs based on AS Hegemony data.

- `single-upstream-pairs`: AS pairs that have a hegemony score of 1 (100%
dependency) during all three snapshots (July 1, 8, and 15, 2024) *see Section
3.1*.
  - **Warning: Large files (~500MB each)**
  - IPv4
    - [ihr_hegemony_ipv4_local_2024-07-01.csv.lz4](https://archive.ihr.live/ihr/hegemony/ipv4/local/2024/07/01/ihr_hegemony_ipv4_local_2024-07-01.csv.lz4)
    - [ihr_hegemony_ipv4_local_2024-07-08.csv.lz4](https://archive.ihr.live/ihr/hegemony/ipv4/local/2024/07/08/ihr_hegemony_ipv4_local_2024-07-08.csv.lz4)
    - [ihr_hegemony_ipv4_local_2024-07-15.csv.lz4](https://archive.ihr.live/ihr/hegemony/ipv4/local/2024/07/15/ihr_hegemony_ipv4_local_2024-07-15.csv.lz4)
  - IPv6
    - [ihr_hegemony_ipv6_local_2024-07-01.csv.lz4](https://archive.ihr.live/ihr/hegemony/ipv6/local/2024/07/01/ihr_hegemony_ipv6_local_2024-07-01.csv.lz4)
    - [ihr_hegemony_ipv6_local_2024-07-08.csv.lz4](https://archive.ihr.live/ihr/hegemony/ipv6/local/2024/07/08/ihr_hegemony_ipv6_local_2024-07-08.csv.lz4)
    - [ihr_hegemony_ipv6_local_2024-07-15.csv.lz4](https://archive.ihr.live/ihr/hegemony/ipv6/local/2024/07/15/ihr_hegemony_ipv6_local_2024-07-15.csv.lz4)
- `direct-pairs`: Subset of pairs that has direct BGP adjacency.
- `indirect-pair`: Subset of pairs with no direct BGP adjacency.

#### `customer cone`

Indirect pairs categorized by their customer cone relationship (based on AS
relationships from July 1, 2024;
[20240701.ppdc-ases.txt.bz2](https://publicdata.caida.org/datasets/as-relationships/serial-1/20240701.ppdc-ases.txt.bz2))

### `as-relationship`

AS pairs based on CAIDA's [AS
relationships](https://www.caida.org/catalog/datasets/as-relationships/) data
for which the customer only has a single provider AS.

- IPv4: [20240701.as-rel.txt.bz2](https://publicdata.caida.org/datasets/as-relationships/serial-1/20240701.as-rel.txt.bz2)
- IPv6: [20240701.as-rel.v6-stable.txt.bz2](https://publicdata.caida.org/datasets/as-relationships/serial-1/20240701.as-rel.v6-stable.txt.bz2)

### `measured`

AS pairs confirmed with active measurements.

- `backup-upstream`: Downstream has a hidden backup upstream.
- `default-route`: Both up- and downstream have a default route and thus result is inconclusive.
- `single-upstream`: Downstream only has a single upstream.

More results will follow.
