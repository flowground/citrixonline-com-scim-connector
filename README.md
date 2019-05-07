# ![LOGO](logo.png) SCIM **flow**ground Connector

## Description

A generated **flow**ground connector for the SCIM API (version N/A).

Generated from: https://api.apis.guru/v2/specs/citrixonline.com/scim/NA/swagger.json<br/>
Generated at: 2019-05-07T17:39:58+03:00

## API Description

The SCIM API lets you manage users in your organization. You can then automate the provisioning of product licenses for these users, and they can use your company's Single Sign-On solution through an Identity Provider.

## Authorization

This API does not require authorization.

## Actions

### Get Groups

> Queries multiple group identities in the organization domain. Filtering, sorting and pagination are available. This call requires the role ROLE_ORG_READ.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `filter` - _optional_ -  Without a filter, all groups are returned. The filter parameter must be a properly formed SCIM filter using the operator "eq" (equals), "sw" (starts with), or "co" (contains). The filter works for the displayName attribute. Sorting and pagination are supported. For example, GET /Groups?filter=displayName%20eq%20%22Engineering%22&sortBy=displayName&sortOrder=ascending&count=50&startIndex=51

### Create Group

> Creates a new organization group and adds it to the user domain. Member groups and member users must be in the organization. This call requires the role ROLE_ORG_WRITE.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'

### Delete Group

> Deletes a group from the organization (but not from the account). The group must be in the organization. This call requires the role ROLE_ORG_WRITE.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `groupKey` - _required_ - The key of the group to query. The group must be in the organization domain

### Get Group

> Queries group details in the organization domain. This call requires the role ROLE_ORG_READ.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `groupKey` - _required_ - The key of the group to query. The group must be in the organization domain

### Update Group

> Updates one or more values of an existing group without sending the full definition. Member groups and member users must be in the organization. This call requires the role ROLE_ORG_WRITE.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `groupKey` - _required_ - The key of the group to query. The group must be in the organization domain

### Replace Group

> Updates an existing group. The request must include the full group definition. To modify one or more values without sending the full definition, see "Update Group". Member groups and member users must be in the organization. This call requires the role ROLE_ORG_WRITE.

*Tags:* `Groups`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `groupKey` - _required_ - The key of the group to query. The group must be in the organization domain

### Get User Schema

> Queries the user schema. The user schema is defined in SCIM Core Schema (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#resource-schema).

*Tags:* `Schemas`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'

### Get Service Provider Configurations

> Queries service provider configurations. The service provider configurations are defined in SCIM Core Schema (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#anchor6). This call returns a description, a documentationURL, name, and specURL.

*Tags:* `Schemas`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'

### Get Users

> Queries multiple user identities in the organization domain. Filtering is available.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `filter` - _optional_ -  Without a filter, all users in a user domain are returned. The filter parameter must be a properly formed SCIM filter using either the operator eq (equals) or the operator sw (starts with). The filter works for userName, displayName, name.givenName, and name.familyName attributes. For example, /Users?filter=name.familyName%20eq%20%%22Smith%22

### Create User

> Creates a new organization user and adds them to the user domain. The user email domain must match an existing organization email domain.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'

### Get Current User

> Queries the identity of the current authenticated user.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'

### Update Current User

> Changes a limited set (or all if you choose) of the current authenticated user's data. The updated user email domain must be an existing organization email domain.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'

### Replace Current User

> Changes the current authenticated user's displayName, locale, timezone, username and password. The request must include the full user definition (to modify one or more values without sending the full definition, see Update User). The replaced user email domain must be an existing organization email domain.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'

### Delete User

> Deletes a user from the organization (but not from the account).

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `userKey` - _required_ - The key of the user to query. The user must be in the organization domain

### Get User

> Queries user identity in the organization domain.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `userKey` - _required_ - The key of the user to query. The user must be in the organization domain

### Update User

> Changes a limited set (or all if you choose) of the user's data. The updated user email domain must be an existing organization email domain.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `userKey` - _required_ - The key of the user to query. The user must be in the organization domain

### Replace User

> Changes an existing user's displayName, locale, timezone, username and password. The request must include the full user definition (to modify one or more values without sending the full definition, see Update User). The replaced user email domain must be an existing organization email domain.

*Tags:* `Users`

#### Input Parameters
* `Authorization` - _required_ - Access token prefixed with 'Bearer ', e.g. 'Bearer 123456abcdef'
* `userKey` - _required_ - The key of the user to query. The user must be in the organization domain

## License

**flow**ground :- Telekom iPaaS / citrixonline-com-scim-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
