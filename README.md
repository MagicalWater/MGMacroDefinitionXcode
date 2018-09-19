# MGMacroDefinitionXcode
Xcode 宏定義方式

1. 選擇專案 Build Settings
2. 選擇 ALL , Combined
3. 搜索 Other Swift Flags
4. 在 Debug 跟 Release 後面加入需要定義的名稱, 字串開頭加入 -D

例如在 Debug 模式 要定義 AA  
在 Debug 的 value 部位點兩下, 跳出框框後選擇 +  
在新的一行加入 

    -DAA
    
接著在程式碼內就能應用, 應用方式如下

    #if AA
    
    let mAppType: String = "debug";
    
    #else
    
    let mAppType: String = "release";
    
    #endif
