# Ant Colony Optimization

- <a target='_blank' href='https://alsk1369854.github.io/AntColonyOptimization-ACO'>Demo</a>

### Install

```bash
npm install @alsk1369854/ant-colony-optimization
```

### Example

#### index.ts

```ts
import {
  AntColonyOptimization,
  Vector3D,
  Vector2D,
} from "@alsk1369854/ant-colony-optimization";

function getRandomVector(max: number): Vector3D {
  return {
    x: Math.floor(Math.random() * max),
    y: Math.floor(Math.random() * max),
    z: Math.floor(Math.random() * max),
  };
}

// 向量序列
let vectorList: Vector3D[] = [];
for (let i = 0; i < 5; i++) {
  vectorList.push(getRandomVector(10));
}

// 蟻群優化算法
const aco: AntColonyOptimization<Vector3D> = new AntColonyOptimization(
  vectorList
);
// 獲得運算結果
aco.getResult().then((result) => console.log(result));
```

#### _END_
