# VK_Universe 
* Version: 3.2
* Last update: 16 Feb 2018
## Settings and start
``` php
require 'VKUniverse.class.php';

try {

 $access_token = 'user_token'; 
 $user_id = 1; 

 $foot = (new VKUniverse)->count_wall($user_id, 'owner', $access_token); // all || owner [ posts ]
 var_dump(json_decode($foot));

} catch (Exception $e) {

 echo 'Error: '.$e->getMessage();

}
```
## The result of the script execution

The result will be given in json format. On the example of the statistics of the wall of Paul Durov
``` 
{
  "response": 
  {
    "likes": 20056370,
    "comments": 1781770,
    "reposts": 906104,
    "views": 93833891,
    "attachments": 
    {
      "count": 267,
      "type": 
      {
        "video": 4,
        "link": 29,
        "photo": 210,
        "doc": 10,
        "poll": 4,
        "photos_list": 1,
        "page": 4,
        "album": 1,
        "note": 3,
        "graffiti": 1
      }
    }
  }
}

```
## Last changes 
<b> from 16 Feb 2018</b>
* Added caching (15 min)
* Exceptions added

## License and Authorship

MIT license, all rights belong to the author of the code <a target="_blank" href="https://vk.com/wnull">Vasily Pirajog</a>

<h4>Allowed free use with copyright notice!</h4>
