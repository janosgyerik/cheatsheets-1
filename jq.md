Given JSON like this:

    {
      "sources": [
        {
          "line": 1,
          "code": "&lt;?php",
          "scmAuthor": "",
          "scmRevision": "",
          "scmDate": "2018-05-24T09:51:34+0200",
          "duplicated": false
        },
        {
          "line": 2,
          "code": "    <span class=\"k\">if</span>(<span class=\"k\">isset</span>($_POST[<span class=\"s\">'a'</span>])){ ",
          "scmAuthor": "",
          "scmRevision": "",
          "scmDate": "2018-05-24T09:51:34+0200",
          "duplicated": false
        },

Extract object having `line: 32`:

    > jq '.sources[] | select(.line == 32)'
    {
      "line": 32,
      "code": "    <span class=\"cd\">// TODO</span>",
      "scmAuthor": "",
      "scmRevision": "",
      "scmDate": "2018-08-09T15:32:29+0200",
      "duplicated": false
    }
