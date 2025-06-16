# 2.3 Batch Processing Systems

这里简单介绍一下Generic Data Processing Framework，结合下面的图片来说

## General Batch Processing Architecture

**Figure** **2**: Generic Data Processing Framework

```xml
<mxfile host="app.diagrams.net" modified="2025-01-01T00:00:00.000Z" agent="5.0" etag="example" version="21.6.5">
  <diagram name="Batch Processing Architecture" id="batch-arch">
    <mxGraphModel dx="1422" dy="794" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        
        <!-- Data Sources Layer -->
        <mxCell id="2" value="Data Sources Layer" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#dae8fc;strokeColor=#6c8ebf;fontSize=14;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="40" y="40" width="720" height="60" as="geometry" />
        </mxCell>
        
        <!-- Individual Data Sources -->
        <mxCell id="3" value="HDFS" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#e1d5e7;strokeColor=#9673a6" vertex="1" parent="1">
          <mxGeometry x="60" y="120" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="4" value="Data Lakes" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#e1d5e7;strokeColor=#9673a6" vertex="1" parent="1">
          <mxGeometry x="180" y="120" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="5" value="Cloud Storage" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#e1d5e7;strokeColor=#9673a6" vertex="1" parent="1">
          <mxGeometry x="300" y="120" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="6" value="Databases" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#e1d5e7;strokeColor=#9673a6" vertex="1" parent="1">
          <mxGeometry x="420" y="120" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="7" value="File Systems" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#e1d5e7;strokeColor=#9673a6" vertex="1" parent="1">
          <mxGeometry x="540" y="120" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="8" value="APIs" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#e1d5e7;strokeColor=#9673a6" vertex="1" parent="1">
          <mxGeometry x="660" y="120" width="100" height="40" as="geometry" />
        </mxCell>
        
        <!-- Resource Management Layer -->
        <mxCell id="9" value="Resource Management Layer" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#fff2cc;strokeColor=#d6b656;fontSize=14;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="40" y="200" width="720" height="60" as="geometry" />
        </mxCell>
        
        <mxCell id="10" value="Apache YARN" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffeaa7;strokeColor=#d63031" vertex="1" parent="1">
          <mxGeometry x="120" y="280" width="120" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="11" value="Apache Mesos" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffeaa7;strokeColor=#d63031" vertex="1" parent="1">
          <mxGeometry x="280" y="280" width="120" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="12" value="Kubernetes" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffeaa7;strokeColor=#d63031" vertex="1" parent="1">
          <mxGeometry x="440" y="280" width="120" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="13" value="Standalone Mode" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffeaa7;strokeColor=#d63031" vertex="1" parent="1">
          <mxGeometry x="600" y="280" width="120" height="40" as="geometry" />
        </mxCell>
        
        <!-- Processing Engine Layer -->
        <mxCell id="14" value="Processing Engine Layer" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#d5e8d4;strokeColor=#82b366;fontSize=14;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="40" y="360" width="720" height="60" as="geometry" />
        </mxCell>
        
        <mxCell id="15" value="Apache Spark" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#a7f3d0;strokeColor=#047857;fontSize=12;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="80" y="440" width="140" height="80" as="geometry" />
        </mxCell>
        
        <mxCell id="16" value="Hadoop MapReduce" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#a7f3d0;strokeColor=#047857" vertex="1" parent="1">
          <mxGeometry x="260" y="440" width="140" height="80" as="geometry" />
        </mxCell>
        
        <mxCell id="17" value="Apache Hive" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#a7f3d0;strokeColor=#047857" vertex="1" parent="1">
          <mxGeometry x="440" y="440" width="140" height="80" as="geometry" />
        </mxCell>
        
        <mxCell id="18" value="Apache Pig" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#a7f3d0;strokeColor=#047857" vertex="1" parent="1">
          <mxGeometry x="620" y="440" width="140" height="80" as="geometry" />
        </mxCell>
        
        <!-- Application Interface Layer -->
        <mxCell id="19" value="Application Interface Layer" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#f8cecc;strokeColor=#b85450;fontSize=14;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="40" y="560" width="720" height="60" as="geometry" />
        </mxCell>
        
        <mxCell id="20" value="SQL APIs" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffcccb;strokeColor=#d62728" vertex="1" parent="1">
          <mxGeometry x="80" y="640" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="21" value="DataFrame APIs" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffcccb;strokeColor=#d62728" vertex="1" parent="1">
          <mxGeometry x="200" y="640" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="22" value="RDD APIs" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffcccb;strokeColor=#d62728" vertex="1" parent="1">
          <mxGeometry x="320" y="640" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="23" value="ML Libraries" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffcccb;strokeColor=#d62728" vertex="1" parent="1">
          <mxGeometry x="440" y="640" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="24" value="Graph APIs" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffcccb;strokeColor=#d62728" vertex="1" parent="1">
          <mxGeometry x="560" y="640" width="100" height="40" as="geometry" />
        </mxCell>
        
        <mxCell id="25" value="Streaming APIs" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#ffcccb;strokeColor=#d62728" vertex="1" parent="1">
          <mxGeometry x="680" y="640" width="100" height="40" as="geometry" />
        </mxCell>
        
        <!-- Arrows connecting layers -->
        <mxCell id="26" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="2" target="9">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <mxCell id="27" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="9" target="14">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <mxCell id="28" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="14" target="19">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <!-- Data flow arrows from sources -->
        <mxCell id="29" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="3" target="2">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <mxCell id="30" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="4" target="2">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <mxCell id="31" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="5" target="2">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <mxCell id="32" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="6" target="2">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <mxCell id="33" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="7" target="2">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
        <mxCell id="34" value="" style="endArrow=classic;html=1;rounded=0;exitX=0.5;exitY=1;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;" edge="1" parent="1" source="8" target="2">
          <mxGeometry width="50" height="50" relative="1" as="geometry">
            <mxPoint x="390" y="400" as="sourcePoint" />
            <mxPoint x="440" y="350" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```



这里写一下Batch Processing的局限性，我想这个局限性是针对于我这个A Lightweight Hybrid Data Processing Framework for Multi-Structured Data Analysis的局限性,就是Batch Processing具有什么样的局限性才导致我要研发一个Lightweight Hybrid Data Processing Framework来解决Batch Processing的这些局限性。然后给这些局限性来个标号，在Limitations这一列写上是之前哪一个局限性的标号，做到局限性和表格的有关联。表格中的论文一定要真实有效且存在。

## Summary of Existing Research on Batch Processing Systems

The following table summarizes key research contributions in the field of batch processing systems:

| Paper (Citation) | Framework | Data Types | Processing Size | Application Area | Evaluation Methods/Metrics | Limitations |
|---|---|---|---|---|---|---|
| Zaharia et al. (2012) | Apache Spark | Structured, Semi-structured | Large-scale (TB-PB) | Machine Learning, Graph Processing | Throughput, Latency, Memory Usage | High memory requirements, GC overhead |
| Dean & Ghemawat (2008) | MapReduce | Structured | Large-scale (TB-PB) | Web indexing, Data mining | Processing time, Scalability | Disk I/O bottlenecks, Limited programming model |
| Armbrust et al. (2015) | Spark SQL | Structured | Medium to Large (GB-TB) | Data warehousing, Analytics | Query performance, Optimization effectiveness | SQL compatibility limitations |
| Vavilapalli et al. (2013) | YARN | Multi-framework | Cluster-wide | Resource management | Resource utilization, Job completion time | Scheduling overhead, Configuration complexity |
| Meng et al. (2016) | MLlib | Structured, Numerical | Large-scale (TB) | Machine Learning | Algorithm convergence, Scalability | Limited algorithm coverage, Performance tuning complexity |
| Ousterhout et al. (2015) | Spark | Mixed workloads | Large-scale (TB) | Performance analysis | Execution time, Resource efficiency | Workload-specific optimizations needed |
| Shi et al. (2015) | Spark | Structured | Large-scale (TB) | Shuffle optimization | Network overhead, Serialization cost | Data skew handling limitations |
| Hindman et al. (2011) | Mesos | Multi-framework | Cluster-wide | Resource management | Resource sharing efficiency, Fault tolerance | Two-level scheduling complexity |
| Ketu et al. (2020) | Spark | Structured, Time-series | Medium to Large (GB-TB) | Real-time analytics | Processing latency, Accuracy | Micro-batching limitations for true real-time |
| Thiruvathukal et al. (2019) | Spark | Mixed | Large-scale (TB) | Memory management | GC performance, Memory utilization | JVM limitations, Memory fragmentation |



## References

1. Armbrust, M., Xin, R. S., Lian, C., Huai, Y., Liu, D., Bradley, J. K., ... & Zaharia, M. (2015). Spark SQL: Relational data processing in Spark. *Proceedings of the 2015 ACM SIGMOD International Conference on Management of Data*, 1383-1394.

2. Dean, J., & Ghemawat, S. (2008). MapReduce: Simplified data processing on large clusters. *Communications of the ACM*, 51(1), 107-113.

3. Hindman, B., Konwinski, A., Zaharia, M., Ghodsi, A., Joseph, A. D., Katz, R., ... & Stoica, I. (2011). Mesos: A platform for fine-grained resource sharing in the data center. *Proceedings of the 8th USENIX Symposium on Networked Systems Design and Implementation*, 295-308.

4. Ketu, S., Mishra, P. K., & Agarwal, S. (2020). Performance analysis of distributed computing frameworks for big data analytics. *Journal of Big Data*, 7(1), 1-32.

5. Meng, X., Bradley, J., Yavuz, B., Sparks, E., Venkataraman, S., Liu, D., ... & Xin, D. (2016). MLlib: Machine learning in Apache Spark. *Journal of Machine Learning Research*, 17(1), 1235-1241.

6. Ousterhout, K., Rasti, R., Ratnasamy, S., Shenker, S., & Chun, B. G. (2015). Making sense of performance in data analytics frameworks. *Proceedings of the 12th USENIX Symposium on Networked Systems Design and Implementation*, 293-307.

7. Shi, J., Qiu, Y., Minhas, U. F., Jiao, L., Wang, C., Reinwald, B., & Özcan, F. (2015). Clash of the titans: MapReduce vs. Spark for large scale data analytics. *Proceedings of the VLDB Endowment*, 8(13), 2110-2121.

8. Thiruvathukal, G. K., Läufer, K., & Gonzalez, B. (2019). Distributed systems and big data processing with Apache Spark. *Computing in Science & Engineering*, 21(3), 78-81.

9. Vavilapalli, V. K., Murthy, A. C., Douglas, C., Agarwal, S., Konar, M., Evans, R., ... & Saha, B. (2013). Apache Hadoop YARN: Yet another resource negotiator. *Proceedings of the 4th Annual Symposium on Cloud Computing*, 1-16.

10. Zaharia, M., Chowdhury, M., Das, T., Dave, A., Ma, J., McCauly, M., ... & Stoica, I. (2012). Resilient distributed datasets: A fault-tolerant abstraction for in-memory cluster computing. *Proceedings of the 9th USENIX Symposium on Networked Systems Design and Implementation*, 15-28.