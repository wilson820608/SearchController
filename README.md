# UISearchController Sample
How to create UISearchController

 ### 簽署協定  
```
@interface ViewController ()<UITableViewDelegate,UITableViewDataSource,UISearchResultsUpdating,UISearchBarDelegate>
```

    
    
### 初始化 UISearchController
```
        _searchController = [[UISearchController alloc] initWithSearchResultsController:nil];
        _searchController.searchResultsUpdater = self;
        _searchController.searchBar.delegate = self;
        self.definesPresentationContext = true;
        _searchController.dimsBackgroundDuringPresentation = NO;
        _searchController.hidesNavigationBarDuringPresentation = YES;
        _searchController.searchBar.frame = CGRectMake(_searchController.searchBar.frame.origin.x,_searchController.searchBar.frame.origin.y, _searchController.searchBar.frame.size.width, 44.0);
```

### 當 UISearchBar 有動作 會觸發這個方法
```
    -(void)updateSearchResultsForSearchController:(UISearchController *)searchController
```
