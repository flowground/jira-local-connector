# ![LOGO](logo.png) JIRA 7.6.1 **flow**ground Connector

## Description

A generated **flow**ground connector for the JIRA 7.6.1 API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/jira.local/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:42:34+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### Returns an application property.

#### Input Parameters
* `key` - _optional_ - a String containing the property key
* `permissionLevel` - _optional_ - when fetching a list specifies the permission level of all items in the list
                        see {@link com.atlassian.jira.bc.admin.ApplicationPropertiesService.EditPermissionLevel}
* `keyFilter` - _optional_ - when fetching a list allows the list to be filtered by the property's start of key
                        e.g. "jira.lf.*" whould fetch only those permissions that are editable and whose keys start with
                        "jira.lf.". This is a regex.

### Returns the properties that are displayed on the "General Configuration > Advanced Settings" page.

### Modify an application property via PUT. The "value" field present in the PUT will override the existing value.

#### Input Parameters
* `id` - _required_

### Returns all ApplicationRoles in the system. Will also return an ETag header containing a version hash of the<br/>
>  collection of ApplicationRoles.

### Updates the ApplicationRoles with the passed data if the version hash is the same as the server.<br/>
>  Only the groups and default groups setting of the role may be updated. Requests to change the key<br/>
>  or the name of the role will be silently ignored. It is acceptable to pass only the roles that are updated<br/>
>  as roles that are present in the server but not in data to update with, will not be deleted.

#### Input Parameters
* `If-Match` - _optional_

### Returns the ApplicationRole with passed key if it exists.

#### Input Parameters
* `key` - _required_ - the key of the role to update.

### Updates the ApplicationRole with the passed data. Only the groups and default groups setting of the<br/>
>  role may be updated. Requests to change the key or the name of the role will be silently ignored.<br/>
>  <p><br/>
>  Optional: If versionHash is passed through the If-Match header the request will be rejected if not the<br/>
>  same as server

#### Input Parameters
* `If-Match` - _optional_ - the hash of the version to update. Optional Param

### Returns the meta information for an attachments, specifically if they are enabled and the maximum upload size<br/>
>  allowed.

### Remove an attachment from an issue.

#### Input Parameters
* `id` - _required_ - id of the attachment to remove

### Returns the meta-data for an attachment, including the URI of the actual attached file.

#### Input Parameters
* `id` - _required_ - id of the attachment to remove

### Tries to expand an attachment. Output is human-readable and subject to change.

#### Input Parameters
* `id` - _required_ - the id of the attachment to expand.

### Tries to expand an attachment. Output is raw and should be backwards-compatible through the course of time.

#### Input Parameters
* `id` - _required_ - the id of the attachment to expand.

### Returns auditing records filtered using provided parameters

#### Input Parameters
* `offset` - _optional_ - - the number of record from which search starts
* `limit` - _optional_ - - maximum number of returned results (if is limit is <= 0 or > 1000, it will be set do default value: 1000)
* `filter` - _optional_ - - text query; each record that will be returned must contain the provided text in one of its fields
* `from` - _optional_ - - timestamp in past; 'from' must be less or equal 'to', otherwise the result set will be empty
               only records that where created in the same moment or after the 'from' timestamp will be provided in response
* `to` - _optional_ - - timestamp in past; 'from' must be less or equal 'to', otherwise the result set will be empty
               only records that where created in the same moment or earlier than the 'to' timestamp will be provided in response
* `projectIds` - _optional_ - - list of project ids to look for
* `userIds` - _optional_ - - list of user ids to look for

### Store a record in Audit Log

### Returns all system avatars of the given type.

#### Input Parameters
* `type` - _required_ - the avatar type

### Creates temporary avatar

#### Input Parameters
* `filename` - _optional_ - name of file being uploaded
* `size` - _optional_ - size of file

### Updates the cropping instructions of the temporary avatar.

#### Input Parameters
* `type` - _required_ - the avatar type

### approveUpgrade

### cancelUpgrade

### acknowledgeErrors

### setReadyToUpgrade

### getState

### Returns the keys of all properties for the comment identified by the key or by the id.

#### Input Parameters
* `commentId` - _required_ - the comment from which keys will be returned.

### Removes the property from the comment identified by the key or by the id. Ths user removing the property is required<br/>
>  to have permissions to administer the comment.

#### Input Parameters
* `commentId` - _required_ - the comment from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Returns the value of the property with a given key from the comment identified by the key or by the id. The user who retrieves<br/>
>  the property is required to have permissions to read the comment.

#### Input Parameters
* `commentId` - _required_ - the comment from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Sets the value of the specified comment's property.<br/>
>  <p><br/>
>  You can use this resource to store a custom data against the comment identified by the key or by the id. The user<br/>
>  who stores the data is required to have permissions to administer the comment.<br/>
>  </p>

#### Input Parameters
* `commentId` - _required_ - the comment from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Create a component via POST.

### Delete a project component.

#### Input Parameters
* `moveIssuesTo` - _optional_ - The new component applied to issues whose 'id' component will be deleted.
                     If this value is null, then the 'id' component is simply removed from the related isues.

### Returns a project component.

#### Input Parameters
* `id` - _required_ - The component to delete.

### Modify a component via PUT. Any fields present in the PUT will override existing values. As a convenience, if a field<br/>
>  is not present, it is silently ignored.<br/>
>  <p><br/>
>  If leadUserName is an empty string ("") the component lead will be removed.

#### Input Parameters
* `id` - _required_ - The component to delete.

### Returns counts of issues related to this component.

#### Input Parameters
* `id` - _required_ - a String containing the component id

### Returns the information if the optional features in JIRA are enabled or disabled. If the time tracking is enabled,<br/>
>  it also returns the detailed information about time tracking configuration.

### Returns a full representation of the Custom Field Option that has the given id.

#### Input Parameters
* `id` - _required_ - a String containing an Custom Field Option id

### Returns a list of all dashboards, optionally filtering them.

#### Input Parameters
* `filter` - _optional_ - an optional filter that is applied to the list of dashboards. Valid values include
                        <code>"favourite"</code> for returning only favourite dashboards, and <code>"my"</code> for returning
                        dashboards that are owned by the calling user.
* `startAt` - _optional_ - the index of the first dashboard to return (0-based). must be 0 or a multiple of
                        <code>maxResults</code>
* `maxResults` - _optional_ - a hint as to the the maximum number of dashboards to return in each call. Note that the
                        JIRA server reserves the right to impose a <code>maxResults</code> limit that is lower than the value that a
                        client provides, dues to lack or resources or any other condition. When this happens, your results will be
                        truncated. Callers should always check the returned <code>maxResults</code> to determine the value that is
                        effectively being used.

### Returns the keys of all properties for the dashboard item identified by the id.

#### Input Parameters
* `itemId` - _required_ - the dashboard item from which keys will be returned.
* `dashboardId` - _required_

### Removes the property from the dashboard item identified by the key or by the id. Ths user removing the property is required<br/>
>  to have permissions to administer the dashboard item.

#### Input Parameters
* `itemId` - _required_ - the dashboard item from which keys will be returned.
* `dashboardId` - _required_
* `propertyKey` - _required_ - the key of the property to return.

### Returns the value of the property with a given key from the dashboard item identified by the id.<br/>
>  The user who retrieves the property is required to have permissions to read the dashboard item.

#### Input Parameters
* `itemId` - _required_ - the dashboard item from which keys will be returned.
* `dashboardId` - _required_
* `propertyKey` - _required_ - the key of the property to return.

### Sets the value of the specified dashboard item's property.<br/>
>  <p><br/>
>  You can use this resource to store a custom data against the dashboard item identified by the id.<br/>
>  The user who stores the data is required to have permissions to administer the dashboard item.<br/>
>  </p>

#### Input Parameters
* `itemId` - _required_ - the dashboard item from which keys will be returned.
* `dashboardId` - _required_
* `propertyKey` - _required_ - the key of the property to return.

### Returns a single dashboard.

#### Input Parameters
* `id` - _required_ - the dashboard id

### Returns a list of all fields, both System and Custom

### Creates a custom field using a definition (object encapsulating custom field data)

### Creates a new filter, and returns newly created filter.<br/>
>  Currently sets permissions just using the users default sharing permissions

#### Input Parameters
* `expand` - _optional_ - the parameters to expand

### Returns the default share scope of the logged-in user.

### Sets the default share scope of the logged-in user. Available values are GLOBAL and PRIVATE.

### Returns the favourite filters of the logged-in user.

#### Input Parameters
* `expand` - _optional_ - the parameters to expand
* `enableSharedUsers` - _optional_ - enable calculating shared users collection

### Delete a filter.

#### Input Parameters
* `id` - _required_ - the id of the filter being looked up

### Returns a filter given an id

#### Input Parameters
* `expand` - _optional_ - the parameters to expand
* `enableSharedUsers` - _optional_ - enable calculating shared users collection

### Updates an existing filter, and returns its new value.

#### Input Parameters
* `expand` - _optional_ - the parameters to expand

### Resets the columns for the given filter such that the filter no longer has its own column config.

#### Input Parameters
* `id` - _required_ - id of the filter

### Returns the default columns for the given filter. Currently logged in user will be used as<br/>
>  the user making such request.

#### Input Parameters
* `id` - _required_ - id of the filter

### Sets the default columns for the given filter.

#### Input Parameters
* `id` - _required_ - id of the filter

### Returns all share permissions of the given filter.

#### Input Parameters
* `id` - _required_

### Adds a share permissions to the given filter. Adding a global permission removes all previous permissions from the filter.

#### Input Parameters
* `id` - _required_

### Removes a share permissions from the given filter.

#### Input Parameters
* `id` - _required_
* `permission-id` - _required_

### Returns a single share permission of the given filter.

#### Input Parameters
* `permissionId` - _required_
* `id` - _required_

### Deletes a group by given group parameter.<br/>
>  <p><br/>
>  Returns no content

#### Input Parameters
* `groupname` - _optional_ - (mandatory) The name of the group to delete.
* `swapGroup` - _optional_ - If you delete a group and content is restricted to that group, the content will be hidden from all users. 
 To prevent this, use this parameter to specify a different group to transfer the restrictions (comments and worklogs only) to.

### Returns REST representation for the requested group. Allows to get list of active users belonging to the<br/>
>  specified group and its subgroups if "users" expand option is provided. You can page through users list by using<br/>
>  indexes in expand param. For example to get users from index 10 to index 15 use "users[10:15]" expand value. This<br/>
>  will return 6 users (if there are at least 16 users in this group). Indexes are 0-based and inclusive.<br/>
>  <p><br/>
>  This resource is deprecated, please use group/member API instead.

#### Input Parameters
* `groupname` - _optional_ - A name of requested group.
* `expand` - _optional_ - List of fields to expand. Currently only available expand is "users".

### Creates a group by given group parameter<br/>
>  <p><br/>
>  Returns REST representation for the requested group.

### This resource returns a <a href="#pagination">paginated</a> list of users who are members of the specified group and its subgroups.<br/>
>  Users in the page are ordered by user names. User of this resource is required to have sysadmin or admin permissions.

#### Input Parameters
* `groupname` - _optional_ - a name of the group for which members will be returned.
* `includeInactiveUsers` - _optional_ - inactive users will be included in the response if set to true.
* `startAt` - _optional_ - the index of the first user in group to return (0 based).
* `maxResults` - _optional_ - the maximum number of users to return (max 50).

### Removes given user from a group.<br/>
>  <p><br/>
>  Returns no content

#### Input Parameters
* `groupname` - _optional_ - A name of requested group.
* `username` - _optional_ - User to remove from a group

### Adds given user to a group.<br/>
>  <p><br/>
>  Returns the current state of the group.

#### Input Parameters
* `groupname` - _optional_ - A name of requested group.

### Returns groups with substrings matching a given query. This is mainly for use with<br/>
>  the group picker, so the returned groups contain html to be used as picker suggestions.<br/>
>  The groups are also wrapped in a single response object that also contains a header for<br/>
>  use in the picker, specifically <i>Showing X of Y matching groups</i>.<br/>
>  <p><br/>
>  The number of groups returned is limited by the system property "jira.ajax.autocomplete.limit"<br/>
>  <p><br/>
>  The groups will be unique and sorted.

#### Input Parameters
* `query` - _optional_ - a String to match groups agains
* `exclude` - _optional_
* `maxResults` - _optional_
* `userName` - _optional_

### Returns a list of users and groups matching query with highlighting. This resource cannot be accessed<br/>
>  anonymously.

#### Input Parameters
* `query` - _optional_ - A string used to search username, Name or e-mail address
* `maxResults` - _optional_ - the maximum number of users to return (defaults to 50). The maximum allowed value is 1000. If
                    you specify a value that is higher than this number, your search results will be truncated.
* `showAvatar` - _optional_
* `fieldId` - _optional_ - The custom field id, if this request comes from a custom field, such as a user picker. Optional.
* `projectId` - _optional_ - The list of project ids to further restrict the search
                    This parameter can occur multiple times to pass in multiple project ids.
                    Comma separated value is not supported.
                    This parameter is only used when fieldId is present.
* `issueTypeId` - _optional_ - The list of issue type ids to further restrict the search.
                    This parameter can occur multiple times to pass in multiple issue type ids.
                    Comma separated value is not supported.
                    Special values such as -1 (all standard issue types), -2 (all subtask issue types) are supported.
                    This parameter is only used when fieldId is present.

### Summarizes index condition of current node.<br/>
>  <p/><br/>
>  Returned data consists of:<br/>
>  <ul><br/>
>  <li><code>nodeId</code> - Node identifier.</li><br/>
>  <li><code>reportTime</code> - Time of this report creation.</li><br/>
>  <li><code>issueIndex</code> - Summary of issue index status.</li><br/>
>  <li><code>replicationQueues</code> - Map of index replication queues, where<br/>
>  keys represent nodes from which replication operations came from.</li><br/>
>  </ul><br/>
>  <p/><br/>
>  <code>issueIndex</code> can contain:<br/>
>  <ul><br/>
>  <li><code>indexReadable</code> - If <code>false</code> the end point failed to read data from issue index<br/>
>  (check JIRA logs for detailed stack trace), otherwise <code>true</code>.<br/>
>  When <code>false</code> other fields of <code>issueIndex</code> can be not visible.</li><br/>
>  <li><code>countInDatabase</code> - Count of issues found in database.</li><br/>
>  <li><code>countInIndex</code> - Count of issues found while querying index.</li><br/>
>  <li><code>lastUpdatedInDatabase</code> - Time of last update of issue found in database.</li><br/>
>  <li><code>lastUpdatedInIndex</code> - Time of last update of issue found while querying index.</li><br/>
>  </ul><br/>
>  <p/><br/>
>  <code>replicationQueues</code>'s map values can contain:<br/>
>  <ul><br/>
>  <li><code>lastConsumedOperation</code> - Last executed index replication operation by current node from sending node's queue.</li><br/>
>  <li><code>lastConsumedOperation.id</code> - Identifier of the operation.</li><br/>
>  <li><code>lastConsumedOperation.replicationTime</code> - Time when the operation was sent to other nodes.</li><br/>
>  <li><code>lastOperationInQueue</code> - Last index replication operation in sending node's queue.</li><br/>
>  <li><code>lastOperationInQueue.id</code> - Identifier of the operation.</li><br/>
>  <li><code>lastOperationInQueue.replicationTime</code> - Time when the operation was sent to other nodes.</li><br/>
>  <li><code>queueSize</code> - Number of operations in queue from sending node to current node.</li><br/>
>  </ul>

### Creates an issue or a sub-task from a JSON representation.<br/>
>  <p/><br/>
>  The fields that can be set on create, in either the fields parameter or the update parameter can be determined<br/>
>  using the <b>/rest/api/2/issue/createmeta</b> resource.<br/>
>  If a field is not configured to appear on the create screen, then it will not be in the createmeta, and a field<br/>
>  validation error will occur if it is submitted.<br/>
>  <p/><br/>
>  Creating a sub-task is similar to creating a regular issue, with two important differences:<br/>
>  <ul><br/>
>  <li>the <code>issueType</code> field must correspond to a sub-task issue type (you can use<br/>
>  <code>/issue/createmeta</code> to discover sub-task issue types), and</li><br/>
>  <li>you must provide a <code>parent</code> field in the issue create request containing the id or key of the<br/>
>  parent issue.</li><br/>
>  </ul>

### Creates issues or sub-tasks from a JSON representation.<br/>
>  <p/><br/>
>  Creates many issues in one bulk operation.<br/>
>  <p/><br/>
>  Creating a sub-task is similar to creating a regular issue. More details can be found in createIssue section:<br/>
>  {@link IssueResource#createIssue(IssueUpdateBean)}}

### Returns the meta data for creating issues. This includes the available projects, issue types and fields,<br/>
>  including field types and whether or not those fields are required.<br/>
>  Projects will not be returned if the user does not have permission to create issues in that project.<br/>
>  <p/><br/>
>  The fields in the createmeta correspond to the fields in the create screen for the project/issuetype.<br/>
>  Fields not in the screen will not be in the createmeta.<br/>
>  <p/><br/>
>  Fields will only be returned if <code>expand=projects.issuetypes.fields</code>.<br/>
>  <p/><br/>
>  The results can be filtered by project and/or issue type, given by the query params.

#### Input Parameters
* `projectIds` - _optional_ - combined with the projectKeys param, lists the projects with which to filter the results. If absent, all projects are returned.
                       This parameter can be specified multiple times, and/or be a comma-separated list.
                       Specifiying a project that does not exist (or that you cannot create issues in) is not an error, but it will not be in the results.
* `projectKeys` - _optional_ - combined with the projectIds param, lists the projects with which to filter the results. If null, all projects are returned.
                       This parameter can be specified multiple times, and/or be a comma-separated list.
                       Specifiying a project that does not exist (or that you cannot create issues in) is not an error, but it will not be in the results.
* `issuetypeIds` - _optional_ - combinded with issuetypeNames, lists the issue types with which to filter the results. If null, all issue types are returned.
                       This parameter can be specified multiple times, and/or be a comma-separated list.
                       Specifiying an issue type that does not exist is not an error.
* `issuetypeNames` - _optional_ - combinded with issuetypeIds, lists the issue types with which to filter the results. If null, all issue types are returned.
                       This parameter can be specified multiple times, but is NOT interpreted as a comma-separated list.
                       Specifiying an issue type that does not exist is not an error.

### Returns suggested issues which match the auto-completion query for the user which executes this request. This REST<br/>
>  method will check the user's history and the user's browsing context and select this issues, which match the query.

#### Input Parameters
* `query` - _optional_ - the query.
* `currentJQL` - _optional_ - the JQL in context of which the request is executed. Only issues which match this JQL query will be included in results.
* `currentIssueKey` - _optional_ - the key of the issue in context of which the request is executed. The issue which is in context will not be included in the auto-completion result, even if it matches the query.
* `currentProjectId` - _optional_ - the id of the project in context of which the request is executed. Suggested issues will be only from this project.
* `showSubTasks` - _optional_ - if set to false, subtasks will not be included in the list.
* `showSubTaskParent` - _optional_ - if set to false and request is executed in context of a subtask, the parent issue will not be included in the auto-completion result, even if it matches the query.

### Delete an issue.<br/>
>  <p/><br/>
>  If the issue has subtasks you must set the parameter deleteSubtasks=true to delete the issue.<br/>
>  You cannot delete an issue without its subtasks also being deleted.

#### Input Parameters
* `deleteSubtasks` - _optional_ - a String of true or false indicating that any subtasks should also be deleted.  If the
                       issue has no subtasks this parameter is ignored.  If the issue has subtasks and this parameter is missing or false,
                       then the issue will not be deleted and an error will be returned.

### Returns a full representation of the issue for the given issue key.<br/>
>  <p><br/>
>  An issue JSON consists of the issue key, a collection of fields,<br/>
>  a link to the workflow transition sub-resource, and (optionally) the HTML rendered values of any fields that support it<br/>
>  (e.g. if wiki syntax is enabled for the description or comments).<br/>
>  <p><br/>
>  The <code>fields</code> param (which can be specified multiple times) gives a comma-separated list of fields<br/>
>  to include in the response. This can be used to retrieve a subset of fields.<br/>
>  A particular field can be excluded by prefixing it with a minus.<br/>
>  <p><br/>
>  By default, all (<code>*all</code>) fields are returned in this get-issue resource. Note: the default is different<br/>
>  when doing a jql search -- the default there is just navigable fields (<code>*navigable</code>).<br/>
>  <ul><br/>
>  <li><code>*all</code> - include all fields</li><br/>
>  <li><code>*navigable</code> - include just navigable fields</li><br/>
>  <li><code>summary,comment</code> - include just the summary and comments</li><br/>
>  <li><code>-comment</code> - include everything except comments (the default is <code>*all</code> for get-issue)</li><br/>
>  <li><code>*all,-comment</code> - include everything except comments</li><br/>
>  </ul><br/>
>  <p><br/>
>  The {@code properties} param is similar to {@code fields} and specifies a comma-separated list of issue<br/>
>  properties to include. Unlike {@code fields}, properties are not included by default. To include them all<br/>
>  send {@code ?properties=*all}. You can also include only specified properties or exclude some properties<br/>
>  with a minus (-) sign.<br/>
>  <p><br/>
>  <ul><br/>
>  <li>{@code *all} - include all properties</li><br/>
>  <li>{@code *all, -prop1} - include all properties except {@code prop1} </li><br/>
>  <li>{@code prop1, prop1} - include {@code prop1} and {@code prop2} properties </li><br/>
>  </ul><br/>
>  </p><br/>
>  <p/><br/>
>  JIRA will attempt to identify the issue by the <code>issueIdOrKey</code> path parameter. This can be an issue id,<br/>
>  or an issue key. If the issue cannot be found via an exact match, JIRA will also look for the issue in a case-insensitive way, or<br/>
>  by looking to see if the issue was moved. In either of these cases, the request will proceed as normal (a 302 or other redirect<br/>
>  will <b>not</b> be returned). The issue key contained in the response will indicate the current value of issue's key.<br/>
>  <p/><br/>
>  The <code>expand</code> param is used to include, hidden by default, parts of response. This can be used to include:<br/>
>  <ul><br/>
>  <li><code>renderedFields</code> - field values in HTML format</li><br/>
>  <li><code>names</code> - display name of each field</li><br/>
>  <li><code>schema</code> - schema for each field which describes a type of the field</li><br/>
>  <li><code>transitions</code> - all possible transitions for the given issue</li><br/>
>  <li><code>operations</code> - all possibles operations which may be applied on issue</li><br/>
>  <li><code>editmeta</code> - information about how each field may be edited. It contains field's schema as well.</li><br/>
>  <li><code>changelog</code> - history of all changes of the given issue</li><br/>
>  <li><code>versionedRepresentations</code> -<br/>
>  REST representations of all fields. Some field may contain more recent versions. RESET representations are numbered.<br/>
>  The greatest number always represents the most recent version. It is recommended that the most recent version is used.<br/>
>  version for these fields which provide a more recent REST representation.<br/>
>  After including <code>versionedRepresentations</code> "fields" field become hidden.</li><br/>
>  </ul>

#### Input Parameters
* `fields` - _optional_ - the list of fields to return for the issue. By default, all fields are returned.
* `expand` - _optional_
* `properties` - _optional_ - the list of properties to return for the issue. By default no properties are returned.

### Edits an issue from a JSON representation.<br/>
>  <p/><br/>
>  The issue can either be updated by setting explicit the field value(s)<br/>
>  or by using an operation to change the field value.<br/>
>  <p/><br/>
>  The fields that can be updated, in either the fields parameter or the update parameter, can be determined<br/>
>  using the <b>/rest/api/2/issue/{issueIdOrKey}/editmeta</b> resource.<br><br/>
>  If a field is not configured to appear on the edit screen, then it will not be in the editmeta, and a field<br/>
>  validation error will occur if it is submitted.<br/>
>  <p/><br/>
>  Specifying a "field_id": field_value in the "fields" is a shorthand for a "set" operation in the "update" section.<br><br/>
>  Field should appear either in "fields" or "update", not in both.

#### Input Parameters
* `notifyUsers` - _optional_ - send the email with notification that the issue was updated to users that watch it.
                    Admin or project admin permissions are required to disable the notification.

### Assigns an issue to a user.<br/>
>  You can use this resource to assign issues when the user submitting the request has the assign permission but not the<br/>
>  edit issue permission.<br/>
>  If the name is "-1" automatic assignee is used.  A null name will remove the assignee.

#### Input Parameters
* `issueIdOrKey` - _required_ - a String containing an issue key

### Add one or more attachments to an issue.<br/>
>  <p><br/>
>  This resource expects a multipart post. The media-type multipart/form-data is defined in RFC 1867. Most client<br/>
>  libraries have classes that make dealing with multipart posts simple. For instance, in Java the Apache HTTP Components<br/>
>  library provides a<br/>
>  <a href="http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html">MultiPartEntity</a><br/>
>  that makes it simple to submit a multipart POST.<br/>
>  <p><br/>
>  In order to protect against XSRF attacks, because this method accepts multipart/form-data, it has XSRF protection<br/>
>  on it.  This means you must submit a header of X-Atlassian-Token: no-check with the request, otherwise it will be<br/>
>  blocked.<br/>
>  <p><br/>
>  The name of the multipart/form-data parameter that contains attachments must be "file"<br/>
>  <p><br/>
>  A simple example to upload a file called "myfile.txt" to issue REST-123:<br/>
>  <pre>curl -D- -u admin:admin -X POST -H "X-Atlassian-Token: no-check" -F "file=@myfile.txt" http://myhost/rest/api/2/issue/TEST-123/attachments</pre>

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue that you want to add the attachments to

### Returns all comments for an issue.<br/>
>  <p><br/>
>  Results can be ordered by the "created" field which means the date a comment was added.<br/>
>  </p>

#### Input Parameters
* `startAt` - _optional_ - the page offset, if not specified then defaults to 0
* `maxResults` - _optional_ - how many results on the page should be included. Defaults to 50.
* `orderBy` - _optional_ - ordering of the results.
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)

### Adds a new comment to an issue.

#### Input Parameters
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)

### Deletes an existing comment .

#### Input Parameters
* `issueIdOrKey` - _required_ - of the issue the comment belongs to
* `id` - _required_ - the ID of the comment to request

### Returns a single comment.

#### Input Parameters
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)
* `id` - _required_ - the ID of the comment to request

### Updates an existing comment using its JSON representation.

#### Input Parameters
* `expand` - _optional_ - optional flags: renderedBody (provides body rendered in HTML)
* `id` - _required_ - the ID of the comment to request

### Returns the meta data for editing an issue.<br/>
>  <p/><br/>
>  The fields in the editmeta correspond to the fields in the edit screen for the issue.<br/>
>  Fields not in the screen will not be in the editmeta.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue whose edit meta data you want to view

### Sends a notification (email) to the list or recipients defined in the request.

#### Input Parameters
* `issueIdOrKey` - _required_ - a string containing the issue id or key the comment will be added to

### Returns the keys of all properties for the issue identified by the key or by the id.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue from which keys will be returned.

### Removes the property from the issue identified by the key or by the id. Ths user removing the property is required<br/>
>  to have permissions to edit the issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Returns the value of the property with a given key from the issue identified by the key or by the id. The user who retrieves<br/>
>  the property is required to have permissions to read the issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Sets the value of the specified issue's property.<br/>
>  <p><br/>
>  You can use this resource to store a custom data against the issue identified by the key or by the id. The user<br/>
>  who stores the data is required to have permissions to edit the issue.<br/>
>  </p>

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Delete the remote issue link with the given global id on the issue.

#### Input Parameters
* `globalId` - _optional_ - the global id of the remote issue link

### A REST sub-resource representing the remote issue links on the issue.

#### Input Parameters
* `globalId` - _optional_ - The id of the remote issue link to be returned.  If null (not provided) all remote links for the
                     issue are returned.
                     <p>For a fullexplanation of Issue Link fields please refer to
                     <a href="https://developer.atlassian.com/display/JIRADEV/Fields+in+Remote+Issue+Links">https://developer.atlassian.com/display/JIRADEV/Fields+in+Remote+Issue+Links</a></p>

### Creates or updates a remote issue link from a JSON representation. If a globalId is provided and a remote issue link<br/>
>  exists with that globalId, the remote issue link is updated. Otherwise, the remote issue link is created.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue to create the remote issue link for

### Delete the remote issue link with the given id on the issue.

#### Input Parameters
* `linkId` - _required_ - the id of the remote issue link
* `issueIdOrKey` - _required_ - the issue to create the remote issue link for

### Get the remote issue link with the given id on the issue.

#### Input Parameters
* `linkId` - _required_ - the id of the remote issue link
* `issueIdOrKey` - _required_ - the issue to create the remote issue link for

### Updates a remote issue link from a JSON representation. Any fields not provided are set to null.

#### Input Parameters
* `linkId` - _required_ - the id of the remote issue link
* `issueIdOrKey` - _required_ - the issue to create the remote issue link for

### Returns an issue's subtask list

#### Input Parameters
* `issueIdOrKey` - _required_ - The parent issue's key or id

### canMoveSubTask

#### Input Parameters
* `issueIdOrKey` - _required_ - The parent issue's key or id

### Reorders an issue's subtasks by moving the subtask at index "from"<br/>
>  to index "to".

#### Input Parameters
* `issueIdOrKey` - _required_ - The parent issue's key or id

### Get a list of the transitions possible for this issue by the current user, along with fields that are required and their types.<br/>
>  <p/><br/>
>  Fields will only be returned if <code>expand=transitions.fields</code>.<br/>
>  <p/><br/>
>  The fields in the metadata correspond to the fields in the transition screen for that transition.<br/>
>  Fields not in the screen will not be in the metadata.

#### Input Parameters
* `transitionId` - _optional_

### Perform a transition on an issue.<br/>
>  When performing the transition you can update or set other issue fields.<br/>
>  <p/><br/>
>  The fields that can be set on transtion, in either the fields parameter or the update parameter can be determined<br/>
>  using the <b>/rest/api/2/issue/{issueIdOrKey}/transitions?expand=transitions.fields</b> resource.<br/>
>  If a field is not configured to appear on the transition screen, then it will not be in the transition metadata, and a field<br/>
>  validation error will occur if it is submitted.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue whose transitions you want to view

### Remove your vote from an issue. (i.e. "unvote")

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue to view voting information for

### A REST sub-resource representing the voters on the issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue to view voting information for

### Cast your vote in favour of an issue.

#### Input Parameters
* `issueIdOrKey` - _required_ - the issue to view voting information for

### Removes a user from an issue's watcher list.

#### Input Parameters
* `username` - _optional_ - a String containing the name of the user to remove from the watcher list. Must not be null.

### Returns the list of watchers for the issue with the given key.

#### Input Parameters
* `issueIdOrKey` - _required_ - a String containing an issue key.

### Adds a user to an issue's watcher list.

#### Input Parameters
* `issueIdOrKey` - _required_ - a String containing an issue key.

### Returns all work logs for an issue. <br/><br/>
>  <strong>Note:</strong> Work logs won't be returned if the Log work field is hidden for the project.

#### Input Parameters
* `issueIdOrKey` - _required_ - a string containing the issue id or key the worklog will be added to

### Adds a new worklog entry to an issue.

#### Input Parameters
* `adjustEstimate` - _optional_ - (optional) allows you to provide specific instructions to update the remaining time estimate of the issue.  Valid values are
                       <ul>
                       <li>"new" - sets the estimate to a specific value</li>
                       <li>"leave"- leaves the estimate as is</li>
                       <li>"manual" - specify a specific amount to increase remaining estimate by</li>
                       <li>"auto"- Default option.  Will automatically adjust the value based on the new timeSpent specified on the worklog</li> </ul>
* `newEstimate` - _optional_ - (required when "new" is selected for adjustEstimate) the new value for the remaining estimate field. e.g. "2d"
* `reduceBy` - _optional_ - (required when "manual" is selected for adjustEstimate) the amount to reduce the remaining estimate by e.g. "2d"

### Deletes an existing worklog entry.

#### Input Parameters
* `adjustEstimate` - _optional_ - (optional) allows you to provide specific instructions to update the remaining time estimate of the issue.  Valid values are
                       <ul>
                       <li>"new" - sets the estimate to a specific value</li>
                       <li>"leave"- leaves the estimate as is</li>
                       <li>"manual" - specify a specific amount to increase remaining estimate by</li>
                       <li>"auto"- Default option.  Will automatically adjust the value based on the new timeSpent specified on the worklog</li> </ul>
* `newEstimate` - _optional_ - (required when "new" is selected for adjustEstimate) the new value for the remaining estimate field. e.g. "2d"
* `increaseBy` - _optional_ - (required when "manual" is selected for adjustEstimate) the amount to increase the remaining estimate by e.g. "2d"

### Returns a specific worklog. <br/><br/>
>  <strong>Note:</strong> The work log won't be returned if the Log work field is hidden for the project.

#### Input Parameters
* `issueIdOrKey` - _required_ - a string containing the issue id or key the worklog belongs to
* `id` - _required_ - id of the worklog to be deleted

### Updates an existing worklog entry.<br/>
>  <p>Note that:</p><br/>
>   <ul><br/>
>       <li>Fields possible for editing are: comment, visibility, started, timeSpent and timeSpentSeconds.</li><br/>
>       <li>Either timeSpent or timeSpentSeconds can be set.</li><br/>
>       <li>Fields which are not set will not be updated.</li><br/>
>       <li>For a request to be valid, it has to have at least one field change.</li><br/>
>   </ul>

#### Input Parameters
* `adjustEstimate` - _optional_ - (optional) allows you to provide specific instructions to update the remaining time estimate of the issue.  Valid values are
                       <ul>
                       <li>"new" - sets the estimate to a specific value</li>
                       <li>"leave"- leaves the estimate as is</li>
                       <li>"auto"- Default option.  Will automatically adjust the value based on the new timeSpent specified on the worklog</li> </ul>
* `newEstimate` - _optional_ - (required when "new" is selected for adjustEstimate) the new value for the remaining estimate field.

### Creates an issue link between two issues.<br/>
>  The user requires the link issue permission for the issue which will be linked to another issue.<br/>
>  The specified link type in the request is used to create the link and will create a link from the first issue<br/>
>  to the second issue using the outward description. It also create a link from the second issue to the first issue using the<br/>
>  inward description of the issue link type.<br/>
>  It will add the supplied comment to the first issue. The comment can have a restriction who can view it.<br/>
>  If group is specified, only users of this group can view this comment, if roleLevel is specified only users who have the specified role can view this comment.<br/>
>  The user who creates the issue link needs to belong to the specified group or have the specified role.

### Deletes an issue link with the specified id.<br/>
>  To be able to delete an issue link you must be able to view both issues and must have the link issue permission<br/>
>  for at least one of the issues.

#### Input Parameters
* `linkId` - _required_ - the issue link id.

### Returns an issue link with the specified id.

#### Input Parameters
* `linkId` - _required_ - the issue link id.

### Returns a list of available issue link types, if issue linking is enabled.<br/>
>  Each issue link type has an id, a name and a label for the outward and inward link relationship.

### Create a new issue link type.

### Delete the specified issue link type.

#### Input Parameters
* `issueLinkTypeId` - _required_

### Returns for a given issue link type id all information about this issue link type.

#### Input Parameters
* `issueLinkTypeId` - _required_

### Update the specified issue link type.

#### Input Parameters
* `issueLinkTypeId` - _required_

### Returns all issue security schemes that are defined.

### Returns the issue security scheme along with that are defined.

#### Input Parameters
* `id` - _required_

### Returns a list of all issue types visible to the user

### Creates an issue type from a JSON representation and adds the issue newly created issue type to the default issue<br/>
>  type scheme.

### Deletes the specified issue type. If the issue type has any associated issues, these issues will be migrated to<br/>
>  the alternative issue type specified in the parameter. You can determine the alternative issue types by calling<br/>
>  the <b>/rest/api/2/issuetype/{id}/alternatives</b> resource.

#### Input Parameters
* `alternativeIssueTypeId` - _optional_ - the id of an issue type to which issues associated with the removed issue type will be migrated.

### Returns a full representation of the issue type that has the given id.

#### Input Parameters
* `id` - _required_ - the id of the issue type to update.

### Updates the specified issue type from a JSON representation.

#### Input Parameters
* `id` - _required_ - the id of the issue type to update.

### Returns a list of all alternative issue types for the given issue type id. The list will contain these issues types, to which<br/>
>  issues assigned to the given issue type can be migrated. The suitable alternatives are issue types which are assigned<br/>
>  to the same workflow, the same field configuration and the same screen scheme.

#### Input Parameters
* `id` - _required_

### Converts temporary avatar into a real avatar

#### Input Parameters
* `id` - _required_ - the id of the issue type, which avatar is updated.

### Creates temporary avatar using multipart. The response is sent back as JSON stored in a textarea. This is because<br/>
>  the client uses remote iframing to submit avatars using multipart. So we must send them a valid HTML page back from<br/>
>  which the client parses the JSON from.<br/>
>  <p><br/>
>  Creating a temporary avatar is part of a 3-step process in uploading a new<br/>
>  avatar for an issue type: upload, crop, confirm. This endpoint allows you to use a multipart upload<br/>
>  instead of sending the image directly as the request body.<br/>
>  </p><br/>
>  <p><br/>
>  You *must* use "avatar" as the name of the upload parameter:</p><br/>
>  <p><br/>
>  <pre><br/>
>  curl -c cookiejar.txt -X POST -u admin:admin -H "X-Atlassian-Token: no-check" \<br/>
>    -F "avatar=@mynewavatar.png;type=image/png" \<br/>
>    'http://localhost:8090/jira/rest/api/2/issuetype/1/avatar/temporary'<br/>
>  </pre>

#### Input Parameters
* `id` - _required_ - the id of the issue type, which avatar is updated.

### Returns the keys of all properties for the issue type identified by the id.

#### Input Parameters
* `issueTypeId` - _required_ - the issue type from which the keys will be returned

### Removes the property from the issue type identified by the id. Ths user removing the property is required<br/>
>  to have permissions to edit the issue type.

#### Input Parameters
* `issueTypeId` - _required_ - the issue type from which the keys will be returned
* `propertyKey` - _required_ - the key of the property to return

### Returns the value of the property with a given key from the issue type identified by the id. The user who retrieves<br/>
>  the property is required to have permissions to view the issue type.

#### Input Parameters
* `issueTypeId` - _required_ - the issue type from which the keys will be returned
* `propertyKey` - _required_ - the key of the property to return

### Sets the value of the specified issue type's property.<br/>
>  <p><br/>
>  You can use this resource to store a custom data against an issue type identified by the id. The user<br/>
>  who stores the data is required to have permissions to edit an issue type.<br/>
>  </p>

#### Input Parameters
* `issueTypeId` - _required_ - the issue type from which the keys will be returned
* `propertyKey` - _required_ - the key of the property to return

### Returns the auto complete data required for JQL searches.

### Returns auto complete suggestions for JQL search.

#### Input Parameters
* `fieldName` - _optional_ - the field name for which the suggestions are generated.
* `fieldValue` - _optional_ - the portion of the field value that has already been provided by the user.
* `predicateName` - _optional_ - the predicate for which the suggestions are generated. Suggestions are generated only for: "by", "from" and "to".
* `predicateValue` - _optional_ - the portion of the predicate value that has already been provided by the user.

### validate

### areMetricsExposed

### getAvailableMetrics

### start

### stop

### Returns all permissions in the system and whether the currently logged in user has them. You can optionally provide a specific context to get permissions for<br/>
>  (projectKey OR projectId OR issueKey OR issueId)<br/>
>  <ul><br/>
>  <li> When no context supplied the project related permissions will return true if the user has that permission in ANY project </li><br/>
>  <li> If a project context is provided, project related permissions will return true if the user has the permissions in the specified project.<br/>
>  For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project </li><br/>
>  <li> If an issue context is provided, it will return whether or not the user has each permission in that specific issue</li><br/>
>  </ul><br/>
>  <p><br/>
>  NB: The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided,<br/>
>  <b>but</b> may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because<br/>
>  any user could be a reporter, except in the context of a concrete issue, where the reporter is known.<br/>
>  </p><br/>
>  <p><br/>
>  Global permissions will still be returned for all scopes.<br/>
>  </p><br/>
>  <p><br/>
>  Prior to version 6.4 this service returned project permissions with keys corresponding to com.atlassian.jira.security.Permissions.Permission constants.<br/>
>  Since 6.4 those keys are considered deprecated and this service returns system project permission keys corresponding to constants defined in com.atlassian.jira.permission.ProjectPermissions.<br/>
>  Permissions with legacy keys are still also returned for backwards compatibility, they are marked with an attribute deprecatedKey=true.<br/>
>  The attribute is missing for project permissions with the current keys.<br/>
>  </p>

#### Input Parameters
* `projectKey` - _optional_ - - key of project to scope returned permissions for.
* `projectId` - _optional_ - - id of project to scope returned permissions for.
* `issueKey` - _optional_ - - key of the issue to scope returned permissions for.
* `issueId` - _optional_ - - id of the issue to scope returned permissions for.

### Removes preference of the currently logged in user. Preference key must be provided as input parameters (key). If<br/>
>  key parameter is not provided or wrong - status code 404. If preference is unset - status code 204.

#### Input Parameters
* `key` - _optional_ - - key of the preference to be removed.

### Returns preference of the currently logged in user. Preference key must be provided as input parameter (key). The<br/>
>  value is returned exactly as it is. If key parameter is not provided or wrong - status code 404. If value is<br/>
>  found  - status code 200.

#### Input Parameters
* `key` - _optional_ - - key of the preference to be returned.

### Sets preference of the currently logged in user. Preference key must be provided as input parameters (key). Value<br/>
>  must be provided as post body. If key or value parameter is not provided - status code 404. If preference is set<br/>
>  - status code 204.

#### Input Parameters
* `key` - _optional_ - - key of the preference to be set.

### Returns currently logged user. This resource cannot be accessed anonymously.

### Modify currently logged user. The "value" fields present will override the existing value.<br/>
>  Fields skipped in request will not be changed. Only email and display name can be change that way.<br/>
>  Requires user password.

### Modify caller password.

### Returns a <a href="#pagination">paginated</a> list of notification schemes. In order to access notification scheme, the calling user is<br/>
>  required to have permissions to administer at least one project associated with the requested notification scheme. Each scheme contains<br/>
>  a list of events and recipient configured to receive notifications for these events. Consumer should allow events without recipients to appear in response.<br/>
>  The list is ordered by the scheme's name.<br/>
>  Follow the documentation of /notificationscheme/{id} resource for all details about returned value.

#### Input Parameters
* `startAt` - _optional_ - the index of the first notification scheme to return (0 based).
* `maxResults` - _optional_ - the maximum number of notification schemes to return (max 50).
* `expand` - _optional_

### Returns a full representation of the notification scheme for the given id. This resource will return a<br/>
>  notification scheme containing a list of events and recipient configured to receive notifications for these events. Consumer<br/>
>  should allow events without recipients to appear in response. User accessing<br/>
>  the data is required to have permissions to administer at least one project associated with the requested notification scheme.<br/>
>  <p><br/>
>  Notification recipients can be:<br/>
>  <ul><br/>
>  <li>current assignee - the value of the notificationType is CurrentAssignee</li><br/>
>  <li>issue reporter - the value of the notificationType is Reporter</li><br/>
>  <li>current user - the value of the notificationType is CurrentUser</li><br/>
>  <li>project lead - the value of the notificationType is ProjectLead</li><br/>
>  <li>component lead - the value of the notificationType is ComponentLead</li><br/>
>  <li>all watchers - the value of the notification type is AllWatchers</li><br/>
>  <li>configured user - the value of the notification type is User. Parameter will contain key of the user. Information about the user will be provided<br/>
>  if <b>user</b> expand parameter is used. </li><br/>
>  <li>configured group - the value of the notification type is Group. Parameter will contain name of the group. Information about the group will be provided<br/>
>  if <b>group</b> expand parameter is used. </li><br/>
>  <li>configured email address - the value of the notification type is EmailAddress, additionally information about the email will be provided.</li><br/>
>  <li>users or users in groups in the configured custom fields - the value of the notification type is UserCustomField or GroupCustomField. Parameter<br/>
>  will contain id of the custom field. Information about the field will be provided if <b>field</b> expand parameter is used. </li><br/>
>  <li>configured project role - the value of the notification type is ProjectRole. Parameter will contain project role id. Information about the project role<br/>
>  will be provided if <b>projectRole</b> expand parameter is used. </li><br/>
>  </ul><br/>
>  Please see the example for reference.<br/>
>  </p><br/>
>  The events can be JIRA system events or events configured by administrator. In case of the system events, data about theirs<br/>
>  ids, names and descriptions is provided. In case of custom events, the template event is included as well.

#### Input Parameters
* `expand` - _optional_

### Returns the list of requirements for the current password policy. For example, "The password must have at least 10 characters.",<br/>
>  "The password must not be similar to the user's name or email address.", etc.

#### Input Parameters
* `hasOldPassword` - _optional_ - whether or not the user will be required to enter their current password.  Use
                       {@code false} (the default) if this is a new user or if an administrator is forcibly changing
                       another user's password.

### Returns a list of statements explaining why the password policy would disallow a proposed password for a new user.<br/>
>  <p><br/>
>  You can use this method to test the password policy validation. This could be done prior to an action <br/>
>  where a new user and related password are created, using methods like the ones in <br/>
>  <a href="https://docs.atlassian.com/jira/latest/com/atlassian/jira/bc/user/UserService.html">UserService</a>.      <br/>
>  For example, you could use this to validate a password in a create user form in the user interface, as the user enters it.<br/><br/>
>  The username and new password must be not empty to perform the validation.<br/><br/>
>  Note, this method will help you validate against the policy only. It won't check any other validations that might be performed <br/>
>  when creating a new user, e.g. checking whether a user with the same name already exists.<br/>
>  </p>

### Returns a list of statements explaining why the password policy would disallow a proposed new password for a user with an existing password.<br/>
>  <p><br/>
>  You can use this method to test the password policy validation. This could be done prior to an action where the password <br/>
>  is actually updated, using methods like <a href="https://docs.atlassian.com/jira/latest/com/atlassian/jira/web/action/user/ChangePassword.html">ChangePassword</a>      <br/>
>  or <a href="https://docs.atlassian.com/jira/latest/com/atlassian/jira/web/action/user/ResetPassword.html">ResetPassword</a>. <br/>
>  For example, you could use this to validate a password in a change password form in the user interface, as the user enters it.<br/><br/>
>  The user must exist and the username and new password must be not empty, to perform the validation.<br/><br/>
>  Note, this method will help you validate against the policy only. It won't check any other validations that might be performed <br/>
>  when submitting a password change/reset request, e.g. verifying whether the old password is valid.<br/>
>  </p>

### Returns all permissions that are present in the JIRA instance - Global, Project and the global ones added by plugins

### Returns a list of all permission schemes.<br/>
>  <p><br/>
>  By default only shortened beans are returned. If you want to include permissions of all the schemes,<br/>
>  then specify the <b>permissions</b> expand parameter. Permissions will be included also if you specify<br/>
>  any other expand parameter.<br/>
>  </p>

#### Input Parameters
* `expand` - _optional_

### Create a new permission scheme.<br/>
>  This method can create schemes with a defined permission set, or without.

#### Input Parameters
* `expand` - _optional_

### getSchemeAttribute

#### Input Parameters
* `permissionSchemeId` - _required_ - permission scheme id
* `attributeKey` - _required_ - permission scheme attribute key

### Updates or inserts the attribute for a permission scheme specified by permission scheme id.<br/>
>  The attribute consists of the key and the value. The value will be converted to Boolean using Boolean#valueOf.

#### Input Parameters
* `permissionSchemeId` - _required_ - permission scheme id
* `key` - _required_ - permission scheme attribute key

### Deletes a permission scheme identified by the given id.

#### Input Parameters
* `schemeId` - _required_

### Returns a permission scheme identified by the given id.

#### Input Parameters
* `expand` - _optional_

### Updates a permission scheme.<br/>
>  <p><br/>
>  If the permissions list is present then it will be set in the permission scheme, which basically means it will overwrite any permission grants that<br/>
>  existed in the permission scheme. Sending an empty list will remove all permission grants from the permission scheme.<br/>
>  </p><br/>
>  <p><br/>
>  To update just the name and description, do not send permissions list at all.<br/>
>  </p><br/>
>  <p><br/>
>  To add or remove a single permission grant instead of updating the whole list at once use the <b>{schemeId}/permission/</b> resource.<br/>
>  </p>

#### Input Parameters
* `expand` - _optional_

### Returns all permission grants of the given permission scheme.

#### Input Parameters
* `expand` - _optional_

### Creates a permission grant in a permission scheme.

#### Input Parameters
* `expand` - _optional_

### Deletes a permission grant from a permission scheme.

#### Input Parameters
* `permissionId` - _required_
* `schemeId` - _required_

### Returns a permission grant identified by the given id.

#### Input Parameters
* `expand` - _optional_
* `schemeId` - _required_

### Returns a list of all issue priorities.

### Returns an issue priority.

#### Input Parameters
* `id` - _required_ - a String containing the priority id

### Returns all projects which are visible for the currently logged in user. If no user is logged in, it returns the<br/>
>  list of projects that are visible when using anonymous access.

#### Input Parameters
* `expand` - _optional_ - the parameters to expand
* `recent` - _optional_ - if this parameter is set then only projects recently accessed by the current user (if not logged in then based on HTTP session) will be returned (maximum count limited to the specified number but no more than 20).

### Creates a new project.

### Returns all the project types defined on the JIRA instance, not taking into account whether<br/>
>  the license to use those project types is valid or not.

### Returns the project type with the given key.

#### Input Parameters
* `projectTypeKey` - _required_

### Returns the project type with the given key, if it is accessible to the logged in user.<br/>
>  This takes into account whether the user is licensed on the Application that defines the project type.

#### Input Parameters
* `projectTypeKey` - _required_

### Deletes a project.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project id or project key

### Contains a full representation of a project in JSON format.<br/>
>  <p><br/>
>  All project keys associated with the project will only be returned if <code>expand=projectKeys</code>.<br/>
>  <p>

#### Input Parameters
* `expand` - _optional_ - the parameters to expand

### Updates a project.<br/>
>  <p><br/>
>  Only non null values sent in JSON will be updated in the project.</p><br/>
>  <p><br/>
>  Values available for the assigneeType field are: "PROJECT_LEAD" and "UNASSIGNED".</p>

#### Input Parameters
* `expand` - _optional_ - the parameters to expand in returned project

### Converts temporary avatar into a real avatar

#### Input Parameters
* `projectIdOrKey` - _required_

### put_api_2_project__projectIdOrKey__avatar

#### Input Parameters
* `projectIdOrKey` - _required_

### Creates temporary avatar using multipart. The response is sent back as JSON stored in a textarea. This is because<br/>
>  the client uses remote iframing to submit avatars using multipart. So we must send them a valid HTML page back from<br/>
>  which the client parses the JSON.

#### Input Parameters
* `projectIdOrKey` - _required_ - Project id or project key

### Deletes avatar

#### Input Parameters
* `projectIdOrKey` - _required_ - Project id or project key
* `id` - _required_ - database id for avatar

### Returns all avatars which are visible for the currently logged in user.  The avatars are grouped into<br/>
>  system and custom.

#### Input Parameters
* `projectIdOrKey` - _required_ - project id or project key

### Contains a full representation of a the specified project's components.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project id or project key

### Returns the keys of all properties for the project identified by the key or by the id.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project from which keys will be returned.

### Removes the property from the project identified by the key or by the id. Ths user removing the property is required<br/>
>  to have permissions to administer the project.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Returns the value of the property with a given key from the project identified by the key or by the id. The user who retrieves<br/>
>  the property is required to have permissions to read the project.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Sets the value of the specified project's property.<br/>
>  <p><br/>
>  You can use this resource to store a custom data against the project identified by the key or by the id. The user<br/>
>  who stores the data is required to have permissions to administer the project.<br/>
>  </p>

#### Input Parameters
* `projectIdOrKey` - _required_ - the project from which keys will be returned.
* `propertyKey` - _required_ - the key of the property to return.

### Returns all roles in the given project Id or key, with links to full details on each role.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project id or project key

### Deletes actors (users or groups) from a project role.<br/>
>  <p><br/>
>  <ul><br/>
>  <li>Delete a user from the role: <code>/rest/api/2/project/{projectIdOrKey}/role/{roleId}?user={username}</code></li><br/>
>  <li>Delete a group from the role: <code>/rest/api/2/project/{projectIdOrKey}/role/{roleId}?group={groupname}</code></li><br/>
>  </ul>

#### Input Parameters
* `user` - _optional_ - the username to remove from the project role
* `group` - _optional_ - the groupname to remove from the project role

### Returns the details for a given project role in a project.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project id or project key
* `id` - _required_ - the project role id

### Adds an actor (user or group) to a project role.

#### Input Parameters
* `projectIdOrKey` - _required_ - the project id or project key
* `id` - _required_ - the project role id

### Updates a project role to include the specified actors (users or groups).

#### Input Parameters
* `projectIdOrKey` - _required_ - the project id or project key
* `id` - _required_ - the project role id

### Get all issue types with valid status values for a project

#### Input Parameters
* `projectIdOrKey` - _required_ - Project id or project key

### Updates the type of a project.

#### Input Parameters
* `projectIdOrKey` - _required_ - identity of the project to update
* `newProjectTypeKey` - _required_ - The key of the new project type

### Returns all versions for the specified project. Results are <a href="#pagination">paginated</a>.<br/>
>  <p><br/>
>  Results can be ordered by the following fields:<br/>
>  <ul><br/>
>  <li>sequence</li><br/>
>  <li>name</li><br/>
>  <li>startDate</li><br/>
>  <li>releaseDate</li><br/>
>  </ul><br/>
>  </p>

#### Input Parameters
* `startAt` - _optional_ - the page offset, if not specified then defaults to 0
* `maxResults` - _optional_ - how many results on the page should be included. Defaults to 50.
* `orderBy` - _optional_ - ordering of the results.
* `expand` - _optional_ - the parameters to expand

### Contains a full representation of a the specified project's versions.

#### Input Parameters
* `expand` - _optional_ - the parameters to expand

### Returns the issue security scheme for project.

#### Input Parameters
* `projectKeyOrId` - _required_

### Gets a notification scheme associated with the project.<br/>
>  Follow the documentation of /notificationscheme/{id} resource for all details about returned value.

#### Input Parameters
* `expand` - _optional_

### Gets a permission scheme assigned with a project.

#### Input Parameters
* `expand` - _optional_

### Assigns a permission scheme with a project.

#### Input Parameters
* `expand` - _optional_

### Returns all security levels for the project that the current logged in user has access to.<br/>
>  If the user does not have the Set Issue Security permission, the list will be empty.

#### Input Parameters
* `projectKeyOrId` - _required_ - - key or id of project to list the security levels for

### Returns all project categories

### Create a project category via POST.

### Delete a project category.

#### Input Parameters
* `id` - _required_

### Contains a representation of a project category in JSON format.

#### Input Parameters
* `id` - _required_

### Modify a project category via PUT. Any fields present in the PUT will override existing values. As a convenience, if a field<br/>
>  is not present, it is silently ignored.

#### Input Parameters
* `id` - _required_

### Validates a project key.

#### Input Parameters
* `key` - _optional_ - the project key

### Returns information on the system reindexes.  If a reindex is currently taking place then information about this reindex is returned.<br/>
>  If there is no active index task, then returns information about the latest reindex task run, otherwise returns a 404<br/>
>  indicating that no reindex has taken place.

#### Input Parameters
* `taskId` - _optional_ - the id of an indexing task you wish to obtain details on.  If omitted, then defaults to the standard behaviour and
               returns information on the active reindex task, or the last task to run if no reindex is taking place. .  If there is no
               reindexing task with that id then a 404 is returned.

### Kicks off a reindex.  Need Admin permissions to perform this reindex.

#### Input Parameters
* `type` - _optional_ - Case insensitive String indicating type of reindex.  If omitted, then defaults to BACKGROUND_PREFERRED.
* `indexComments` - _optional_ - Indicates that comments should also be reindexed. Not relevant for foreground reindex, where comments are always reindexed.
* `indexChangeHistory` - _optional_ - Indicates that changeHistory should also be reindexed. Not relevant for foreground reindex, where changeHistory is always reindexed.
* `indexWorklogs` - _optional_ - Indicates that changeHistory should also be reindexed. Not relevant for foreground reindex, where changeHistory is always reindexed.

### Reindexes one or more individual issues.  Indexing is performed synchronously - the call returns when indexing of<br/>
>  the issues has completed or a failure occurs.<br/>
>  <p><br/>
>  Use either explicitly specified issue IDs or a JQL query to select issues to reindex.

#### Input Parameters
* `issueId` - _optional_ - the IDs or keys of one or more issues to reindex.
* `indexComments` - _optional_ - Indicates that comments should also be reindexed.
* `indexChangeHistory` - _optional_ - Indicates that changeHistory should also be reindexed.
* `indexWorklogs` - _optional_ - Indicates that changeHistory should also be reindexed.

### Returns information on the system reindexes.  If a reindex is currently taking place then information about this reindex is returned.<br/>
>  If there is no active index task, then returns information about the latest reindex task run, otherwise returns a 404<br/>
>  indicating that no reindex has taken place.

#### Input Parameters
* `taskId` - _optional_ - the id of an indexing task you wish to obtain details on.  If omitted, then defaults to the standard behaviour and
               returns information on the active reindex task, or the last task to run if no reindex is taking place. .  If there is no
               reindexing task with that id then a 404 is returned.

### Executes any pending reindex requests.  Returns a JSON array containing the IDs of the reindex requests<br/>
>  that are being processed.  Execution is asynchronous - progress of the returned tasks can be monitored through<br/>
>  other REST calls.

### Retrieves the progress of a multiple reindex requests.  Only reindex requests that actually exist will be returned<br/>
>  in the results.

#### Input Parameters
* `requestId` - _optional_ - the reindex request IDs.

### Retrieves the progress of a single reindex request.

#### Input Parameters
* `requestId` - _required_ - the reindex request ID.

### Returns a list of all resolutions.

### Returns a resolution.

#### Input Parameters
* `id` - _required_ - a String containing the resolution id

### Get all the ProjectRoles available in JIRA. Currently this list is global.

### Creates a new ProjectRole to be available in JIRA.<br/>
>  The created role does not have any default actors assigned.

### Deletes a role. May return 403 in the future

#### Input Parameters
* `swap` - _optional_ - if given, removes a role even if it is used in scheme by replacing the role with the given one

### Get a specific ProjectRole available in JIRA.

#### Input Parameters
* `id` - _required_

### Partially updates a roles name or description.

#### Input Parameters
* `id` - _required_

### Fully updates a roles. Both name and description must be given.

#### Input Parameters
* `id` - _required_

### Removes default actor from the given role.

#### Input Parameters
* `user` - _optional_ - if given, removes an actor from given role
* `group` - _optional_ - if given, removes an actor from given role

### Gets default actors for the given role.

#### Input Parameters
* `id` - _required_ - the role id to remove the actors from

### Adds default actors to the given role. The request data should contain a list of usernames or a list of groups to add.

#### Input Parameters
* `id` - _required_ - the role id to remove the actors from

### Adds field or custom field to the default tab

#### Input Parameters
* `fieldId` - _required_ - id of field / custom field

### Gets available fields for screen. i.e ones that haven't already been added.

#### Input Parameters
* `screenId` - _required_ - id of screen

### Returns a list of all tabs for the given screen

#### Input Parameters
* `projectKey` - _optional_ - the key of the project; this parameter is optional

### Creates tab for given screen

#### Input Parameters
* `screenId` - _required_ - id of screen

### Deletes tab to give screen

#### Input Parameters
* `screenId` - _required_ - id of screen
* `tabId` - _required_ - id of tab

### Renames tab on given screen

#### Input Parameters
* `screenId` - _required_ - id of screen
* `tabId` - _required_ - id of tab

### Gets all fields for a given tab

#### Input Parameters
* `projectKey` - _optional_ - the key of the project; this parameter is optional
* `tabId` - _required_ - id of tab

### Adds field to the given tab.

#### Input Parameters
* `screenId` - _required_ - id of screen
* `tabId` - _required_ - id of tab

### Removes field from given tab

#### Input Parameters
* `screenId` - _required_ - id of screen
* `tabId` - _required_ - id of tab
* `id` - _required_

### Moves field on the given tab

#### Input Parameters
* `screenId` - _required_ - id of screen
* `tabId` - _required_ - id of tab
* `id` - _required_

### Moves tab position

#### Input Parameters
* `screenId` - _required_ - id of screen
* `tabId` - _required_ - id of tab
* `pos` - _required_ - position of tab

### Searches for issues using JQL.<br/>
>  <p><br/>
>  <b>Sorting</b><br/>
>  the <code>jql</code> parameter is a full <a href="http://confluence.atlassian.com/display/JIRA/Advanced+Searching">JQL</a><br/>
>  expression, and includes an <code>ORDER BY</code> clause.<br/>
>  </p><br/>
>  <p><br/>
>  The <code>fields</code> param (which can be specified multiple times) gives a comma-separated list of fields<br/>
>  to include in the response. This can be used to retrieve a subset of fields.<br/>
>  A particular field can be excluded by prefixing it with a minus.<br/>
>  <p><br/>
>  By default, only navigable (<code>*navigable</code>) fields are returned in this search resource. Note: the default is different<br/>
>  in the get-issue resource -- the default there all fields (<code>*all</code>).<br/>
>  <ul><br/>
>  <li><code>*all</code> - include all fields</li><br/>
>  <li><code>*navigable</code> - include just navigable fields</li><br/>
>  <li><code>summary,comment</code> - include just the summary and comments</li><br/>
>  <li><code>-description</code> - include navigable fields except the description (the default is <code>*navigable</code> for search)</li><br/>
>  <li><code>*all,-comment</code> - include everything except comments</li><br/>
>  </ul><br/>
>  <p><br/>
>  </p><br/>
>  <p><b>GET vs POST:</b><br/>
>  If the JQL query is too large to be encoded as a query param you should instead<br/>
>  POST to this resource.<br/>
>  </p><br/>
>  <p><br/>
>  <b>Expanding Issues in the Search Result:</b><br/>
>  It is possible to expand the issues returned by directly specifying the expansion on the expand parameter passed<br/>
>  in to this resources.<br/>
>  </p><br/>
>  <p><br/>
>  For instance, to expand the &quot;changelog&quot; for all the issues on the search result, it is neccesary to<br/>
>  specify &quot;changelog&quot; as one of the values to expand.<br/>
>  </p>

#### Input Parameters
* `jql` - _optional_ - a JQL query string
* `startAt` - _optional_ - the index of the first issue to return (0-based)
* `maxResults` - _optional_ - the maximum number of issues to return (defaults to 50). The maximum allowable value is
                      dictated by the JIRA property 'jira.search.views.default.max'. If you specify a value that is higher than this
                      number, your search results will be truncated.
* `validateQuery` - _optional_ - whether to validate the JQL query
* `fields` - _optional_ - the list of fields to return for each issue. By default, all navigable fields are returned.
* `expand` - _optional_ - A comma-separated list of the parameters to expand.

### Performs a search using JQL.

### Returns a full representation of the security level that has the given id.

#### Input Parameters
* `id` - _required_ - a String containing an issue security level id

### Returns general information about the current JIRA server.

#### Input Parameters
* `doHealthCheck` - _optional_

### Sets the base URL that is configured for this JIRA instance.

### Returns the default system columns for issue navigator. Admin permission will be required.

### Sets the default system columns for issue navigator. Admin permission will be required.

### Returns a list of all statuses

### Returns a full representation of the Status having the given id or name.

#### Input Parameters
* `idOrName` - _required_ - a numeric Status id or a status name

### Returns a list of all status categories

### Returns a full representation of the StatusCategory having the given id or key

#### Input Parameters
* `idOrKey` - _required_ - a numeric StatusCategory id or a status category key

### getAvatars

#### Input Parameters
* `type` - _required_
* `owningObjectId` - _required_

### post_api_2_universal_avatar_type__type__owner__owningObjectId__avatar

#### Input Parameters
* `type` - _required_
* `owningObjectId` - _required_

### Deletes avatar

#### Input Parameters
* `id` - _required_ - database id for avatar
* `type` - _required_ - Project id or project key
* `owningObjectId` - _required_

### post_api_2_universal_avatar_type__type__owner__owningObjectId__temp

#### Input Parameters
* `type` - _required_
* `owningObjectId` - _required_

### Returns the result of the last upgrade task.<br/>
> <br/>
>  Returns {@link javax.ws.rs.core.Response#seeOther(java.net.URI)} if still running.

### Runs any pending delayed upgrade tasks.  Need Admin permissions to do this.

### Removes user.

#### Input Parameters
* `username` - _optional_ - the username
* `key` - _optional_ - user key

### Returns a user. This resource cannot be accessed anonymously.

#### Input Parameters
* `username` - _optional_ - the username
* `key` - _optional_ - user key

### Create user. By default created user will not be notified with email.<br/>
>  If password field is not set then password will be randomly generated.

### Modify user. The "value" fields present will override the existing value.<br/>
>  Fields skipped in request will not be changed.

#### Input Parameters
* `username` - _optional_ - the username
* `key` - _optional_ - user key

### Remove user from given application. Admin permission will be required to perform this operation.

#### Input Parameters
* `username` - _optional_ - username
* `applicationKey` - _optional_ - application key

### Add user to given application. Admin permission will be required to perform this operation.

#### Input Parameters
* `username` - _optional_ - username
* `applicationKey` - _optional_ - application key

### Returns a list of users that match the search string and can be assigned issues for all the given projects.<br/>
>  This resource cannot be accessed anonymously.

#### Input Parameters
* `username` - _optional_ - the username
* `projectKeys` - _optional_ - the keys of the projects we are finding assignable users for, comma-separated
* `startAt` - _optional_ - the index of the first user to return (0-based)
* `maxResults` - _optional_ - the maximum number of users to return (defaults to 50). The maximum allowed value is 1000.
                       If you specify a value that is higher than this number, your search results will be truncated.

### Returns a list of users that match the search string. This resource cannot be accessed anonymously.<br/>
>  Please note that this resource should be called with an issue key when a list of assignable users is retrieved<br/>
>  for editing.  For create only a project key should be supplied.  The list of assignable users may be incorrect<br/>
>  if it's called with the project key for editing.

#### Input Parameters
* `username` - _optional_ - the username
* `project` - _optional_ - the key of the project we are finding assignable users for
* `issueKey` - _optional_ - the issue key for the issue being edited we need to find assignable users for.
* `startAt` - _optional_ - the index of the first user to return (0-based)
* `maxResults` - _optional_ - the maximum number of users to return (defaults to 50). The maximum allowed value is 1000.
                   If you specify a value that is higher than this number, your search results will be truncated.
* `actionDescriptorId` - _optional_

### Converts temporary avatar into a real avatar

#### Input Parameters
* `username` - _optional_ - username

### put_api_2_user_avatar

#### Input Parameters
* `username` - _optional_

### Creates temporary avatar using multipart. The response is sent back as JSON stored in a textarea. This is because<br/>
>  the client uses remote iframing to submit avatars using multipart. So we must send them a valid HTML page back from<br/>
>  which the client parses the JSON from.<br/>
>  <p><br/>
>  Creating a temporary avatar is part of a 3-step process in uploading a new<br/>
>  avatar for a user: upload, crop, confirm. This endpoint allows you to use a multipart upload<br/>
>  instead of sending the image directly as the request body.<br/>
>  </p><br/>
>  <p><br/>
>  You *must* use "avatar" as the name of the upload parameter:</p><br/>
>  <p/><br/>
>  <pre><br/>
>  curl -c cookiejar.txt -X POST -u admin:admin -H "X-Atlassian-Token: no-check" \<br/>
>    -F "avatar=@mynewavatar.png;type=image/png" \<br/>
>    'http://localhost:8090/jira/rest/api/2/user/avatar/temporary?username=admin'<br/>
>  </pre>

#### Input Parameters
* `username` - _optional_ - Username

### Deletes avatar

#### Input Parameters
* `username` - _optional_ - username

### Returns all avatars which are visible for the currently logged in user.

#### Input Parameters
* `username` - _optional_ - username

### Reset the default columns for the given user to the system default. Admin permission will be required to get<br/>
>  columns for a user other than the currently logged in user.

#### Input Parameters
* `username` - _optional_ - username

### Returns the default columns for the given user. Admin permission will be required to get columns for a user<br/>
>  other than the currently logged in user.

#### Input Parameters
* `username` - _optional_ - username

### Sets the default columns for the given user.  Admin permission will be required to get columns for a user<br/>
>  other than the currently logged in user.

### Modify user password.

#### Input Parameters
* `username` - _optional_ - the username
* `key` - _optional_ - user key

### Returns a list of active users that match the search string and have all specified permissions for the project or issue.<br><br/>
>  This resource can be accessed by users with ADMINISTER_PROJECT permission for the project or global ADMIN or SYSADMIN rights.

#### Input Parameters
* `username` - _optional_ - the username filter, list includes all users if unspecified
* `permissions` - _optional_ - comma separated list of permissions for project or issue returned users must have, see
                    <a href="https://developer.atlassian.com/static/javadoc/jira/6.0/reference/com/atlassian/jira/security/Permissions.Permission.html">Permissions</a>
                    JavaDoc for the list of all possible permissions.
* `issueKey` - _optional_ - the issue key for the issue for which returned users have specified permissions.
* `projectKey` - _optional_ - the optional project key to search for users with if no issueKey is supplied.
* `startAt` - _optional_ - the index of the first user to return (0-based)
* `maxResults` - _optional_ - the maximum number of users to return (defaults to 50). The maximum allowed value is 1000.
                    If you specify a value that is higher than this number, your search results will be truncated.

### Returns a list of users matching query with highlighting. This resource cannot be accessed anonymously.

#### Input Parameters
* `query` - _optional_ - A string used to search username, Name or e-mail address
* `maxResults` - _optional_ - the maximum number of users to return (defaults to 50). The maximum allowed value is 1000.
                   If you specify a value that is higher than this number, your search results will be truncated.
* `showAvatar` - _optional_
* `exclude` - _optional_

### Returns the keys of all properties for the user identified by the key or by the id.

#### Input Parameters
* `userKey` - _optional_ - key of the user whose properties are to be returned
* `username` - _optional_ - username of the user whose properties are to be returned

### Removes the property from the user identified by the key or by the id. Ths user removing the property is required<br/>
>  to have permissions to administer the user.

#### Input Parameters
* `userKey` - _optional_ - key of the user whose property is to be removed
* `username` - _optional_ - username of the user whose property is to be removed

### Returns the value of the property with a given key from the user identified by the key or by the id. The user who retrieves<br/>
>  the property is required to have permissions to read the user.

#### Input Parameters
* `userKey` - _optional_ - key of the user whose property is to be returned
* `username` - _optional_ - username of the user whose property is to be returned

### Sets the value of the specified user's property.<br/>
>  <p><br/>
>  You can use this resource to store a custom data against the user identified by the key or by the id. The user<br/>
>  who stores the data is required to have permissions to administer the user.<br/>
>  </p>

#### Input Parameters
* `userKey` - _optional_ - key of the user whose property is to be set
* `username` - _optional_ - username of the user whose property is to be set

### Returns a list of users that match the search string. This resource cannot be accessed anonymously.

#### Input Parameters
* `username` - _optional_ - A query string used to search username, name or e-mail address
* `startAt` - _optional_ - the index of the first user to return (0-based)
* `maxResults` - _optional_ - the maximum number of users to return (defaults to 50). The maximum allowed value is 1000.
                        If you specify a value that is higher than this number, your search results will be truncated.
* `includeActive` - _optional_ - If true, then active users are included in the results (default true)
* `includeInactive` - _optional_ - If true, then inactive users are included in the results (default false)

### Returns a list of active users that match the search string. This resource cannot be accessed anonymously <br/>
>  and requires the Browse Users global permission.<br/>
>  Given an issue key this resource will provide a list of users that match the search string and have<br/>
>  the browse issue permission for the issue provided.

#### Input Parameters
* `username` - _optional_ - the username filter, no users returned if left blank
* `issueKey` - _optional_ - the issue key for the issue being edited we need to find viewable users for.
* `projectKey` - _optional_ - the optional project key to search for users with if no issueKey is supplied.
* `startAt` - _optional_ - the index of the first user to return (0-based)
* `maxResults` - _optional_ - the maximum number of users to return (defaults to 50). The maximum allowed value is 1000.
                   If you specify a value that is higher than this number, your search results will be truncated.

### Create a version via POST.

### Returns the remote version links for a given global ID.

#### Input Parameters
* `globalId` - _optional_ - the global ID of the remote resource that is linked to the versions

### Delete a project version.

#### Input Parameters
* `moveFixIssuesTo` - _optional_ - The version to set fixVersion to on issues where the deleted version is the fix version,
                             If null then the fixVersion is removed.
* `moveAffectedIssuesTo` - _optional_ - The version to set affectedVersion to on issues where the deleted version is the affected version,
                             If null then the affectedVersion is removed.

### Returns a project version.

#### Input Parameters
* `expand` - _optional_

### Modify a version via PUT. Any fields present in the PUT will override existing values. As a convenience, if a field<br/>
>  is not present, it is silently ignored.

#### Input Parameters
* `id` - _required_ - The version to delete

### Merge versions

#### Input Parameters
* `moveIssuesTo` - _required_ - The version to set fixVersion to on issues where the deleted version is the fix version,
                     If null then the fixVersion is removed.
* `id` - _required_ - The version that will be merged to version {@code moveIssuesTo} and removed

### Modify a version's sequence within a project.<br/>
>  <p/><br/>
>  The move version bean has 2 alternative field value pairs:<br/>
>  <dl><br/>
>  <dt>position</dt><dd>An absolute position, which may have a value of 'First', 'Last', 'Earlier' or 'Later'</dd><br/>
>  <dt>after</dt><dd>A version to place this version after.  The value should be the self link of another version</dd><br/>
>  </dl>

#### Input Parameters
* `id` - _required_ - a String containing the version id

### Returns a bean containing the number of fixed in and affected issues for the given version.

#### Input Parameters
* `id` - _required_ - a String containing the version id

### Delete a project version.

#### Input Parameters
* `id` - _required_ - The version to delete

### Returns the number of unresolved issues for the given version

#### Input Parameters
* `id` - _required_ - a String containing the version id

### Delete all remote version links for a given version ID.

#### Input Parameters
* `versionId` - _required_ - The version for which to delete ALL existing remote version links

### Returns the remote version links associated with the given version ID.

#### Input Parameters
* `versionId` - _required_ - The version for which to delete ALL existing remote version links

### Create a remote version link via POST.  The link's global ID will be taken from the<br/>
>  JSON payload if provided; otherwise, it will be generated.

#### Input Parameters
* `versionId` - _required_ - The version for which to delete ALL existing remote version links

### Delete a specific remote version link with the given version ID and global ID.

#### Input Parameters
* `versionId` - _required_ - The version ID of the remote link
* `globalId` - _required_ - The global ID of the remote link

### A REST sub-resource representing a remote version link

#### Input Parameters
* `versionId` - _required_ - The version ID of the remote link
* `globalId` - _required_ - The global ID of the remote link

### Create a remote version link via POST.  The link's global ID will be taken from the<br/>
>  JSON payload if provided; otherwise, it will be generated.

#### Input Parameters
* `versionId` - _required_ - The version ID of the remote link
* `globalId` - _required_ - The global ID of the remote link

### Returns all workflows.

#### Input Parameters
* `workflowName` - _optional_

### Delete a property from the passed transition on the passed workflow. It is not an error to delete a property that<br/>
>  does not exist.

#### Input Parameters
* `key` - _optional_ - the name of the property to add.
* `workflowName` - _optional_ - the name of the workflow to use.
* `workflowMode` - _optional_ - the type of workflow to use. Can either be "live" or "draft".

### Return the property or properties associated with a transition.

#### Input Parameters
* `includeReservedKeys` - _optional_ - some keys under the "jira." prefix are editable, some are not. Set this to true
                            in order to include the non-editable keys in the response.
* `key` - _optional_ - the name of the property key to query. Can be left off the query to return all properties.
* `workflowName` - _optional_ - the name of the workflow to use.
* `workflowMode` - _optional_ - the type of workflow to use. Can either be "live" or "draft".

### Add a new property to a transition. Trying to add a property that already<br/>
>  exists will fail.

#### Input Parameters
* `key` - _optional_ - the name of the property to add.
* `workflowName` - _optional_ - the name of the workflow to use.
* `workflowMode` - _optional_ - the type of workflow to use. Can either be "live" or "draft".

### Update/add new property to a transition. Trying to update a property that does<br/>
>  not exist will result in a new property being added.

#### Input Parameters
* `key` - _optional_ - the name of the property to add.
* `workflowName` - _optional_ - the name of the workflow to use.
* `workflowMode` - _optional_ - the type of workflow to use. Can either be "live" or "draft".

### Create a new workflow scheme.<br/>
>  <p/><br/>
>  The body contains a representation of the new scheme. Values not passed are assumed to be set to their defaults.

### Delete the passed workflow scheme.

#### Input Parameters
* `id` - _required_ - the id of the scheme.

### Returns the requested workflow scheme to the caller.

#### Input Parameters
* `returnDraftIfExists` - _optional_ - when true indicates that a scheme's draft, if it exists, should be queried instead of
                            the scheme itself.

### Update the passed workflow scheme.<br/>
>  <p/><br/>
>  The body of the request is a representation of the workflow scheme. Values not passed are assumed to indicate<br/>
>  no change for that field.<br/>
>  <p/><br/>
>  The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft<br/>
>  should be created and/or updated when the actual scheme cannot be edited (e.g. when the scheme is being used by<br/>
>  a project). Values not appearing the body will not be touched.

#### Input Parameters
* `id` - _required_ - the id of the scheme.

### Create a draft for the passed scheme. The draft will be a copy of the state of the parent.

#### Input Parameters
* `id` - _required_ - the id of the parent scheme.

### Remove the default workflow from the passed workflow scheme.

#### Input Parameters
* `updateDraftIfNeeded` - _optional_ - when true will create and return a draft when the workflow scheme cannot be edited
                            (e.g. when it is being used by a project).

### Return the default workflow from the passed workflow scheme.

#### Input Parameters
* `returnDraftIfExists` - _optional_ - when true indicates that a scheme's draft, if it exists, should be queried instead of
                            the scheme itself.

### Set the default workflow for the passed workflow scheme.<br/>
>  <p/><br/>
>  The passed representation can have its<br/>
>  updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme<br/>
>  cannot be edited.

#### Input Parameters
* `id` - _required_ - the id of the scheme.

### Delete the passed draft workflow scheme.

#### Input Parameters
* `id` - _required_ - the id of the parent scheme.

### Returns the requested draft workflow scheme to the caller.

#### Input Parameters
* `id` - _required_ - the id of the parent scheme.

### Update a draft workflow scheme. The draft will created if necessary.<br/>
>  <p/><br/>
>  The body is a representation of the workflow scheme. Values not passed are assumed to indicate no change for that field.

#### Input Parameters
* `id` - _required_ - the id of the parent scheme.

### Remove the default workflow from the passed draft workflow scheme.

#### Input Parameters
* `id` - _required_ - the id of the parent scheme.

### Return the default workflow from the passed draft workflow scheme to the caller.

#### Input Parameters
* `id` - _required_ - the id of the parent scheme.

### Set the default workflow for the passed draft workflow scheme.

#### Input Parameters
* `id` - _required_ - the id of the parent scheme.

### Remove the specified issue type mapping from the draft scheme.

#### Input Parameters
* `issueType` - _required_ - the issue type being set.
* `id` - _required_ - the id of the parent scheme.

### Returns the issue type mapping for the passed draft workflow scheme.

#### Input Parameters
* `issueType` - _required_ - the issue type being set.
* `id` - _required_ - the id of the parent scheme.

### Set the issue type mapping for the passed draft scheme.<br/>
>  <p/><br/>
>  The passed representation can have its updateDraftIfNeeded flag set to true to indicate that<br/>
>  the draft should be created/updated when the actual scheme cannot be edited.

#### Input Parameters
* `issueType` - _required_ - the issue type being set.
* `id` - _required_ - the id of the parent scheme.

### Delete the passed workflow from the draft workflow scheme.

#### Input Parameters
* `workflowName` - _optional_ - the name of the workflow to delete.

### Returns the draft workflow mappings or requested mapping to the caller.

#### Input Parameters
* `workflowName` - _optional_ - the workflow mapping to return. Null can be passed to return all mappings. Must be a valid workflow name.

### Update the draft scheme to include the passed mapping.<br/>
>  <p/><br/>
>  The body is a representation of the workflow mapping.<br/>
>  Values not passed are assumed to indicate no change for that field.

#### Input Parameters
* `workflowName` - _optional_ - the name of the workflow mapping to update.

### Remove the specified issue type mapping from the scheme.

#### Input Parameters
* `updateDraftIfNeeded` - _optional_ - when true will create and return a draft when the workflow scheme cannot be edited
                            (e.g. when it is being used by a project).
* `id` - _required_ - the id of the scheme.

### Returns the issue type mapping for the passed workflow scheme.

#### Input Parameters
* `returnDraftIfExists` - _optional_ - when true indicates that a scheme's draft, if it exists, should be queried instead of
                            the scheme itself.
* `id` - _required_ - the id of the scheme.

### Set the issue type mapping for the passed scheme.<br/>
>  <p/><br/>
>  The passed representation can have its updateDraftIfNeeded flag set to true to indicate that<br/>
>  the draft should be created/updated when the actual scheme cannot be edited.

#### Input Parameters
* `issueType` - _required_ - the issue type being set.
* `id` - _required_ - the id of the scheme.

### Delete the passed workflow from the workflow scheme.

#### Input Parameters
* `workflowName` - _optional_ - the name of the workflow to delete.
* `updateDraftIfNeeded` - _optional_ - flag to indicate if a draft should be created if necessary to delete the workflow
                            from the scheme.

### Returns the workflow mappings or requested mapping to the caller for the passed scheme.

#### Input Parameters
* `workflowName` - _optional_ - the workflow mapping to return. Null can be passed to return all mappings. Must be a valid workflow name.
* `returnDraftIfExists` - _optional_ - when true indicates that a scheme's draft, if it exists, should be queried instead of
                            the scheme itself.

### Update the scheme to include the passed mapping.<br/>
>  <p/><br/>
>  The body is a representation of the workflow mapping.<br/>
>  Values not passed are assumed to indicate no change for that field.<br/>
>  <p/><br/>
>  The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft<br/>
>  should be created/updated when the actual scheme cannot be edited.

#### Input Parameters
* `workflowName` - _optional_ - the name of the workflow mapping to update.

### Returns worklogs id and delete time of worklogs that was deleted since given time.<br/>
>  The returns set of worklogs is limited to 1000 elements.<br/>
>  This API will not return worklogs deleted during last minute.

#### Input Parameters
* `since` - _optional_ - a date time in unix timestamp format since when deleted worklogs will be returned.

### Returns worklogs for given worklog ids. Only worklogs to which the calling user has permissions, will be included in the result.<br/>
>  The returns set of worklogs is limited to 1000 elements.

### Returns worklogs id and update time of worklogs that was updated since given time.<br/>
>  The returns set of worklogs is limited to 1000 elements.<br/>
>  This API will not return worklogs updated during last minute.

#### Input Parameters
* `since` - _optional_ - a date time in unix timestamp format since when updated worklogs will be returned.

### Logs the current user out of JIRA, destroying the existing session, if any.

### Returns information about the currently authenticated user's session. If the caller is not authenticated they<br/>
>  will get a 401 Unauthorized status code.

### Creates a new session for a user in JIRA. Once a session has been successfully created it can be used to access<br/>
>  any of JIRA's remote APIs and also the web UI by passing the appropriate HTTP Cookie header.<br/>
>  <p><br/>
>  Note that it is generally preferrable to use HTTP BASIC authentication with the REST API. However, this resource<br/>
>  may be used to mimic the behaviour of JIRA's log-in page (e.g. to display log-in errors to a user).

### This method invalidates the any current WebSudo session.

## License

**flow**ground :- Telekom iPaaS / jira-local-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
