
# Gurisa REST Contract
*** 

RESTful API Standard used by [Gurisa](https://gurisa.com "Software Developer"). 
Feel free to use and contribute, cheers!

***

## Success Response
```json
{
	"code": "00",
	"status": "SUCCESS",
	"message": "ping success",
	"data": {
		"name": "EduStudent Service",
		"version": "1.0"
	}
}
```

## Failed Response

```json
{
	"code": "01",
	"status": "INVALID_DATA",
	"message": "invalid data",
	"error": [
		{
			"msg": "Invalid value",
			"param": "username",
			"location": "body"
		},
	]
}
```

### Code

|Type|Value|Description  |
|--|--|--|
|string| 00 | Success response with zero exit code |
|string| 01 | General error response code |
|...| ... | ... |


### Status
|Type|Value|Description  |
|--|--|--|
|string| SUCCESS| Success response with zero exit code |
|string| ERROR| General error response |
|string| INVALID_DATA | General invalid data provided by client |
|string| NOT_FOUND | General not found resources (endpoint, data, etc) |
|string| FORBIDDEN | General forbidden access to protected resources |
|string| UNAUTHENTICATE | General unauthenticate access to protected resources |
|...| ... | ... |

### Message
|Type|Value|Description  |
|--|--|--|
|string| [contextual action] | Single string represented |

### Error
|Type|Value|Description  |
|--|--|--|
|array| [multiple value] | Multiple error |
|...| ... | ... |

### Data
|Type|Value|Description  |
|--|--|--|
|object| [single value] | Single resource |
|array| [multiple value] | Multiple resource |
|...| ... | ... |

## Author
- [Raka Suryaardi Widjaja](https://gitlab.com/kokoraka "Raka Suryaardi Widjaja")
 - You're the next contributor?