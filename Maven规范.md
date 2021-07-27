### Maven配置规范

#### 多模块

根模块坐标：

```
<groupId>域名</groupId>
<artifactId>项目名</artifactId>
<version>版本号</version>
```

子模块坐标

```
<artifactId>项目名-模块名</artifactId>
```

#### 版本控制

在父POM中统一控制版本，各子模块原则上不允许使用自定义版本。对于各模块需要单独依赖的外部模块，可以将版本定义在各子模块中。

对于引入的同一项目的其他模块，统一使用`${project.version}`来指定，不允许直接写版本号。

