# anime recommender


## __Overview__

Recommendation system using KNN(K Nearest Neighbor).


## __Usage__ 

1. Upload two files(anime.csv and raiting.csv) to jupyter notebook. 

2. Put your favorite anime in the * in the bottom cell. 

3. Then the recommended animation is output. 


## __Demo__

[name : Ajin, type : only TV]

```
Anime = 'Ajin'#＊

distance, indice = model_knn.kneighbors(anime_pivot.iloc[anime_pivot.index== Anime].values.reshape(1,-1),n_neighbors=11)
for i in range(0, len(distance.flatten())):
    if  i == 0:
        print('If you like "{0}", I recommend this anime to you!!\n'.format(anime_pivot[anime_pivot.index== Anime].index[0]))
    else:
        print('No.{0}: {1} : {2}' .format(i,anime_pivot.index[indice.flatten()[i]],distance.flatten()[i]))
        if distance.flatten()[i] < 0.65:
         print("★★★★★")
        elif distance.flatten()[i] < 0.75 :
           print("★★★★")
        elif distance.flatten()[i] < 0.8 :
           print("★★★")
        elif distance.flatten()[i] < 0.9 :
           print("★★")
        else:
           print("★")
```

If you like "Ajin", I recommend this anime to you!!

No.1: Koutetsujou no Kabaneri : 0.5961621021362509

★★★★★

No.2: Boku dake ga Inai Machi : 0.6167826151713363

★★★★★

No.3: Hai to Gensou no Grimgar : 0.6379469362551933

★★★★★

No.4: Boku no Hero Academia : 0.6414973657514145

★★★★★

No.5: Dimension W : 0.6428901138976989

★★★★★

No.6: God Eater : 0.648452650519753

★★★★★

No.7: Owari no Seraph: Nagoya Kessen-hen : 0.6526893383034591

★★★★

No.8: Kiseijuu: Sei no Kakuritsu : 0.6540025386627561

★★★★

No.9: One Punch Man : 0.6547459339750734

★★★★

No.10: Re:Zero kara Hajimeru Isekai Seikatsu : 0.6556035238547402

★★★★



## __References__

・<https://qiita.com/yshi12/items/26771139672d40a0be32> 

・<https://dse-souken.com/2021/03/25/ai-20/> 

・<https://qiita.com/sco7825/items/0c9d101ec5daba041b76> 
