---
layout: default
title: Change dropNotNullConstraint
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'dropNotNullConstraint'

Makes a column nullable

## Available Attributes ##

<table>
<tr><th>Name</th><th>Description</th><th>Required&nbsp;For</th><th>Since</th></tr>
<tr><td style='vertical-align: top'>catalogName</td><td>Name of the catalog</td><td style='vertical-align: top'></td><td style='vertical-align: top'>3.0</td></tr>
<tr><td style='vertical-align: top'>columnDataType</td><td>Current data type of the column</td><td style='vertical-align: top'>mssql, postgres, mysql</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>columnName</td><td>Name of the column to drop the constraint from</td><td style='vertical-align: top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>dbms</td><td>null</td><td style='vertical-align: top'></td><td style='vertical-align: top'>3.0</td></tr>
<tr><td style='vertical-align: top'>schemaName</td><td>Name of the schema</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>tableName</td><td>Name of the table containing that the column to drop the constraint from</td><td style='vertical-align: top'>all</td><td style='vertical-align: top'></td></tr>
</table>

<div id='changelog-tabs'>
<ul>
    <li><a href="#tab-xml">XML Sample</a></li>
    <li><a href="#tab-yaml">YAML Sample</a></li>
    <li><a href="#tab-json">JSON Sample</a></li>
  </ul>
<div id='tab-xml'>
{% highlight xml %}
<changeSet author="liquibase-docs" id="dropNotNullConstraint-example">
    <dropNotNullConstraint catalogName="cat"
            columnDataType="A String"
            columnName="id"
            dbms="h2, oracle"
            schemaName="public"
            tableName="person"/>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: dropNotNullConstraint-example
  author: liquibase-docs
  changes:
  - dropNotNullConstraint:
      catalogName: cat
      columnDataType: A String
      columnName: id
      dbms: h2, oracle
      schemaName: public
      tableName: person

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "dropNotNullConstraint-example",
    "author": "liquibase-docs",
    "changes": [
      {
        "dropNotNullConstraint": {
          "catalogName": "cat",
          "columnDataType": "A String",
          "columnName": "id",
          "dbms": "h2, oracle",
          "schemaName": "public",
          "tableName": "person"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (MySQL)

{% highlight sql %}
ALTER TABLE cat.person MODIFY id A STRING NULL;


{% endhighlight %}

## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>Cache</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>DB2i</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Derby</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Firebird</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>H2</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>HyperSQL</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Informix</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>MySQL</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Oracle</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>PostgreSQL</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>SAP DB</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>SQL Server</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>SQLite</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>Sybase</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
</table>