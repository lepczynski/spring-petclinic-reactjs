Hello good soul!

This repo is a fok of https://github.com/spring-petclinic/spring-petclinic-reactjs.
I created it just to be able to learn Spring in more depth and to remember working with such mix break of over half a year at the moment of writing this.

I'm putting this up in hope that it might help someone traveling up the same path as me.
That is to understand setting up a Spring Boot+Hibernate+React App.

As I believe in learning by doing.

I also believe that doing something that you're passionate about.

One of my biggest DIY interests is programming MCU's and

IoT'izing lights at my flat in Warsaw (esp8266 + C++; platformio with OTA by CI/CD but It's in the process of dockerizing)

and recently my refrigerator on Wemos D1 mini in Micro Python (I'll try to put this up on GH as well)


This repo is a fork of 
https://github.com/spring-petclinic/spring-petclinic-reactjs
that I I'll try to maintain as time allows.

Soon I also hope to start sharing my technical knowledge that I am storing in form of a tree of hyperlinks, a vast mind-map ranging from mathematics through Micro Python to Java and Spring and beyond.

I hope to start a blog sharing stuff I learn (recently a few thoughts on ".dotfiles")


## Install and run

Note: Spring Boot Server App must be running before starting the client!

To start the server, launch a Terminal and run from the project's root folder (`spring-petclinic`):
```
./mvnw spring-boot:run
```

When the server is running you can try to access the API for example to query all known pet types:
```
curl http://localhost:8080/api/pettypes
```

After starting the server you can install and run the client from the `client` folder:

1. `npm install` (installs the node modules and the TypeScript definition files)
2. `PORT=4444 npm start` 
3. Open `http://localhost:4444`

(Why not use the same server for backend and frontend? Because Webpack does a great job for serving JavaScript-based SPAs and I think it's not too uncommon to run this kind of apps using two dedicated server, one for backend, one for frontend)

## Feedback

In case you have any comments, please feel free to open an issue in this repository.
If you want to contact me, please do so at lepi at hackerspace.pl : )
------


<table>
  <tr>
    <th width="300px">Spring Boot Configuration</th><th width="300px"></th>
  </tr>
  <tr>
    <td>The Main Class</td>
    <td><a href="/src/main/java/org/springframework/samples/petclinic/application/PetClinicApplication.java">PetClinicApplication.java</a></td>
  </tr>
  <tr>
    <td>Properties Files</td>
    <td>
      <a href="/src/main/resources/application.properties">application.properties</a>
    </td>
  </tr>
  <tr>
    <td>Caching</td>
    <td>Use of EhCache <a href="/src/main/java/org/springframework/samples/petclinic/config/CacheConfig.java">CacheConfig.java</a> <a href="/src/main/resources/ehcache.xml">ehcache.xml</a></td>
  </tr>
  <tr>
    <td>Dandelion</td>
    <td>DatatablesFilter, DandelionFilter and DandelionServlet registration <a href="/src/main/java/org/springframework/samples/petclinic/config/DandelionConfig.java">DandelionConfig.java</a></td>
  </tr>
  <tr>
    <td>Spring MVC - XML integration</td>
    <td><a href="/src/main/java/org/springframework/samples/petclinic/config/CustomViewsConfiguration.java">CustomViewsConfiguration.java</a></td>
  </tr>
</table>


<table>
  <tr>
    <th width="300px">Others</th><th width="300px">Files</th>
  </tr>
 <tr>
    <td>JSP custom tags</td>
    <td>
      <a href="/src/main/webapp/WEB-INF/tags">WEB-INF/tags</a>
      <a href="/src/main/webapp/WEB-INF/jsp/owners/createOrUpdateOwnerForm.jsp">createOrUpdateOwnerForm.jsp</a></td>
  </tr>
  <tr>
    <td>Bower</td>
    <td>
      <a href="/pom.xml">bower-install maven profile declaration inside pom.xml</a> <br />
      <a href="/bower.json">JavaScript libraries are defined by the manifest file bower.json</a> <br />
      <a href="/.bowerrc">Bower configuration using JSON</a> <br />
      <a href="/src/main/resources/spring/mvc-core-config.xml#L30">Resource mapping in Spring configuration</a> <br />
      <a href="/src/main/webapp/WEB-INF/jsp/fragments/staticFiles.jsp#L12">sample usage in JSP</a></td>
    </td>
  </tr>
  <tr>
    <td>Dandelion-datatables</td>
    <td>
      <a href="/src/main/webapp/WEB-INF/jsp/owners/ownersList.jsp">ownersList.jsp</a>
      <a href="/src/main/webapp/WEB-INF/jsp/vets/vetList.jsp">vetList.jsp</a>
      <a href="/src/main/webapp/WEB-INF/web.xml">web.xml</a>
      <a href="/src/main/resources/dandelion/datatables/datatables.properties">datatables.properties</a>
   </td>
  </tr>
</table>


## Interaction with other open source projects

One of the best parts about working on the Spring Petclinic application is that we have the opportunity to work in direct contact with many Open Source projects. We found some bugs/suggested improvements on various topics such as Spring, Spring Data, Bean Validation and even Eclipse! In many cases, they've been fixed/implemented in just a few days.
Here is a list of them:

<table>
  <tr>
    <th width="300px">Name</th>
    <th width="300px"> Issue </th>
  </tr>

  <tr>
    <td>Spring JDBC: simplify usage of NamedParameterJdbcTemplate</td>
    <td> <a href="https://jira.springsource.org/browse/SPR-10256"> SPR-10256</a> and <a href="https://jira.springsource.org/browse/SPR-10257"> SPR-10257</a> </td>
  </tr>
  <tr>
    <td>Bean Validation / Hibernate Validator: simplify Maven dependencies and backward compatibility</td>
    <td>
      <a href="https://hibernate.atlassian.net/browse/HV-790"> HV-790</a> and <a href="https://hibernate.atlassian.net/browse/HV-792"> HV-792</a>
      </td>
  </tr>
  <tr>
    <td>Spring Data: provide more flexibility when working with JPQL queries</td>
    <td>
      <a href="https://jira.springsource.org/browse/DATAJPA-292"> DATAJPA-292</a>
      </td>
  </tr>  
  <tr>
    <td>Eclipse: validation bug when working with .tag/.tagx files (has only been fixed for Eclipse 4.3 (Kepler)). <a href="https://github.com/spring-projects/spring-petclinic/issues/14">See here for more details.</a></td>
    <td>
      <a href="https://issuetracker.springsource.com/browse/STS-3294"> STS-3294</a>
    </td>
  </tr>    
</table>


# Contributing

The [issue tracker](https://github.com/spring-projects/spring-petclinic/issues) is the preferred channel for bug reports, features requests and submitting pull requests.

For pull requests, editor preferences are available in the [editor config](https://github.com/spring-projects/spring-petclinic/blob/master/.editorconfig) for easy use in common text editors. Read more and download plugins at <http://editorconfig.org>.




