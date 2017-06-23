# WebView弹窗

假如封装APP中有弹窗+跳转会出现跳转到另外一个地址的界面，而WebView本身不能加载这个界面，会调用系统的浏览器重新打开这个界面
![alt](https://github.com/NeusoftSEMI/CommonRepository/blob/master/drawable/Screenshot_20170623-092813.png?raw=true) ![alt](https://github.com/NeusoftSEMI/CommonRepository/blob/master/drawable/Screenshot_20170623-114346.png?raw=true)

调用下面的shouldOverrideUrlLoading方法就可以在同一个webView中加载弹窗后的界面

```java
wb=(WebView)findViewById(R.id.wb);
        wb.getSettings().setJavaScriptEnabled(true);
        wb.setWebViewClient(new WebViewClient() {
            @Override
            public boolean shouldOverrideUrlLoading(WebView view, String url) {
                
                ...
                
                }
                return super.shouldOverrideUrlLoading(view, url);
            }
        });
        wb.loadUrl(URL);
