# learn

[newspaper_crawler](https://github.com/arfu2016/nlp/tree/master/nlp_models/newspaper_crawler)

[List of User Agents](https://developers.whatismybrowser.com/useragents/explore/)

[User Agent: Find Out Your Web Browser's UA Here](https://www.whoishostingthis.com/tools/user-agent/)

    scrapy shell -s USER_AGENT='custom user agent' 'http://www.example.com'

[HTTP 403 Responses when using Python Scrapy](https://stackoverflow.com/questions/24814028/http-403-responses-when-using-python-scrapy)

[Avoiding getting banned](https://doc.scrapy.org/en/latest/topics/practices.html#avoiding-getting-banned)

Point to the disired element in the webpage, and right click in chrome for inspect; then you will see the corresponding html part highlighted, right click that part, and choose copy-copy Xpath.

    response.xpath('//*[@itemprop="price"][1]/text()').extract()
    
    response.xpath('//*[@itemprop="price"][1]/text()').re('[.0-9]+')
    
如果是异步加载的网页（移动端的网页非常常见该模式），需要等一些时间，比如几秒，use download delays (2 or higher). See DOWNLOAD_DELAY setting. 否则的话，返回的数据不完整。
