## Youtube-Channel-Videos-Scraper
A python library that uses browser automation to scrape videos from given youtube channel
It uses [datakund](https://pypi.org/project/datakund) internally

Complete Documentation available [here](https://youtube-api.datakund.com/en/latest/)


### Support
For any help / feedback you can message us here
* datakund@gmail.com
* https://t.me/datakund

### Installation

```sh
pip install youtube-channel-videos-scraper
```

### Import

```javascript
from youtube-channel-videos-scraper import *
```

### Open Channel link

To open channel link we use ``open`` function
It requires **url** as input parameter

```javascript
youtube.open("place_channel_url_here")
```

### Fetch Videos

To fetch videos we use ``channel_videos`` function
It does not require any input parameter
It fetches videos from whichever channel link is opened in browser

```javascript
response=youtube.channel_videos
videos=response['body']
```

### Example Response

```sh
[
   {
      "Title":"Title",
      "Video_Link":"Video_Link"
   },
   {},
   ...
]
```

### Fetch more videos with Scrolling

To fetch more videos of the channel we use ``keypress`` function
It requires **key** as input parameter
This **key** can be any keyboard key which we want to press
We will pass **pagedown** here to scroll down
Then we use ``channel_videos`` function to fetch new loaded videos

```javascript
youtube.keypress("pagedown")
response=youtube.channel_videos()
videos=response['body']
```

We can continue scrolling in while loop to fetch more videos

### DataKund
It uses [datakund](https://pypi.org/project/datakund/) internally to do browser automation
DataKund is an automation library that uses selenium & supports automation of many sites including [Youtube](https://youtube-api.datakund.com/en/latest/), [Amazon](https://amazon-api.datakund.com/en/latest/), [Twitter](https://twitter-api.datakund.com/en/latest/), [LinkedIn](https://linkedin-api.datakund.com/en/latest/) , [Google](https://google-api.datakund.com/en/latest/) etc.
