# pardot-smalltalk

[Pardot](http://developer.pardot.com/) for Pharo Smalltalk.

# Supported Smalltalk Versions

Pharo Smalltalk 6.0

# Installation

```smalltalk
Metacello new
    baseline: 'Pardot';
    repository: 'github://newapplesho/pardot-smalltalk:v0.1/pharo-repository';
    load.
```

# Usage

## Setup
[official documentation](http://developer.pardot.com/#authentication)
> Obtain the email, password, and user_key (available in Pardot under {your email address} > Settings in the API User Key row) for the Pardot user account that will be submitting API requests.

```smalltalk
PardotSettings initialize.
```


## Authentication

```smalltalk
"print it. 32-character hexadecimal API key will be returned".
PardotLogin new authenticate. 
```

## Prospects

### Upserting Prospects

```smalltalk
PardotProspects new upsertEmail: '<email>'
```

## Visitors

### Assigning and Reassigning Visitors

```smalltalk
PardotVisitor new assignVisitorId: <visitor_id> byProspectId: <prospect_id>.
```