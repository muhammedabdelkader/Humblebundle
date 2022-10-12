# Humblebundle
Fetching Humblebundle posts links 

```
for i in {1..1000000};do if [[ $(curl https://blog.humblebundle.com/wp-json/wp/v2/posts/$i | jq ".data.status") -ne 404 ]];then curl https://blog.humblebundle.com/wp-json/wp/v2/posts\?post\=$i | jq '.[]|.link' >> ~/Humble.links; fi; done
```
