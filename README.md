### Feat : 체육관 서비스 Ver 0.0.1   

## 😄 Service introduce
### 학교  스포츠 시설 예약 및 커뮤티니 플랫폼 
- `로그인,회원가입`
- `운동시설 예약, 예약 취소`
- `커뮤니티 글쓰기,삭제,수정,댓글`
- `현재위치 날씨정보`
- `닉네임 변경 ,포인트 충전,내가 쓴 글,댓글 보기`


## 📱 Tech Stack
` Kotlin ` `GSON` `OkHttp` `RetrofitCoroutines` `Glide`   
`AAC` `DataBinding` `LiveData` `Navigation` `Repository` `ViewModel`

## ⚙️  Architecture
`MVVM`


------------------------------------------


### 로고,로그인,예약 홈,예약 화면
| 로고 | 로그인 | 예약 홈 | 예약 화면 |
| ------------ | ------------- |------------- |------------- |
| ![Screenshot_20230814-203532_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/2abb3f12-56d4-4c2b-a200-11c2c6bdd4a8)| ![Screenshot_20230814-203521_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/9de93186-d728-45dc-8a43-16ba32b0f396) |![Screenshot_20230814-203547_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/8020bb67-6c7d-4b95-b7bb-574dfaceee22)| ![Screenshot_20230814-203604_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/33b4a90d-902a-4f62-9f44-ead9e8f13f78) |

### 주변정보,게시판,날씨,내정보
| 주변정보 | 게시판 | 날씨 | 내정보 |
| ------------ | ------------- |------------- |------------- |
| ![Screenshot_20230814-203607_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/247867cb-4f0b-416a-ba39-18b7bd9a7908)| ![Screenshot_20230814-203614_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/0a91e2ff-12fe-4c18-bcb4-6a86edc1b7a8)|![Screenshot_20230814-203618_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/893fcd2c-7fc6-4488-9bc4-21f19ba52858)| ![Screenshot_20230814-203621_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/f8701548-ac26-4518-8479-7989995e8a0a)|

### 글 쓰기,글 정보,글 메뉴바,글 수정
| 글 쓰기 | 글 정보 | 글 메뉴바 | 글 수정 |
| ------------ | ------------- |------------- |------------- |
| ![Screenshot_20230814-210618_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/529f9114-f028-4deb-b3e1-d2e98447cf65)| ![Screenshot_20230814-203720_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/816172b1-dc83-4a11-9add-b4ca8e1eecb4)|![Screenshot_20230814-210637_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/2f8f0857-cbfc-49c9-8af8-330e38c1a797)| ![Screenshot_20230814-210627_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/1ecb59f4-3fa8-42a5-aeec-54b133069672) |

### 닉네임 설정,내가 쓴 글보기,내가 쓴 댓글 보기, 포인트 충전
| 닉네임 설정 | 내가 쓴 글보기 | 내가 쓴 댓글 보기 | 포인트 충전 |
| ------------ | ------------- |------------- |------------- |
| ![Screenshot_20230814-211517_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/30c0b62b-71ae-485c-a84a-2a6c41988011)| ![Screenshot_20230814-203709_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/e1f836af-7b55-4922-a1cb-50736d1e7def)|![Screenshot_20230814-203626_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/78056a66-8365-4a64-904b-1e3a04041f12)| ![Screenshot_20230814-203624_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/7fc2ded0-e39d-4649-9fac-3c45bb0bcdb4) |

### 예약 홈 메뉴바,예약 내역,예약 내역 정보
| 예약 홈 메뉴바 | 예약 내역 | 예약 내역 정보 | 
| ------------ | ------------- |------------- |
| ![Screenshot_20230814-203937_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/d841e47d-5eaf-4b90-bb64-e5c92975fc66)| ![Screenshot_20230814-203752_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/0ea45a27-b3a4-4726-be21-db0ab0d8f5fd)|![Screenshot_20230814-204112_test](https://github.com/GNU-SPORTS/SPORTS-CLIENT-APP/assets/97229292/6ce83cf6-3425-4bd2-9127-d285ffe29067)|

## 🚀 트러블 슈팅

### 🧑🏻‍💻 안드로이드
<details>
<summary>
<h3>🛠 트러블 슈팅 1</h3>
</summary>
<div markdown="3">

- **Problem & Reason**
- 기존의 sharedprefernce 만 사용하는 방식
```
기존 방식은 토큰을 SharedPreferences에 저장하고 필요할 때마다 수동으로 토큰을 가져와 요청 헤더에 추가하였습니다 이로 인해 각각의 요청에서 토큰을 일일이 관리하고 추가해야 번거로움 있고
코드 낭비가 심하다고 느낌
```

- **To Solve**

<details>
<summary>
<h3>🛠 트러블 슈팅 2</h3>
</summary>
- **Problem & Reason**
- 커뮤니티 글 API를 호출할때 한번에 20개로 제한이 되어있어 페이지를 따로 만들어야하는 낭비가 생김
- 또한 글 검색을 할때 현재 페이지 글만 검색되는 오류 발견


- **To Solve**
- 특정 글을 가져오는 API를 이용하여 모든 글을 가져올 수 있도록 함
- 스크롤을 내릴 때마다 글 하나씩 호출하여 계속해서 글을 가져옴
- 모든 글 정보를 가져와서 page 처리하지 않고 특정 글 가져오는 api를 이용하여 메모리 낭비를 줄임

PostViewmodel.kt
  ```
   private var page = 0;

    suspend fun loadMore() {
        if (isLoading.value) return
        if (isLast) return

        isLoading.value = true

        val response = suspendCoroutine<PostsResponse> {
            apiService.searchPosts("title", query.value, _sortType.value.value, 20, page)
                .enqueue(object : Callback<PostsResponse> {
                    override fun onResponse(
                        call: Call<PostsResponse>,
                        response: Response<PostsResponse>
                    ) {
                        it.resumeWith(Result.success(response.body() ?: PostsResponse().apply {
                            last = true
                        }))
                    }

                    override fun onFailure(call: Call<PostsResponse>, t: Throwable) {
                        t.printStackTrace()

                        it.resumeWith(Result.success(PostsResponse().apply {
                            last = true
                        }))
                    }
                })
        }

        isLoading.value = false

        val result = if (page == 0) {
            response.content
        } else {
            posts.value + response.content
        }

        page += 1
        isLast = response.last
        posts.emit(result)
    }
}

enum class PostSortType(val value: String) {
    LATEST("latest"),
    OLDEST("oldest")
}

  ```
Postfragment.kt
```
private val launchEditor =
        registerForActivityResult(ActivityResultContracts.StartActivityForResult()) { result ->
            if (result.resultCode == Activity.RESULT_OK) {
                lifecycleScope.launch {
                    viewModel.refresh()
                }
            }
        }

    private val launchViewer =
        registerForActivityResult(ActivityResultContracts.StartActivityForResult()) { result ->
            if (result.resultCode == Activity.RESULT_OK) {
                val old: Post? = result.data?.getParcelableExtra("old")
                val new: Post? = result.data?.getParcelableExtra("new")

                if (old == null) return@registerForActivityResult

                val posts = ArrayList(viewModel.posts.value)
                val index = posts.indexOfFirst { it.id == old.id }
                if (index >= 0) {
                    if (new != null) {
                        posts[index] = new;
                    } else {
                        posts.removeAt(index)
                    }

                    viewModel.posts.tryEmit(posts)
                }
            }
        }
```
</div>
