# Results

Tables from the paper are reproduced in the `tables.ipynb` notebook.

Miscellaneous files:

- `hypergiant-asns.json`: The mapping of ASN to Hypergiants used in the paper.
Based on
[2021_04_hypergiants_asns.json](https://github.com/pgigis/sigcomm2021-hypergiants-offnets/blob/692b778c419e7fee4ce6aef529123ed64f0db347/datasets/hypergiants/2021_04_hypergiants_asns.json
) by [Gigis et al.](https://dl.acm.org/doi/10.1145/3452296.3472928) with
modifications (Removed Limelight, renamed Twitter, added IBM).

## `as-hegemony`

Analysis results based on AS Hegemony data.

- `downstream-dependency-ip-version.csv`: Base of Table 2. Downstream dependency
by IP version and IP capability.
- `downstreams-at-ixps-as-hegemony-v4.csv`: Base of Table 6. Single-upstream
networks with presence at IXPs and names of the IXPs.
- `dual-stack-downstreams-upstream-relationships.csv`: Base of Table 4.
Relationship of upstream sets for dual-stack downstreams.
- `hg-reachable-via-ixp-as-hegemony-v4.csv`: Base of Table 6. Single-upstream
networks with presence at IXPs *and* potential peering ability with Hypergiants.
- `sibling-classification-as-hegemony-v4.csv`: Base of `BGP view` row of Tables
5 & 9. Contains the sibling classification of single-upstream pairs by different
datasets ([Borges](), [AS2Org](), and [IIL-AS2Org]()).
  - TODO: Link to datasets
  - Borges: Author copy (2025-08-19)
  - AS2Org: 20240401.as-org2info.txt.gz
  - IIL-AS2Org: ii.as-org.v01.2024-01.json (History of repo has been rewritten several times)

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
- `default-route`: Both up- and downstream have a default route and thus result
is inconclusive.
- `single-upstream`: Downstream only has a single upstream.
- `isp-pairs`: Subset of pairs that are considered for the ISP case study.
Selection is based on population threshold so additional columns show for the
*downstream*: The country code, population coverage (>=5%), and rank in the
country based on the [APNIC population estimate]().

## `measured`

Analysis results based on active measurements.

- `downstreams-at-ixps-measured-v4.csv`: Base of Table 6. Single-upstream
networks with presence at IXPs and names of the IXPs.
- `hg-reachable-via-ixp-measured-v4.csv`: Base of Table 6. Single-upstream
networks with presence at IXPs *and* potential peering ability with Hypergiants.
- `sibling-classification-measured-v4.csv`: Base of `Measured` and `ISPs` rows
of Tables 5 & 9. Contains the sibling classification of single-upstream pairs by
different datasets ([Borges](), [AS2Org](), and [IIL-AS2Org]()).

More results will follow.
