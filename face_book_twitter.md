```python
from facebook_scraper import get_posts

listposts = []
for post in get_posts("991207408214090", pages=10):
    print(post['text'][:50])
    listposts.append(post)

```


```python
listposts
```




    []




```python
import pandas as pd
 
df = pd.DataFrame(listposts)
df.to_csv('post.csv', header=True, index=False)
```


```python
post = pd.read_csv('post.csv')
```


```python
post
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>post_id</th>
      <th>text</th>
      <th>post_text</th>
      <th>shared_text</th>
      <th>original_text</th>
      <th>time</th>
      <th>timestamp</th>
      <th>image</th>
      <th>image_lowquality</th>
      <th>images</th>
      <th>...</th>
      <th>w3_fb_url</th>
      <th>reactions</th>
      <th>reaction_count</th>
      <th>with</th>
      <th>page_id</th>
      <th>sharers</th>
      <th>image_id</th>
      <th>image_ids</th>
      <th>was_live</th>
      <th>header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1108968836437946</td>
      <td>**YOU CAN COUNT ON PRESIDENT TRUMP **\n**MAKE ...</td>
      <td>**YOU CAN COUNT ON PRESIDENT TRUMP **\n**MAKE ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-02 19:05:43</td>
      <td>1675343143</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-2.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>103</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>5.664907e+15</td>
      <td>['5664906780287256']</td>
      <td>False</td>
      <td>Rita Marcus‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1111770476157782</td>
      <td>🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲\nPresident Trump we...</td>
      <td>🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲🇺🇲\nPresident Trump we...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-07 09:52:08</td>
      <td>1675741928</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>50</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Martha Davis‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1104406396894190</td>
      <td>God bless president TRUMP, and thank you MR.Trump</td>
      <td>God bless president TRUMP, and thank you MR.Trump</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-01-26 04:22:45</td>
      <td>1674685365</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Stuart Kirchoff‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1112192092782287</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-08 02:24:06</td>
      <td>1675801446</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-1.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>390</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>6.626118e+15</td>
      <td>['6626117954081265']</td>
      <td>False</td>
      <td>Rodney Dangler‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1112207622780734</td>
      <td>I love ❤️ you all</td>
      <td>I love ❤️ you all</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-08 03:08:40</td>
      <td>1675804120</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-1.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>252</td>
      <td>NaN</td>
      <td>106793748987941</td>
      <td>NaN</td>
      <td>1.209745e+14</td>
      <td>['120974527564039']</td>
      <td>False</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1111427909525372</td>
      <td>Trump the greatest President in history! He wi...</td>
      <td>Trump the greatest President in history! He wi...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-06 20:51:52</td>
      <td>1675695112</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>307</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>1220332944702810</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Rodney Dangler‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1110373046297525</td>
      <td>Please Mr President help our country 🙏 😢 😔 😞 n...</td>
      <td>Please Mr President help our country 🙏 😢 😔 😞 n...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-05 02:18:44</td>
      <td>1675541924</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>110</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Shirley Cosby‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>7</th>
      <td>1093918151276348</td>
      <td>Mr. Trump is already our president!</td>
      <td>Mr. Trump is already our president!</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-01-08 05:35:52</td>
      <td>1673134552</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>389</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Joe Mostacci‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1109275339740629</td>
      <td>This is the Trump the media doesn’t want you t...</td>
      <td>This is the Trump the media doesn’t want you t...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-03 07:03:47</td>
      <td>1675386227</td>
      <td>NaN</td>
      <td>https://scontent.fdac5-2.fna.fbcdn.net/v/t15.5...</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>120</td>
      <td>NaN</td>
      <td>101642140171339</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1109229353078561</td>
      <td>The Best News....\nDonald Trump Announces 2024...</td>
      <td>The Best News....\nDonald Trump Announces 2024...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-03 04:46:09</td>
      <td>1675377969</td>
      <td>NaN</td>
      <td>https://scontent.fdac5-2.fna.fbcdn.net/v/t15.5...</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>66</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Rita Marcus‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1105359780132185</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-01-27 18:14:19</td>
      <td>1674821659</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-1.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>83</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>5.045695e+14</td>
      <td>['504569491813317']</td>
      <td>False</td>
      <td>Ernesto G Chavarria‎President Donald J. Trump ...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1108474106487419</td>
      <td>❤️❤️❤️</td>
      <td>❤️❤️❤️</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-02 02:03:30</td>
      <td>1675281810</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-1.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>123</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>110680275009988</td>
      <td>NaN</td>
      <td>3.478981e+15</td>
      <td>['3478980982337326']</td>
      <td>False</td>
      <td>Lydia Huddleston‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1111638172837679</td>
      <td>Donal Trump will Rock this Nation back into sh...</td>
      <td>Donal Trump will Rock this Nation back into sh...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-07 04:03:04</td>
      <td>1675720984</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>174</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Tim Lindsey‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>13</th>
      <td>1109905103010986</td>
      <td>President Trump, We need you now!</td>
      <td>President Trump, We need you now!</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-04 08:15:38</td>
      <td>1675476938</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>75</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>Bob Huston‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1111066212894875</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-06 06:42:10</td>
      <td>1675644130</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-2.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>129</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>5.106969e+14</td>
      <td>['510696867867246']</td>
      <td>False</td>
      <td>Ernesto G Chavarria‎President Donald J. Trump ...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>1108943716440458</td>
      <td>Welcome back mr Trump</td>
      <td>Welcome back mr Trump</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-02 18:16:03</td>
      <td>1675340163</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-2.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>53</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>2.114611e+14</td>
      <td>['211461104867530']</td>
      <td>False</td>
      <td>Terry Dean‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>16</th>
      <td>1104942863507210</td>
      <td>God has prepared Trump and all Saints who love...</td>
      <td>God has prepared Trump and all Saints who love...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-01-27 00:41:07</td>
      <td>1674758467</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>87</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>102259852763474</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[]</td>
      <td>False</td>
      <td>David Reichner‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>17</th>
      <td>1111194759548687</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-06 11:50:59</td>
      <td>1675662659</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-1.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>96</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>2.362114e+15</td>
      <td>['2362114400633599']</td>
      <td>False</td>
      <td>Heather Lee‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1111820709486092</td>
      <td>Now that Trump's Facebook and Instagram accoun...</td>
      <td>Now that Trump's Facebook and Instagram accoun...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-07 12:11:32</td>
      <td>1675750292</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-2.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>260</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>1.038807e+14</td>
      <td>['103880689293060']</td>
      <td>False</td>
      <td>Lee Penrod‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>19</th>
      <td>1112192549448908</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-08 02:25:34</td>
      <td>1675801534</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-1.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>135</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>6.626121e+15</td>
      <td>['6626121264080934']</td>
      <td>False</td>
      <td>Rodney Dangler‎President Donald J. Trump 2024</td>
    </tr>
    <tr>
      <th>20</th>
      <td>1108968836437946</td>
      <td>**YOU CAN COUNT ON PRESIDENT TRUMP **\n**MAKE ...</td>
      <td>**YOU CAN COUNT ON PRESIDENT TRUMP **\n**MAKE ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2023-02-02 19:05:43</td>
      <td>1675343143</td>
      <td>https://m.facebook.com/photo/view_full_size/?f...</td>
      <td>https://scontent.fdac5-2.fna.fbcdn.net/v/t39.3...</td>
      <td>['https://m.facebook.com/photo/view_full_size/...</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>103</td>
      <td>[{'name': 'President Donald J. Trump 2024', 'l...</td>
      <td>991207408214090</td>
      <td>NaN</td>
      <td>5.664907e+15</td>
      <td>['5664906780287256']</td>
      <td>False</td>
      <td>Rita Marcus‎President Donald J. Trump 2024</td>
    </tr>
  </tbody>
</table>
<p>21 rows × 51 columns</p>
</div>




```python
import snscrape.modules.twitter  as snstwitter
```


```python

```


```python
sn
```




    <snscrape.modules.twitter.TwitterSearchScraper at 0x1ef2fd0f760>




```python
sn = snstwitter.TwitterSearchScraper('#python')
tweets = []
for i, tweet in enumerate(sn.get_items()):
    data = [tweet.date,
       tweet.id,
       tweet.content,
       tweet.likeCount]
    tweets.append(data)
    if i>50:
        break
    
```

    C:\Users\W.C\AppData\Local\Temp\ipykernel_2024\735482289.py:6: FutureWarning: content is deprecated, use rawContent instead
      tweet.content,
    


```python
tweet_df = pd.DataFrame(tweets,columns=["date","id","content","likecouunt"])
tweet_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>date</th>
      <th>id</th>
      <th>content</th>
      <th>likecouunt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2023-02-26 19:49:22+00:00</td>
      <td>1629931650623610881</td>
      <td>Day 2 of Kick Streaming Never seen stats on tw...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2023-02-26 19:37:55+00:00</td>
      <td>1629928768977371136</td>
      <td>📢 Stats\n\n#JPL #JupilerProLeague #ANDSTA #RSC...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2023-02-26 19:28:19+00:00</td>
      <td>1629926352970215425</td>
      <td>1. Focus on #stats \n\nThis is the precursor t...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2023-02-26 19:07:48+00:00</td>
      <td>1629921188372783104</td>
      <td>25 pts., 9 rebs., 2 asts., 2 stls. vs. Grand F...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2023-02-26 19:07:37+00:00</td>
      <td>1629921142290141184</td>
      <td>@PierrePoilievre Any proof, professor? Or is t...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2023-02-26 18:53:16+00:00</td>
      <td>1629917530818215936</td>
      <td>Dying from choking on food is more Rare than D...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2023-02-26 18:42:55+00:00</td>
      <td>1629914924624510976</td>
      <td>This is the } #stats https://t.co/tzsW9AGX6C</td>
      <td>0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2023-02-26 18:34:15+00:00</td>
      <td>1629912745880477705</td>
      <td>#Stats https://t.co/rwWDCZLQpZ</td>
      <td>0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2023-02-26 18:31:34+00:00</td>
      <td>1629912070996066304</td>
      <td>Bak wen dey had LOU ALCINDOR. Imagine we have ...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2023-02-26 18:25:30+00:00</td>
      <td>1629910542058942464</td>
      <td>If one is earning 25K INR (300USD) per month i...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2023-02-26 17:50:42+00:00</td>
      <td>1629901787590213634</td>
      <td>La 🇫🇷France a installé 13.2GW de ☀️solaire. Su...</td>
      <td>9</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2023-02-26 17:47:37+00:00</td>
      <td>1629901010721288193</td>
      <td>#Stats 📊: L'homme en forme côté Freiburg s'app...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2023-02-26 17:47:13+00:00</td>
      <td>1629900908053114881</td>
      <td>Sur les 118 derniers jours, le ☀️solaire en 🇩🇪...</td>
      <td>6</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2023-02-26 17:42:54+00:00</td>
      <td>1629899824714711041</td>
      <td>📺 #rstatsvideo: Tom Mock | RStudio Connect in ...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2023-02-26 17:38:27+00:00</td>
      <td>1629898703174508544</td>
      <td>#Stats 📊: Jamal Musiala 🇩🇪 fête son anniversai...</td>
      <td>13</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2023-02-26 17:29:50+00:00</td>
      <td>1629896532970606592</td>
      <td>Rohit vs Babar: 47 टेस्ट के बाद रोहित या बाबर,...</td>
      <td>6</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2023-02-26 17:24:15+00:00</td>
      <td>1629895131426897921</td>
      <td>Avec une "erreur" dans le calcul. Un conteneur...</td>
      <td>4</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2023-02-26 17:22:04+00:00</td>
      <td>1629894579968262144</td>
      <td>📢 Stats\n\n#JPL #JupilerProLeague #OHLANT #RAF...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2023-02-26 17:13:23+00:00</td>
      <td>1629892394786390018</td>
      <td>25% say that the church should lead the charge...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2023-02-26 16:48:55+00:00</td>
      <td>1629886239498272769</td>
      <td>Why are class probablities important. Find Out...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>2023-02-26 16:39:29+00:00</td>
      <td>1629883862330351616</td>
      <td>Після закриття зимового трансферного вікна ста...</td>
      <td>5</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2023-02-26 16:14:57+00:00</td>
      <td>1629877688096772096</td>
      <td>Nelle ultime tre stagioni il Team @JumboVismaR...</td>
      <td>3</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2023-02-26 16:14:41+00:00</td>
      <td>1629877623542145024</td>
      <td>#stats https://t.co/iio0evX7JA</td>
      <td>0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2023-02-26 16:13:49+00:00</td>
      <td>1629877405476171776</td>
      <td>#Stats 📊: Chelsea n'a gagné que DEUX matchs de...</td>
      <td>2</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2023-02-26 16:13:27+00:00</td>
      <td>1629877311024627714</td>
      <td>Emission de CO2, en g/kWh, pour la consommatio...</td>
      <td>5</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2023-02-26 16:09:41+00:00</td>
      <td>1629876362231046149</td>
      <td>#Stats 📊: Cristian Stellini 🇮🇹 pendant l'absen...</td>
      <td>11</td>
    </tr>
    <tr>
      <th>26</th>
      <td>2023-02-26 16:05:05+00:00</td>
      <td>1629875205727297538</td>
      <td>#STARDOM #Wrestling #Stats\n\n@TmtmTmx\n\n@PWM...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2023-02-26 16:00:05+00:00</td>
      <td>1629873950065844226</td>
      <td>2022/2023 centuries (variation in the Players ...</td>
      <td>16</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2023-02-26 16:00:00+00:00</td>
      <td>1629873926611378178</td>
      <td>🔉 ⚠️ $BTC 4 Hours Update ⚠️ 🔉\nPrice @ $23252 ...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2023-02-26 16:00:00+00:00</td>
      <td>1629873926594523138</td>
      <td>🔉 ⚠️ $ETH 4 Hours Update ⚠️ 🔉\nPrice @ $1605 (...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>30</th>
      <td>2023-02-26 15:55:32+00:00</td>
      <td>1629872804664610816</td>
      <td>In fact, according to a new poll, 93 percent o...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>31</th>
      <td>2023-02-26 15:50:00+00:00</td>
      <td>1629871409588477955</td>
      <td>📊LIVE STATS\n\nWOLVES VS CAVALIERS\n\n🏆 @NBLen...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>32</th>
      <td>2023-02-26 15:47:23+00:00</td>
      <td>1629870750998855684</td>
      <td>33k sample size:\n\nFrom 2359 hrs Feb 18th (fo...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>33</th>
      <td>2023-02-26 15:42:13+00:00</td>
      <td>1629869452006129665</td>
      <td>Comparaison des émissions de 🏭CO2 en g/kWh pou...</td>
      <td>6</td>
    </tr>
    <tr>
      <th>34</th>
      <td>2023-02-26 15:40:45+00:00</td>
      <td>1629869082626469892</td>
      <td>#Stats 📊: Chelsea n'a marqué que 4 buts en Pre...</td>
      <td>17</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2023-02-26 15:17:35+00:00</td>
      <td>1629863252128849922</td>
      <td>スプリント回数はルキアンで走行距離は山岸祐也、いいタンデム。 / “【公式】福岡vsＣ大阪の...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>36</th>
      <td>2023-02-26 15:03:00+00:00</td>
      <td>1629859583325011968</td>
      <td>colorの違う天才達の言うことを何とか理解しようとして脳と耳が必死だったからかな💦\nレベ...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>37</th>
      <td>2023-02-26 14:53:33+00:00</td>
      <td>1629857205825556483</td>
      <td>Comparaison du nombre de jours à une place don...</td>
      <td>9</td>
    </tr>
    <tr>
      <th>38</th>
      <td>2023-02-26 14:48:21+00:00</td>
      <td>1629855894665134084</td>
      <td>Comparaison du nombre de jours sous une valeur...</td>
      <td>3</td>
    </tr>
    <tr>
      <th>39</th>
      <td>2023-02-26 14:43:43+00:00</td>
      <td>1629854731219656704</td>
      <td>#Angers - #OL (1-3) : premier coup franc direc...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>40</th>
      <td>2023-02-26 14:40:45+00:00</td>
      <td>1629853984742682624</td>
      <td>Comparaison des émissions de 🏭CO2 en g/kWh pou...</td>
      <td>2</td>
    </tr>
    <tr>
      <th>41</th>
      <td>2023-02-26 14:37:54+00:00</td>
      <td>1629853265960607747</td>
      <td>Nombre de jours à une place donnée dans mon cl...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>42</th>
      <td>2023-02-26 14:35:21+00:00</td>
      <td>1629852624211046400</td>
      <td>Nombre de jours sous une valeur donnée d'émiss...</td>
      <td>3</td>
    </tr>
    <tr>
      <th>43</th>
      <td>2023-02-26 14:33:29+00:00</td>
      <td>1629852152871940098</td>
      <td>📢 Stats\n\n#JPL #JupilerProLeague #CLUGNT #Clu...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>44</th>
      <td>2023-02-26 14:29:19+00:00</td>
      <td>1629851105474777089</td>
      <td>#UAAPSeason85 🏐 2-26-23\n\nMen’s Division \nFE...</td>
      <td>10</td>
    </tr>
    <tr>
      <th>45</th>
      <td>2023-02-26 14:27:45+00:00</td>
      <td>1629850710761172996</td>
      <td>Moyennes du taux de 🏭CO2 en g/kWh pour la cons...</td>
      <td>28</td>
    </tr>
    <tr>
      <th>46</th>
      <td>2023-02-26 14:15:00+00:00</td>
      <td>1629847501858643971</td>
      <td>the number of towns in Portugal increased by 1...</td>
      <td>2</td>
    </tr>
    <tr>
      <th>47</th>
      <td>2023-02-26 14:02:40+00:00</td>
      <td>1629844399461900291</td>
      <td>DRS Success: अंपायर का फैसला पलटने में माहिर ह...</td>
      <td>10</td>
    </tr>
    <tr>
      <th>48</th>
      <td>2023-02-26 13:52:08+00:00</td>
      <td>1629841750402424835</td>
      <td>- #Stats \n\n- فاز مانشستر يونايتد على نيوكاسل...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>49</th>
      <td>2023-02-26 13:40:09+00:00</td>
      <td>1629838734534275073</td>
      <td>#survivorGR #SurvivorAllStarGR #survivor2023 #...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>50</th>
      <td>2023-02-26 13:30:23+00:00</td>
      <td>1629836276642861056</td>
      <td>🔔 World Mobile #WMT 🌍📈 Daily Stats\n\n📶 data  ...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>51</th>
      <td>2023-02-26 13:05:16+00:00</td>
      <td>1629829954719428611</td>
      <td>Emissions de 🏭CO2 en g/kWh à 11h00 entre la 🇫🇷...</td>
      <td>6</td>
    </tr>
  </tbody>
</table>
</div>




```python

```




    [datetime.datetime(2023, 2, 26, 19, 43, 4, tzinfo=datetime.timezone.utc),
     1629930061708029952,
     'AI Best: #GeoSpatial Analysis with #Python!. #BigData #Analytics #AI #MachineLearning #DataScience #IoT #IIoT #RStats #JavaScript #ReactJS #CloudComputing #Serverless #DataScientist #Linux #Mathematics #Programming #Coding #100DaysofCode\nhttps://t.co/V9NLpiY4eK https://t.co/B1omnYc0sc',
     0]



# facebook


```python
import snscrape.modules.facebook as fb
import datetime as dt

```


```python
query = 'from:facebook since:2021-01-01 until:2021-01-31'

```


```python
import snscrape.modules.facebook as snfacebook
import pandas as pd
items = 100
list_facebook = []
for i, fb in enumerate(snfacebook.FacebookGroupScraper(group='makeupartistsgroup').get_items()):
    if i > items:
        break
    list_facebook.append(fb.content)

DATA_FACEBOOK = pd.DataFrame(data=list_facebook, columns=['text'])
DATA_FACEBOOK.head()
```


    ---------------------------------------------------------------------------

    ScraperException                          Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_2024\1697075620.py in <module>
          3 items = 100
          4 list_facebook = []
    ----> 5 for i, fb in enumerate(snfacebook.FacebookGroupScraper(group='makeupartistsgroup').get_items()):
          6     if i > items:
          7         break
    

    ~\anaconda3\lib\site-packages\snscrape\modules\facebook.py in get_items(self)
        323 
        324                 if 'content:{pagelet_group_mall:{container_id:"' not in r.text:
    --> 325                         raise snscrape.base.ScraperException('Code container ID marker not found (does the group exist?)')
        326 
        327                 soup = bs4.BeautifulSoup(r.text, 'lxml')
    

    ScraperException: Code container ID marker not found (does the group exist?)



```python
posts = scrape_facebook_posts(query)

```


    ---------------------------------------------------------------------------

    ScraperException                          Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_2024\3338523394.py in <module>
    ----> 1 posts = scrape_facebook_posts(query)
    

    ~\AppData\Local\Temp\ipykernel_2024\4125870572.py in scrape_facebook_posts(query)
          4 
          5     # Use snscrape to extract the posts
    ----> 6     for post in fb.FacebookGroupScraper(query + ' lang:en').get_items():
          7         posts.append({
          8             'id': post.id,
    

    ~\anaconda3\lib\site-packages\snscrape\modules\facebook.py in get_items(self)
        323 
        324                 if 'content:{pagelet_group_mall:{container_id:"' not in r.text:
    --> 325                         raise snscrape.base.ScraperException('Code container ID marker not found (does the group exist?)')
        326 
        327                 soup = bs4.BeautifulSoup(r.text, 'lxml')
    

    ScraperException: Code container ID marker not found (does the group exist?)



```python

```


    ---------------------------------------------------------------------------

    WorksheetNotFound                         Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_4960\2567447956.py in <module>
          1 sheet_data = client.sheet.get('1iBVjeg_dkOuLUwcM3qAy002fk8R4NEJxUzkcTEYWIhI')
          2 sheet = client.open_by_url("https://docs.google.com/spreadsheets/d/1iBVjeg_dkOuLUwcM3qAy002fk8R4NEJxUzkcTEYWIhI/edit#gid=1979203912")
    ----> 3 wks = sheet.worksheet_by_title('Sheet1')
          4 print(wks)
    

    ~\anaconda3\lib\site-packages\pygsheets\spreadsheet.py in worksheet_by_title(self, title)
        195         :returns: :class:`Worksheets <Worksheet>`.
        196         """
    --> 197         return self.worksheet('title', title)
        198 
        199     def add_worksheet(self, title, rows=100, cols=26, src_tuple=None, src_worksheet=None, index=None):
    

    ~\anaconda3\lib\site-packages\pygsheets\spreadsheet.py in worksheet(self, property, value)
        186         :returns: :class:`Worksheets <Worksheet>`.
        187         """
    --> 188         return self.worksheets(property, value)[0]
        189 
        190     def worksheet_by_title(self, title):
    

    ~\anaconda3\lib\site-packages\pygsheets\spreadsheet.py in worksheets(self, sheet_property, value, force_fetch)
        167             sheets = [x for x in self._sheet_list if getattr(x, sheet_property) == value]
        168             if not len(sheets) > 0:
    --> 169                 raise WorksheetNotFound()
        170         return sheets
        171 
    

    WorksheetNotFound: 



```python

```


    ---------------------------------------------------------------------------

    HttpError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_4960\2971753004.py in <module>
    ----> 1 data = client.sheet.get('1WxrMbgqKLkW7SHhkrbir26oqQh6J_uFa')
    

    ~\anaconda3\lib\site-packages\pygsheets\sheet.py in get(self, spreadsheet_id, **kwargs)
        163         if 'includeGridData' not in kwargs:
        164             kwargs['includeGridData'] = True
    --> 165         return self._execute_requests(self.service.spreadsheets().get(spreadsheetId=spreadsheet_id, **kwargs))
        166 
        167     #################################
    

    ~\anaconda3\lib\site-packages\pygsheets\sheet.py in _execute_requests(self, request)
        494         """
        495         try:
    --> 496             response = request.execute(num_retries=self.retries)
        497         except HttpError as error:
        498             if error.resp['status'] == '429' and self.check:
    

    ~\anaconda3\lib\site-packages\googleapiclient\_helpers.py in positional_wrapper(*args, **kwargs)
        128                 elif positional_parameters_enforcement == POSITIONAL_WARNING:
        129                     logger.warning(message)
    --> 130             return wrapped(*args, **kwargs)
        131 
        132         return positional_wrapper
    

    ~\anaconda3\lib\site-packages\googleapiclient\http.py in execute(self, http, num_retries)
        936             callback(resp)
        937         if resp.status >= 300:
    --> 938             raise HttpError(resp, content, uri=self.uri)
        939         return self.postproc(resp, content)
        940 
    

    HttpError: <HttpError 400 when requesting https://sheets.googleapis.com/v4/spreadsheets/1WxrMbgqKLkW7SHhkrbir26oqQh6J_uFa?fields=%2A&includeGridData=true&alt=json returned "This operation is not supported for this document". Details: "This operation is not supported for this document">



```python

```

    <Spreadsheet 'sector_fundflow' Sheets:1>
    


```python

```


```python

```

    <Worksheet 'Sheet1' index:0>
    




    47


