---
title: "MHopCAV: Multi-Hop Clustering for Autonomous Vehicle Networks"
authors:
- admin
- Mustafa Ilhan Akbas
date: "2020-03-28T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2020-03-28T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In Florida Conference on Recent Advances in Robotics 2018
publication_short: In FCRAR 2018

abstract: Autonomous vehicle (AV) technology will have a massive impact on the transportation infrastructure [1]. Intelligent transportation systems are going to be available as vehicle (V2V) and vehicle to infrastructure (V2I) communication become available together with AV technology. In the intelligent transportation systems, the communication among AVs and between AV networks and the infrastructure will be critical. Therefore, clustering solutions must be developed for AV fleets. In this paper, we present the clustering protocol, MHopCAV, the Multi-Hop Clustering Algorithm for Autonomous Vehicle Networks. MHopCAV uses the k-hop clustering algorithm [2], which is designed for dynamic, wireless networks, and adapts it for the clustering of nodes in ACV networks. The k-hop Clustering Algorithm uses a set of four rules to distribute a cluster based on weights. There is a minimum and maximum weight that are defined, "MIN" and "MAX" respectively, as well as the weight of each node, "wn". The cluster head is the node with the MAX weight. The cluster heads also have the network of nodes surrounding them, "N(n)". The set of rules are as follows: Rule 1: This rule creates the basis for the hierarchical structure of each cluster, where each node will adopt a weight one less than whatever the greatest weight in its network is. if max(W(N(n))) > wn, wn = max(W(N(n)))-1 Rule 2: Whenever all nodes in a network have the minimum weight, the node will declare itself the cluster head. if max(W(N(n)) == MIN && wn == MIN, wn = MAX; Rule 3: In order to avoid fragmentation, when none of the nodes are the cluster head, the node will lower its weight by one. if max(W(N(n))) <= wn && wn != MAX, wn = wn-1; Rule 4: When there are multiple cluster heads, some other criteria can be used to decide which node will remain cluster head. if max(W(N(n)) == MAX && wn == MAX, wn = apply criterion to select a node from set(max(W(N(n)), wn); wn = wn-1; MHopCAV adapts k-hop clustering algorithms for AV networks. In these networks, the members of a cluster are defined within a predefined communication range and the maximum weight found in that network, "W(N(n))". AVs use their communication capabilities to announce their properties to other AVs around them periodically, and from the information gathered, calculate their own weight in the network. Each node has its own update interval at which it sends out the information including its address, weight and energy. The energy is important in this update since for rule four, the node with the most battery left is used as the cluster head. Each node stores every one of these packets as a neighbor ("N(n)") and uses the timestamp given in it to check if it hasn't been updated for mobility purposes. As a results of the highly mobile nature of AV network, MHopCAV ensures that nodes that are not within range of any other node adopt the minimum weight. Additionally, the neighbors are traversed to remove any node that has not been heard from for a preset time interval. OMNeT++ [3] is used for the simulation study of MHopCAV. OMNeT++ allows realistic simulation of the mobility and wireless networking features of AV networks.

# Summary. An optional shortened abstract.
summary: Simulating a multihop clustering algorithm for connected vehicles.

tags:
- Simulation
- Connected Vehicles
- OMNeT++
- Ad-hoc Clustering Algorithms
featured: true

links:
url_pdf: http://mae.ucf.edu/fcrar2018/wp-content/uploads/2018/05/19_FPU-Autonomous-Medrano-Berumen-Akbas-cr.pdf
url_code: '#'
url_dataset: '#'
url_poster: '#'
url_project: ''
url_slides: ''
url_source: '#'
url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'OMNeT++ simulation of connected vehicles'
  focal_point: Smart
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
