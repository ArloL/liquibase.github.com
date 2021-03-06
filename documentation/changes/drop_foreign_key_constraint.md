---
layout: default
title: Change dropForeignKeyConstraint
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'dropForeignKeyConstraint'

Drops an existing foreign key

## Available Attributes ##

<table>
<tr><th>Name</th><th>Description</th><th>Required&nbsp;For</th><th>Supports</th><th>Since</th></tr>
<tr><td style='vertical-align: top'>baseTableCatalogName</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'>3.0</td></tr>
<tr><td style='vertical-align: top'>baseTableName</td><td style='vertical-align: top'>Name of the table containing the column constrained by the foreign key</td><td style='vertical-align: top'>informix, sybase, cache, unsupported, asany, postgresql, firebird, oracle, maxdb, db2i, mssql, hsqldb, db2, derby, mysql, h2</td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>baseTableSchemaName</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>constraintName</td><td style='vertical-align: top'>Name of the foreign key constraint to drop</td><td style='vertical-align: top'>informix, sybase, cache, unsupported, asany, postgresql, firebird, oracle, maxdb, db2i, mssql, hsqldb, db2, derby, mysql, h2</td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
</table>

<div id='changelog-tabs'>
<ul>
    <li><a href="#tab-xml">XML Sample</a></li>
    <li><a href="#tab-yaml">YAML Sample</a></li>
    <li><a href="#tab-json">JSON Sample</a></li>
  </ul>
<div id='tab-xml'>
{% highlight xml %}
<changeSet author="liquibase-docs" id="dropForeignKeyConstraint-example">
    <dropForeignKeyConstraint baseTableCatalogName="A String"
            baseTableName="person"
            baseTableSchemaName="A String"
            constraintName="fk_address_person"/>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: dropForeignKeyConstraint-example
  author: liquibase-docs
  changes:
  - dropForeignKeyConstraint:
      baseTableCatalogName: A String
      baseTableName: person
      baseTableSchemaName: A String
      constraintName: fk_address_person

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "dropForeignKeyConstraint-example",
    "author": "liquibase-docs",
    "changes": [
      {
        "dropForeignKeyConstraint": {
          "baseTableCatalogName": "A String",
          "baseTableName": "person",
          "baseTableSchemaName": "A String",
          "constraintName": "fk_address_person"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (MySQL)

{% highlight sql %}
ALTER TABLE A String.person DROP FOREIGN KEY fk_address_person;


{% endhighlight %}

## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>Cache</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>DB2i</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Derby</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Firebird</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>H2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>HyperSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Informix</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>MySQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Oracle</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>PostgreSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SAP DB</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQL Server</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQLite</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Sybase</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td>No</td></tr>
</table>
