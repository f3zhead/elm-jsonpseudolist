# elm-jsonpseudolist

This package provides a JSON decoder for Javascript Array-like objects. These are objects that have a length and can be indexed, but are not actually Arrays and so don't have any Array methods. Examples include [NodeList](https://developer.mozilla.org/en/docs/Web/API/NodeList) and [TextTrackCueList](https://developer.mozilla.org/en-US/docs/Web/API/TextTrackCueList).
To use it, simply import JsonPseudoList and use the jsonPseudoList decoder as you would with Json.Decode.list:

    >>> Json.Decode.decodeString
    ...     (jsonPseudoList Json.Decode.string)
    ...     """{
    ...           "length": 2,
    ...           "0": "hello",
    ...           "1": "world"
    ...         }"""
    Ok ["hello", "world"]

This is a fork of [lovasoa's package](https://github.com/lovasoa/elm-jsonpseudolist), updated for Elm 0.19.
