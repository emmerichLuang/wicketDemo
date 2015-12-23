# wicketDemo
maven部署的wicket demo。

最小化的一个demo。好让初学者了解框架的结构。

1、第一步， 创建一个maven web project。并增加配置。
配置的目的：用的jetty插件跑项目，wicket的依赖。

2、在src/main/java目录中创建文件。HomePage.java、HomePage.html、MainApplication.java。
HomePage.java:描述HomePage.html的属性，动作。命名与homePage.html匹配。
HomePage.html:具体页面。命名有一个.java文件描述其动作、属性。

MainApplication.java：入口类。要配置到web.xml中。配置见：
要配置wicketServlet、和入口的application。

	<servlet>
		<servlet-name>HelloWorldApplication</servlet-name>
		<servlet-class>
			org.apache.wicket.protocol.http.WicketServlet
		</servlet-class>
		<init-param>
			<param-name>applicationClassName</param-name>
			<param-value>wicketDemo.MainApplication</param-value>
		</init-param>
	</servlet>
	<servlet-mapping>
		<servlet-name>HelloWorldApplication</servlet-name>
		<url-pattern>/*</url-pattern>
	</servlet-mapping>

