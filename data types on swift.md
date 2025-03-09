
![data types](https://github.com/user-attachments/assets/5a584757-36bd-4ad3-b4a8-b9ef07db21cb)


```
if indexPath.item == self.feedViewModel.postList.count-1 && !FeedPaginationSingletonModel.sharedInstance.isFinishedPaging {PaginationSingletonModel.shPaginationSingletonModel.sh
            
            self.webService.continuePagesFeed { postList in
                
                self.feedViewModel = FeedVcViewModel(postList: postList)
                
                DispatchQueue.main.async {
                    
                    self.tableView.reloadData()
                }
            }
        }

```
