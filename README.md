ios-KRKmeans-Algorithm
=================

This's AES256 encrypt algorithm.

``` objective-c
#import "KRKmeansOne.h"
#import "KRKmeansTwo.h"

- (void)kmeans
{
    //One dimensional K-Means, the data set is any number means.
    //1 維 K-Means
	KRKmeansOne *_krKmeans = [KRKmeansOne sharedKmeans];
    _krKmeans.sources = @[@0.33, @0.88, @1, @0.52, @146, @120, @45, @43, @0.4];
    [_krKmeans clustering];
    [_krKmeans printResults];
    
    //Two dimesional K-Means, the data set is (x, y)
    //2 維 K-Means
    KRKmeansTwo *_krKmeansTwo = [KRKmeansTwo sharedKmeans];
    [_krKmeansTwo addSets:[NSMutableArray arrayWithObjects:@[@1, @1], @[@1, @2], @[@2, @2], @[@3, @2], @[@3, @1], nil]];
    [_krKmeansTwo addSets:[NSMutableArray arrayWithObjects:@[@6, @4], @[@7, @6], @[@5, @6], @[@6, @5], nil]];
    _krKmeansTwo.sources = @[@[@5, @4], @[@3, @4], @[@2, @5]];
    [_krKmeansTwo clustering];
    [_krKmeansTwo printResults];
}

@end
```

## Version

V1.0

## License

MIT.
