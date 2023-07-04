## CV
<img src="img/my_photo.jpg" width="75%" height="75%" />

### Voitov Vladislav, 19 y.o

[Telegram](адрес "https://t.me/dobrihlopez")


[Vkontakte](адрес "https://vk.com/dobrihlopez")

dobrihlopez@gmail.com


Mobile phone +375-29-xxx-21-31 

#### About
I'm passionate about android apps development. I started my programming journey in the 9th grade having participated in both online and offline programming competitions. Since then I've tried many frameworks and chose the most engaging one - mobile development.

#### Hard-skills
* English B1
* Kotlin, Java
* RxJava2, Kotlin flows and coroutines
* Jetpack compose
* Dagger2
* MVVM, MVI
* Data/View Binding
* REST API
* Room, retrofit, gson

#### Soft-skills
* Goal-oriented
* Responsible

Spoken languages: Belarusian (native), russian (native)
#### Projects

So far I've completed a couple of projects. Here is a list of the most exciting ones. Feel free to visit my github at [GitHub](адрес "https://github.com/VladislavDobrihlopez") 

  Проекты   | Стек    | Ссылка  |
------------|:-------:|:-------:|
VK mobile client|Jetpack compose, Kotlin flows + coroutines,  Dagger2, Room, Retrofit , Picasso,  MVVM   |[github]("https://github.com/VladislavDobrihlopez/VkNewsClient/tree/develop") 
Diabetes diary |Jetpack compose, Kotlin flows + coroutines,  Hilt, Mongo Db Atlas Realm, Retrofit , Coil, MVI, Multi module architecture|[github](адрес "https://github.com/VladislavDobrihlopez/YourDiabetesDiary/tree/develop") 
Welding control system| Android View, RxJava2, Dagger2, Room, Retrofit, MVVM| [github](адрес "https://github.com/VladislavDobrihlopez/WeldingStartup") 

#### Education

I'm a student at the Belarusian-Russian university specializing in software engineering (2nd year)

__Cources and trainings__:
* __Completed__
    - Android + Java from scratch (Andrey Sumin)
    - Kotlin quick start (Andrey Sumin)
    - Android professional (Andrey Sumin)
    - Jetpack Compose (Andrey Sumin)
    - Android multithreading masterclass (Vitaly Zukanov)

* __In progress__
    - Kotlin coroutines + Flow (Lukas Lechner)


__Code example:__
```
private suspend fun retrieveFeedData(): FeedResponseResult {
        val placeToStartLoadingFrom = nextPostFrom

        if (vkHasNothingToRecommendAnymore()) {
            return FeedResponseResult.EndOfNewsFeed
        }

        val feedResponseResult = try {
            val response = if (placeToStartLoadingFrom == null) {
                recommendationsFeedApiService.loadRecommendations(getUserToken())
            } else {
                recommendationsFeedApiService.loadRecommendations(
                    getUserToken(),
                    placeToStartLoadingFrom
                )
            }
            FeedResponseResult.Success(response)
        } catch (_: Exception) {
            FeedResponseResult.Failure
        }

        if (feedResponseResult is FeedResponseResult.Success) {
            nextPostFrom = feedResponseResult.newsFeedContentResponseDto.content.nextFrom
            val mappedPosts =
                postMapper.mapDtoResponseToEntitiesOfPostItem(feedResponseResult.newsFeedContentResponseDto)
            _posts.addAll(mappedPosts)
        }
        return feedResponseResult
    }
```
