# BlockPos

Represents a position of a block in the world

这个类由mod-id为`crafttweaker`的模组添加. 因此，如果要使用此功能，则需要安装此mod。

## 导入相关包
如果遇到任何问题（例如强制转换数组），则可能需要导入软件包，因此，最好的方式就是导入包支持。
```zenscript
crafttweaker.api.util.BlockPos
```

## Constructor #构造函数
```zenscript
new crafttweaker.api.util.BlockPos(x as int, y as int, z as int);
```
| 参数 | 类型  | 描述                      |
| -- | --- | ----------------------- |
| x  | int | No description provided |
| y  | int | No description provided |
| z  | int | No description provided |



## 方法
### add

Adds two positions together and returns the result.

 返回： `个新的 [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) 带有添加的值`

返回类型： [craftmiliter.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).add(pos as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).add(new BlockPos(3, 2, 1));
```

| 参数 | 类型                                                           | 描述                    |
| -- | ------------------------------------------------------------ | --------------------- |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to add |



Adds the given values to this position, and returns a new position with the new values.

 返回： `一个基于提供值的值和此位置` 的新位置

返回类型： [craftmiliter.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).add(x as double, y as double, z as double);
new BlockPos(0, 1, 2).add(50.21, -20.8, -25.2);
```

| 参数 | 类型     | 描述             |
| -- | ------ | -------------- |
| x  | double | x value to add |
| y  | double | y value to add |
| z  | double | z value to add |



Adds the given values to this position, and returns a new position with the new values.

 返回： `一个基于提供值的值和此位置` 的新位置

返回类型： [craftmiliter.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
新 BlockPost(0, 1, 2) .add(x as int, y as int, z int);
new BlockPost(0, 1, 2).add(50, 20, -25);
```

| 参数 | 类型  | 描述             |
| -- | --- | -------------- |
| x  | int | x value to add |
| y  | int | y value to add |
| z  | int | z value to add |


### crossProduct

Creates a new BlockPos based on the cross product of this position, and the given position

 返回： `一个基于此BlockPos 和给定BlockPos 的交叉产品的新BlockPos`

返回类型： [craftmiliter.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).crossProduct(pos as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).crossProduct(new BlockPos(5, 8, 2););
```

| 参数 | 类型                                                           | 描述                        |
| -- | ------------------------------------------------------------ | ------------------------- |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to cross product |


### distanceSq

Gets the squared distance of this position to the specified BlockPos, using the center of the BlockPos

 返回： `当前位置和给定方块的距离。`

返回类型：双倍数

```zenscript
new BlockPos(0, 1, 2).distanceSq(to as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).distanceSq(new BlockPos(256, 128, 10););
```

| 参数 | 类型                                                           | 描述                        |
| -- | ------------------------------------------------------------ | ------------------------- |
| to | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to check against |



Gets the squared distance of this position to the specified BlockPos

 返回： `当前位置和给定方块的距离。`

返回类型：双倍数

```zenscript
new BlockPos(0, 1, 2).distanceSq(to as crafttweaker.api.util.BlockPos, useCenter as boolean);
new BlockPos(0, 1, 2).distanceSq(new BlockPos(256, 128, 10);, true);
```

| 参数        | 类型                                                           | 描述                                                                    |
| --------- | ------------------------------------------------------------ | --------------------------------------------------------------------- |
| to        | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to check against                                             |
| useCenter | boolean                                                      | should the center of the coordinate be used? (adds 0.5 to each value) |



Gets the squared distance of this position to the specified coordinates

 返回： `当前位置和给定坐标的正方位。`

返回类型：双倍数

```zenscript
new BlockPos(0, 1, 2).distanceSq(x as double, y as double, z as double, useCenter as boolean);
new BlockPos(0, 1, 2).distanceSq(500.25, 250.75, 100.20, false);
```

| 参数        | 类型      | 描述                                                                    |
| --------- | ------- | --------------------------------------------------------------------- |
| x         | double  | x position to check against                                           |
| y         | double  | y position to check against                                           |
| z         | double  | z position to check against                                           |
| useCenter | boolean | should the center of the coordinate be used? (adds 0.5 to each value) |


### down

Creates a new BlockPos based on this BlockPos that is one block lower than this BlockPos

 Returns: `a new BlockPos that is one block lower than this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).down();
```

### east

Creates a new BlockPos based on this BlockPos that is one block east of this BlockPos

 Returns: `a new BlockPos that is one block east of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).east();
```


Creates a new BlockPos based on this BlockPos that is n block(s) east of this BlockPos

 Returns: `a new BlockPos that is n block(s) east of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).east(n as int);
new BlockPos(0, 1, 2).east(2);
```

| 参数 | 类型  | 描述                      |
| -- | --- | ----------------------- |
| n  | int | No description provided |


### manhattanDistance

Gets the Manhattan Distance of this pos compared to a different position

 返回： `位置的曼哈顿距离`

Return type: int

```zenscript
new BlockPos(0, 1, 2).manhattanDistance(other as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).manhattanDistance(new BlockPos(4, 5, 6));
```

| 参数    | 类型                                                           | 描述                                    |
| ----- | ------------------------------------------------------------ | ------------------------------------- |
| other | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to get the distance to |


### north

Creates a new BlockPos based on this BlockPos that is one block north of this BlockPos

 Returns: `a new BlockPos that is one block north of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).north();
```


Creates a new BlockPos based on this BlockPos that is n block(s) north of this BlockPos

 Returns: `a new BlockPos that is n block(s) north of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).north(n as int);
new BlockPos(0, 1, 2).north(10);
```

| 参数 | 类型  | 描述                      |
| -- | --- | ----------------------- |
| n  | int | No description provided |


### offset

Creates a new BlockPos based on this BlockPos that is one block offset of this BlockPos based on the given [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)

 Returns: `a new BlockPos that is 1 block offset of this BlockPos`

返回类型： [craftmiliter.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).offset(direction as crafttweaker.api.util.Direction);
new BlockPos(0, 1, 2).offset(<direction:east>);
```

| 参数        | 类型                                                             | 描述                      |
| --------- | -------------------------------------------------------------- | ----------------------- |
| direction | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction) | No description provided |



Creates a new BlockPos based on this BlockPos that is n block(s) offset of this BlockPos based on the given [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)

 Returns: `a new BlockPos that is n block(s) offset of this BlockPos`

返回类型： [craftmiliter.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).offset(direction as crafttweaker.api.util.Direction, n as int);
new BlockPos(0, 1, 2).offset(<direction:south>, 3);
```

| 参数        | 类型                                                             | 描述                      |
| --------- | -------------------------------------------------------------- | ----------------------- |
| direction | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction) | No description provided |
| n         | int                                                            | No description provided |


### south

Creates a new BlockPos based on this BlockPos that is one block south of this BlockPos

 Returns: `a new BlockPos that is one block south of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).south();
```


Creates a new BlockPos based on this BlockPos that is n block(s) south of this BlockPos

 Returns: `a new BlockPos that is n block(s) south of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).south(n as int);
new BlockPos(0, 1, 2).south(12);
```

| 参数 | 类型  | 描述                      |
| -- | --- | ----------------------- |
| n  | int | No description provided |


### subtract

Subtracts two positions together and returns the result.

 返回： `个新的 [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) 与删除的值。`

返回类型： [craftmiliter.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).subtract(pos as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).subtract(new BlockPos(2, 1, 3));
```

| 参数 | 类型                                                           | 描述                       |
| -- | ------------------------------------------------------------ | ------------------------ |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to remove |


### up

Creates a new BlockPos based on this BlockPos that is one block higher than this BlockPos

 Returns: `a new BlockPos that is one block higher than this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).up();
```


Creates a new BlockPos based on this BlockPos that is n block(s) higher than this BlockPos

 Returns: `a new BlockPos that is n block(s) higher than this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).up(n as int);
new BlockPos(0, 1, 2).up(45);
```

| 参数 | 类型  | 描述                      |
| -- | --- | ----------------------- |
| n  | int | No description provided |


### west

Creates a new BlockPos based on this BlockPos that is one block west of this BlockPos

 Returns: `a new BlockPos that is one block west of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).west();
```


Creates a new BlockPos based on this BlockPos that is n block(s) west of this BlockPos

 Returns: `a new BlockPos that is n block(s) west of this BlockPos`

返回类型：net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).west(n as int);
new BlockPos(0, 1, 2).west(120);
```

| 参数 | 类型  | 描述                      |
| -- | --- | ----------------------- |
| n  | int | No description provided |


### withinDistance

Checks if the given BlockPos is within the specified distance of this BlockPos (this uses the middle of the BlockPos)

 Returns: `true if the given BlockPos is within the given distance of this BlockPos`

Return type: boolean

```zenscript
new BlockPos(0, 1, 2).withinDistance(pos as crafttweaker.api.util.BlockPos, distance as double);
new BlockPos(0, 1, 2).withinDistance(new BlockPos(80, 75, 54);, 10);
```

| 参数       | 类型                                                           | 描述                                             |
| -------- | ------------------------------------------------------------ | ---------------------------------------------- |
| 点        | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to check if it is within the distance |
| distance | double                                                       | distance to check within                       |



## 参数

| 名称 | 类型  | 可获得  | 可设置   |
| -- | --- | ---- | ----- |
| x  | int | true | false |
| y  | int | true | false |
| z  | int | true | false |

## 运算符
### ADD

Adds two positions together and returns the result.

 返回： `个新的 [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) 带有添加的值`

```zenscript
new BlockPos(0, 1, 2) + pos as crafttweaker.api.util.BlockPos
new BlockPos(0, 1, 2) + new BlockPos(3, 2, 1)
```

| 参数 | 类型                                                           | 描述                    |
| -- | ------------------------------------------------------------ | --------------------- |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to add |
### SUB

Subtracts two positions together and returns the result.

 返回： `个新的 [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) 与删除的值。`

```zenscript
new BlockPos(0, 1, 2) - pos as crafttweaker.api.util.BlockPos
new BlockPos(0, 1, 2) - new BlockPos(2, 1, 3)
```

| 参数 | 类型                                                           | 描述                       |
| -- | ------------------------------------------------------------ | ------------------------ |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to remove |

## Casters

| 结果类型 | 是否隐藏  |
| ---- | ----- |
| long | false |
