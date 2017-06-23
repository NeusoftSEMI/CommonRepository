# WebView弹窗

假如封装APP中有弹窗+跳转 

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
