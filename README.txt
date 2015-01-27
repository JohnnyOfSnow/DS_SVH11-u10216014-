# DS_SVH11-u10216014-
DS_SVH11 = Data Structure Summer Vacation Homwork 11(DFS 深度優先搜尋)

一、程式說明
1.	目標：撰寫有向圖及無向圖之DFS
2.	修動態網頁設計者請用Javascript及Canvas撰寫，未修者請用Java applet。
3.	以鄰接矩陣表示Graph(以一維或二維array)，因此由user輸入時，亦用此方式，且1代表二個vertex連接，0代表不連接。
4.	須包含d[ ]，F[ ]，PI[ ]，Stack等結構(在PI[ ]中-1代表nil)。
5.	模式：
        Run-all mode:一次完成所有內容及過程說明。
        Step mode:一次只完成一步驟，呈現該step之過程說明，且以白、綠、黑色變化;stack之TOP需跟隨變化。
        Quiz mode(測驗模式):要求user輸入d[ ],F[], PI[ ]之內容，且由程式判斷對或錯，錯在何處？需有回饋。
        Clear all:清除所有輸入盒內容及變數恢復為內定初值。
6.	過程說明請搭配演算法
    Algorithm:
      DFS(G)
        for each vertex u in V[G]
          do color[u] <- white
          pi[u] <- NIL
        time <- 0
        for each vertex u in V[G]
          do if color[u] = white
            then DFS-Visit(u)


      DFS-Visit(u)
        color[u] <- gray
        d[u] <- time <- time + 1
        for each v in Adj[u]
          do if color[v] = white
            then pi[v] <- u
              DFS-Visit(v)
        color[u] <- black
        f[u] <- time <- time + 1
