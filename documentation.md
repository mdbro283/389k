
# Worldwide Sporting Events

---

Name: Michael Brody

Date: 12/06/2018

Project Topic: Worldwide Sporting Event Planner

URL:

---


### 1. Data Format and Storage

Data point fields:
- `Field 1`:  name       `Type: String`
- `Field 2`: city       `Type: String`
- `Field 3`:  state       `Type: String`
- `Field 4`:  country      `Type: String`
- `Field 5`:  capacity       `Type: Number`
- `Field 6`:  name       `Type: String`
- `Field 7`:  arenaName       `Type: String`
- `Field 8`:  date       `Type: Date`
- `Field 9`:  teams       `Type: [String]`
- `Field 10`:  info       `Type: String`
Schema:
```javascript
{
  name: {
    type: String,
    unique: true
  },
  city: {
    type: String
  },
  state: {
    type: String
  },
  country: {
    type: String
  },
  capacity: {
    type: Number
  }
  name: {
    type: String,
    unique: true
  }
  date: {
    type: Date
  },
  arenaName: {
    type: String
  },
  teams: {
    type: [String]
  },
  info: {
    type: String
  }
}
```

### 2. Add New Data

HTML form route: `/new_arena`
HTML form route: `/new_event`

POST endpoint route: `/api/new_arena`
POST endpoint route: `/api/new_event`


Example Node.js POST request to endpoint:
```javascript
var request = require("request");

var options = {
    method: 'POST',
    url: 'http://localhost:3000/api/new_arena',
    headers: {
        'content-type': 'application/x-www-form-urlencoded'
    },
    form: {
       ...
    }
};

var options = {
    method: 'POST',
    url: 'http://localhost:3000/api/new_event',
    headers: {
        'content-type': 'application/x-www-form-urlencoded'
    },
    form: {
       ...
    }
};

request(options, function (error, response, body) {
  if (error) throw new Error(error);

  console.log(body);
});
```

### 3. View Data

GET endpoint route: `/api/...`

### 4. Search Data

Search Field: `name`

### 5. Navigation Pages

Navigation Filters
1. All Arenas -> `/`
2. Arenas in Maryland -> `/arenas_MD`
3. Arenas Sorted by Size -> `/arenas_capacity`
4. Sorted Arenas -> `/arenas_sorted`
5. All Events -> `/all_events`
