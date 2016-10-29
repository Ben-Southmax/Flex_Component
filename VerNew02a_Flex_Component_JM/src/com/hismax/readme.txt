Package 元則說明:
1. 由江門開發的元件分在 com.hismax.jm 下
2. 共用之元件為 com.hismax.jm.component 下, 以 ____C 結尾
   *** 註1 : 元件一般使用下均為共用, 元件本身不應含有 Data Provider(資料來源)
   *** 註2 : 元件本身不應含有存取外部元件之功能，除了該外部元件己包含在此元件本身。
   *** 註3 : 元件與外部元件溝通的方式均透過 Event.
   *** 註4 : 元件本身需善用繼承來 reuse 其他元件。
   *** 註5 : 元件可以為 .as 或 .mxml
   *** 註6 : 元件不分系統
2. 共用之畫面為 com.hismax.jm.view 下, 以 ____V 結尾
   *** 註1 : View 才會有與後端溝通之方法。
   *** 註2 : 一個 View 會含有許多 Component或者其他 View
   *** 註3 : Component 之間均透過 Event 及其Event本身夾帶之物件.
   *** 註4 : Listener寫在父輩去聴所有元件所發出之事件, 再去操做底下之元件。
3. NS 專屬之 View 放於 com.hismax.ns.view 下, 以 ____V 結尾
4. com,hismax.jm.valueobject 目前應該用不到，以現有 ValueObject 為處理原則
   