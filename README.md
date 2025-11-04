# 高校危化试剂仓储系统

## 前言

随着高校科研活动的日益频繁，危险化学品的管理显得尤为重要。为了提高危化试剂的储存和管理效率，降低安全风险，我们开发了一套高校危化试剂仓储系统。本项目采用Java语言，结合Spring Boot框架，以及前端技术如JS、Vue和CSS3等，旨在为高校提供一个安全、便捷的危化试剂管理解决方案。

## 内容介绍

本项目主要包括以下功能模块：用户管理、试剂信息管理、仓库管理、入库管理、出库管理等。系统通过科学的信息化手段，实现了试剂的全生命周期管理，确保了试剂的安全、合规使用。此外，系统还提供了丰富的查询统计功能，方便管理人员实时了解仓库状况，为决策提供数据支持。

## 技术介绍

- 语言：Java
- 使用框架：Spring Boot
- 前端技术：JS、Vue、CSS3
- 开发工具：IDEA/Eclipse
- 数据库：MySQL 5.7/8.0
- 数据库管理工具：phpstudy/Navicat
- JDK版本：jdk1.8
- Maven：apache-maven 3.8.1-bin
- 前端环境：Node.Js 12\14\16

## 核心代码

以下是项目中一个简单的示例代码，展示了如何实现试剂信息的增删改查功能：

```java
@RestController
@RequestMapping("/api/chemicals")
public class ChemicalController {

    @Autowired
    private ChemicalService chemicalService;

    // 查询试剂信息
    @GetMapping("/{id}")
    public Chemical getChemicalById(@PathVariable Long id) {
        return chemicalService.getById(id);
    }

    // 添加试剂信息
    @PostMapping("/")
    public Chemical addChemical(@RequestBody Chemical chemical) {
        return chemicalService.save(chemical);
    }

    // 修改试剂信息
    @PutMapping("/{id}")
    public Chemical updateChemical(@PathVariable Long id, @RequestBody Chemical chemical) {
        chemical.setId(id);
        return chemicalService.update(chemical);
    }

    // 删除试剂信息
    @DeleteMapping("/{id}")
    public void deleteChemical(@PathVariable Long id) {
        chemicalService.deleteById(id);
    }
}
```

## 免费源码获取

8000套系统成品，复制到浏览器：www.yuque.com/yuqueyonghux32e1j/kxdc9g 
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

## 项目截图

（此处为空）
## 万字文档
![文档介绍](https://img14.360buyimg.com/ddimg/jfs/t1/338393/1/3576/156947/68b1ad0cF74dc525c/ff9cd6c574295685.jpg)
