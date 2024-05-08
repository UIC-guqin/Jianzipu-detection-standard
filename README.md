

## Label标准

### 一期目标（TBD）

位置字：

| Label | 减字符 |
| ----- | ------ |
| yi    | 一     |
| er    | 二     |
| san   | 三     |
| si    | 四     |
| wu    | 五     |
| liu   | 六     |
| qi    | 七     |
| ba    | 八     |
| jiu   | 九     |
| shi   | 十     |
| wai   | 外     |
| ban   | 半     |

左手指法：

| Label | 减字符 |
| ----- | ------ |
| da    | 大指   |
| shi2  | 食指   |
| zhong | 中指   |
| ming  | 无名指 |
| gui   | 跪指   |

右手指法：

| Label | 减字符 |
| ----- | ------ |
| gou   | 勾     |
| ti    | 剔     |
| mo    | 抹     |
| tiao  | 挑     |
| da2   | 打     |
| zhai  | 摘     |
| pi    | 擘     |
| tuo2  | 托     |



## 识别输出标准

1. 一字一音: 如大九勾四
2. 一字多音: 多音单指法，如挑抹，历
3. 一字重(chong)音: 一字多指法重音，如撮，拨
4. 非音字符: 不是用来描述音的单字，有其他含义，如泛起
5. 多字 掐撮三声等

```json
{
    "type": int         // 1,2,3,4
    "meaning": str      // 非音字符的含义，type为4时使用
    "sound": [          // type为1,2,3时使用
        {// 音1
            "left": {
                "point": int   // 徽位
                "fingering": str  // 指法
            }
            "right":{
                "string": [int]   // 弦位
                "fingering": str  // 指法
            }
        },
				{
          // 音2，如有
        }
    ]
    "unicode": str     // 减字的unicode
}
```

