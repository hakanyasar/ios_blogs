
![data types](https://github.com/user-attachments/assets/5a584757-36bd-4ad3-b4a8-b9ef07db21cb)


```
isItLikedBefore(postId: postViewModel.post.postId) { result in
            if result == true{
                
                cell.isLikedCheck = true
                cell.likeButton.setImage(UIImage(systemName: "heart.fill"), for: .normal)
            }else{
                
                cell.isLikedCheck = false
                cell.likeButton.setImage(UIImage(systemName: "heart"), for: .normal)
            }
        }

```
