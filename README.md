# GXCardView
卡片式布局(探探附近/QQ配对)，可重用机制，跟tableView一个用法，网上看了很多写得过于复杂，想想还是自己写。

# 喜欢就给个star哦，QQ：279694479

Requirements
--
- iOS 7.0 or later
- Xcode 9.0 or later

Usage in you Podfile:
--

```
pod 'GXCardView'
```

GXCardViewDataSource
--

```objc
- (NSInteger)numberOfCountInCardView:(GXCardView *)cardView;

- (GXCardViewCell *)cardView:(GXCardView *)cardView cellForRowAtIndex:(NSInteger)index;
```

GXCardViewDelegate
--

```objc
- (void)cardView:(GXCardView *)cardView didRemoveCell:(GXCardViewCell *)cell forRowAtIndex:(NSInteger)index;

- (void)cardView:(GXCardView *)cardView didRemoveLastCell:(GXCardViewCell *)cell forRowAtIndex:(NSInteger)index;

- (void)cardView:(GXCardView *)cardView didDisplayCell:(GXCardViewCell *)cell forRowAtIndex:(NSInteger)index;

- (void)cardView:(GXCardView *)cardView didMoveCell:(GXCardViewCell *)cell forMovePoint:(CGPoint)point;
```

重载数据 
--

```objc
- (void)reloadData;
- (void)reloadDataAnimated:(BOOL)animated;
```

可以设置参数
--

```objc
/** 卡片可见数量(默认3) */
@property (nonatomic, assign) NSInteger visibleCount;
/** 行间距(默认10.0，可自行计算scale比例来做间距) */
@property (nonatomic, assign) CGFloat lineSpacing;
/** 列间距(默认10.0，可自行计算scale比例来做间距) */
@property (nonatomic, assign) CGFloat interitemSpacing;
/** 侧滑最大角度(默认15°) */
@property (nonatomic, assign) CGFloat maxAngle;
/** 最大移除距离(默认屏幕的1/4) */
@property (nonatomic, assign) CGFloat maxRemoveDistance;
```

License
--
MIT


