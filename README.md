# MyNetHttp
OKHttp+Rerofit网络请求框架
页面调用：
 LocalService.getApi().getHealthClassify()
                .subscribeOn(Schedulers.io())
                .observeOn(Schedulers.io())
                .observeOn(AndroidSchedulers.mainThread())
                .subscribe(new AbsAPICallback<List<HealthClassifyBean>>() {
                    @Override
                    protected void onDone(List<HealthClassifyBean> list) {

                        //请求成功，做相应的页面操作

                    }

                    @Override
                    public void onError(Throwable e) {
                        super.onError(e);
                        //e.getMessage() 可获取服务器返回错误信息
                    }
                });