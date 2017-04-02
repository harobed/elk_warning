I have create this repository to test this issue:

```
[WARN ][o.e.d.i.m.MapperService ] [unmapped_type:string] should be replaced with [unmapped_type:keyword]
```

See this thread: https://discuss.elastic.co/t/warn-o-e-d-i-m-mapperservice-unmapped-type-string-should-be-replaced-with-unmapped-type-keyword/79948

How to test the bug:

```
$ docker-compose up
```

wait

go to http://127.0.0.1:5601 and you see this warning:

```
elasticsearch_1  | [2017-04-02T13:00:00,713][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [title]
elasticsearch_1  | [2017-04-02T13:00:00,715][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [timeFieldName]
elasticsearch_1  | [2017-04-02T13:00:00,716][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [intervalName]
elasticsearch_1  | [2017-04-02T13:00:00,718][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [fields]
elasticsearch_1  | [2017-04-02T13:00:00,720][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [sourceFilters]
elasticsearch_1  | [2017-04-02T13:00:00,721][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [fieldFormatMap]
elasticsearch_1  | [2017-04-02T13:00:00,723][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [title]
elasticsearch_1  | [2017-04-02T13:00:00,724][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [timeFieldName]
elasticsearch_1  | [2017-04-02T13:00:00,725][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [intervalName]
elasticsearch_1  | [2017-04-02T13:00:00,725][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [fields]
elasticsearch_1  | [2017-04-02T13:00:00,726][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [sourceFilters]
elasticsearch_1  | [2017-04-02T13:00:00,726][WARN ][o.e.d.i.m.StringFieldMapper$TypeParser] The [string] field is deprecated, please use [text] or [keyword] instead on [fieldFormatMap]
```
