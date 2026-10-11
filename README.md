# 上海理工大学基础学院 · 校园导览

面向 2026 级新生的校园导览站点：平面图定位、楼栋查询、路线指引，附新生手册与培养计划。

## 在线访问

https://ranchunxu.github.io/campus-map/

## 页面

| 页面 | 说明 |
| --- | --- |
| `index.html` | 导览主页面（校园平面图 + 点位标记 + 搜索 + 路线） |
| `handbook.html` | 新生手册（学分/绩点/分流/奖学金等章节） |
| `curriculum.html` | 电子信息类培养计划 |

## 本地运行

纯静态站点，无构建步骤。任选一种：

```bash
# 方式一：Python
python -m http.server 8931

# 方式二：Node
npx serve .
```

然后浏览器打开 http://127.0.0.1:8931/

直接双击 `index.html` 也能看，但手册里的章节跳转建议用本地服务器打开。

## 目录结构

```
index.html / handbook.html / curriculum.html
data/
  campus.json                  点位与楼栋数据
  place_handbook_map.json      点位 → 手册章节映射
  curriculum_eit.json          培养计划数据
  campus-plan-base-*.png       校园平面底图
  board-ground.jpg             展板底图
  wayfinding-ground.jpg        指路牌底图
  handbook/                    新生手册正文（Markdown）
  sources.json                 资料来源
photos/                        实景照片
```
