## LAlertDialog 使用介绍


### 好处  全程只有一个好处 就是使用方便!!!

### 使用方式 
```

   alertDialog =
                            AlertDialog.Builder(this)
                                     //设置布局 参数 布局id 或者 布局 view
                                    .setContentView(R.layout.ui_test_dialog_layout) 
                                    //设置弹出和消失的默认动画           
                                    .setDefaultAnimation()  
                                    // 设置dialog 布局内容充满全屏                                   
                                    .setFullWidth()      
                                     // 点击外部是否可以消失 参数 true 或 false                                      
                                    .setCancelable(false)     
                                    //设置dialog 内部 某个控件可见不可见 false 为 gone ; true 为 Visible 默认Visible                                
                                    .setVisible(R.id.ui_dialog_ok_btn,false)   
                                    // 给控件设置文本 参数1 控件id  参数2 需要设置的文本内容         
                                    .setText(R.id.ui_dialog_input_et,"我们一起学猫叫～～～") 
                                    // 设置dialog 底部弹出 参数 true 表示 底部弹出时带动画; false 表示 弹出时不带动画  默认屏幕是中国间弹出 
                                    .setFromBottom(false)     
                                    //设置自定义宽高                                  
                                    .setWidthAndHeight(900,300) 
                                    //设置自定义弹出和消失动画****                  
                                    .setAnimation(R.style.DialogFromBottom)  
                                    .setOnClickLisenter(R.id.ui_dialog_ok_btn) {
                                            //do Something
                                    }       
                                    .show()                                                     

                    // 根据资源id 获取 控件 
                    val btn : Button = alertDialog?.getView(R.id.ui_dialog_ok_btn) as Button

                    // 获取到控件之后 做需要做的操作
                    btn.setTextColor(ContextCompat.getColor(this,R.color.colorAccent))

                    btn.setBackgroundColor(ContextCompat.getColor(this,R.color.colorPrimaryDark))
```
### Dependency

#### Step 1. Add the JitPack repository to your build file
    
```
        allprojects {
                repositories {
                    ...
                    maven { url 'https://jitpack.io' }
                }
            }
```
#### Step 2. Add the dependency

```
    dependencies {

	}
```