# Slack-go Sample

ref: https://github.com/slack-go/slack

# setup

## get package

```
$ go get -u github.com/slack-go/slack
```

## create webhook

create webhook url from https://slack.com/services/new/incoming-webhook

## set your slack webhook to .env

```
SLACK_WEBHOOK={YOUR_SLACK_WEBHOOK}
echo "SLACK_WEBHOOK_URL=$SLACK_WEBHOOK" > .env
```

# usage

1. set post params in main.go

e.g.

```
	params := &slack.MessageParams{
		Color:         slack.ColorGreen,
		AuthorName:    "KotaroYamazaki",
		AuthorLink:    "https://github.com/KotaroYamazaki",
		AuthorIconURL: "https://avatars.githubusercontent.com/u/7589567?v=4",
		Text:          "hello world",
		Footer:        "github.com",
		FooterIconURL: "https://github.githubassets.com/images/modules/logos_page/Octocat.png",
		Timestamp:     time.Now(),
		ButtonText:    "Click Me",
		ButtonURL:     "https://github.com/KotaroYamazaki/slack-go-sample",
	}
```

2. run

```
go run main.go
```

# result

![image](https://user-images.githubusercontent.com/7589567/136696917-ad2e1463-1f49-40b5-a8ab-16c63315e547.png)
