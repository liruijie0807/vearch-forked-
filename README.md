<div align="center">
  <img src="docs/img/vearch_logo.png">
</div>

[![Build Status](https://github.com/vearch/vearch/actions/workflows/CI.yml/badge.svg)](https://github.com/vearch/vearch/actions/workflows/CI.yml)  &nbsp;&nbsp;&nbsp; [![Gitter](https://badges.gitter.im/vector_search/community.svg)](https://gitter.im/vector_search/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
## Overview

Vearch is a scalable distributed system for efficient similarity search of deep learning vectors. 

## Quick start
![docs/img/plugin/main_process.gif](docs/img/plugin/main_process.gif)

* Quickly compile the source codes to build a distributed vector search system with RESTful API, please see [docs/SourceCompileDeployment.md](docs/SourceCompileDeployment.md).

* Vearch can be leveraged to build a complete visual search system to index billions of images. The image retrieval plugin for object detection and feature extraction is also required. For more information, please refer to [docs/Quickstart.md](docs/Quickstart.md).

* Vearch Python SDK enables vearch to use locally. Vearch python sdk can be installed easily by pip install vearch. For more information, please refer to [docs/APIPythonSDK.md](docs/APIPythonSDK.md).

## APIs and Use Cases


### LowLevelAPI
* [docs/APILowLevel.md](docs/APILowLevel.md)
* For GPU [docs/APILowLevel.md](docs/APILowLevelOnGPU.md)


### VisualSearchAPI
* [docs/APIVisualSearch.md](docs/APIVisualSearch.md)

### PythonSDKAPI
* [docs/APIPythonSDK.md](docs/APIPythonSDK.md)

## Document

* https://vearch.readthedocs.io/en/latest
* https://vearch.readthedocs.io/zh_CN/latest

## Components

<details>
  <summary><b>Vearch Architecture</b></summary>

![arc](docs/img/VearchArch.jpg)

</details>

<details>
  <summary><b>Master</b></summary>
  Responsible for schema mananagement, cluster-level metadata, and resource coordination. 
</details>

<details>
  <summary><b>Router</b></summary>
  Provides RESTful API: `create`  , `delete`  `search` and `update` ; request routing, and result merging. 
</details>

<details>
  <summary><b>PartitionServer (PS)</b></summary>
  Hosts document partitions with raft-based replication.

  Gamma is the core vector search engine implemented based on [faiss](https://github.com/facebookresearch/faiss). It provides the ability of storing, indexing and retrieving the vectors and scalars.
</details>

## Benchmarks

* [benchmarks](/engine/benchs/README.md)

## Reference
Reference to cite when you use Vearch in a research paper:
```
@misc{li2019design,
      title={The Design and Implementation of a Real Time Visual Search System on JD E-commerce Platform}, 
      author={Jie Li and Haifeng Liu and Chuanghua Gui and Jianyu Chen and Zhenyun Ni and Ning Wang},
      year={2019},
      eprint={1908.07389},
      archivePrefix={arXiv},
      primaryClass={cs.IR}
}
```

## Community
You can report bugs or ask questions in the [issues page](https://github.com/vearch/vearch/issues) of the repository.

For public discussion of Vearch or for questions, you can also send email to vearch-maintainers@groups.io.

Our slack : https://vearchwrokspace.slack.com

## Known Users
Welcome to register the company name in this issue: https://github.com/vearch/vearch/issues/230 (in order of registration)

欢迎在此 issue https://github.com/vearch/vearch/issues/230 中登记公司名称

![科大讯飞](static/kedaxunfei.png)
![飞搜科技](static/faceall.png)
![君库科技](static/bigbigwork.png)
![爱奇艺](static/iqiyi.png)
![人民科技](static/peopletech.png)
![趣头条](static/qutoutiao.png)
![网易严选](static/wangyiyanxuan.png)
![咸唐科技](static/sunthang.png)
![华为技术](static/huawei.png)
![OPPO](static/oppo.png)
![汽车之家](static/autohome.png)
![芯翌智能](static/xforwardai.png)
![图灵机器人](static/turingapi.png)
![金山云](static/ksyun.png)
![汇智通信](static/teligen.png)
![小红书](static/xiaohongshu.png)
![VIVO](static/vivo.png)
![京东](static/jd.png)
![中原消费金融](static/zhongyuan_consumer_finance.jpg)

## License

Licensed under the Apache License, Version 2.0. For detail see [LICENSE and NOTICE](https://github.com/vearch/vearch/blob/master/LICENSE).
