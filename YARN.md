# YARN 
YARN(Yet Another Resource Negotiator)
HDFS 와 똑같은 Distribute Architecture 을 가지고 있다.
- Resource Manager (master)
    - 전체 클러스터의 이용률과 report 를 가지고 있다.
    - A file 을 두개의 block 으로 처리한다라고 하면 resource manager 는 이것을 처리할 수 있는 node manager 를 찾아서 요청하고 완료된 결과를 수집하는 역할을 한다.
    - YARN 으로 인하여 Map-reduce 에 대한 다양한 방법이 나왔다.  Spark (in-memory) / Apache Giraffe(graph-proccsing)
- Node Manager (worker)
    - all worker reporting resourece manager