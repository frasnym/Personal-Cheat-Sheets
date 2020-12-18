# Personal Cheat Sheets

<ul>
    <li><b>Useful Websites</b>
        <ul>
            <li><a href="#usefulWebsite">Useful Websites</a></li>
        </ul>
    </li>
    <li><b>Node JS</b>
        <ul>
            <li><a href="#initializeProjectNodeJS">Initialize Project</a></li>
            <li><a href="#gitignoreNodeJS">.gitignore</a></li>
            <li><a href="#deployToHerokuNodeJS">Deploy to HEROKU</a></li>
        </ul>
    </li>
    <li><b>Flutter</b>
        <ul>
            <li><a href="#createProjectFlutter">Create Project</a></li>
            <li><a href="#fontAssetsSize">Font Assets Size</a></li>
            <li><a href="#deployPlayStoreFlutter">Deploy Google PlayStore</a></li>
        </ul>
    </li>
    <li><b>React JS</b>
        <ul>
            <li><a href="#createProjectReact">Create Project</a></li>
            <li><a href="#deployGithubPagesReactJS">Deploy to Github Pages</a></li>
            <li><a href="#routerDOMNetlifySettingReactJS">Router DOM Netlify Setting</a></li>
        </ul>
    </li>
    <li><b>React Native</b>
        <ul>
            <li><a href="#createProjectRN">Create Project</a></li>
        </ul>
    </li>
    <li><b>Laravel</b>
        <ul>
            <li><a href="#createProjectLaravel">Create Project</a></li>
            <li><a href="#startServerLaravel">Start Server</a></li>
            <li><a href="#artisanMakeMigration">Make Migration</a></li>
            <li><a href="#artisanMigrate">Migrate</a></li>
        </ul>
    </li>
    <li><b>Lumen</b>
        <ul>
            <li><a href="#createProjectLumen">Create Project</a></li>
            <li><a href="#startServerLumen">Start Server</a></li>
        </ul>
    </li>
    <li><b>Docker</b>
        <ul>
            <li><a href="#dockerfiletemplate">Dockerfile Template</a></li>
            <li><a href="#buildContainerDocker">Build Custom Image</a></li>
            <li><a href="#runBasedOnImage">Run Container Based on Image</a></li>
            <li><a href="#getRunningProcessDocker">Get Running Container Process</a></li>
            <li><a href="#stopProcessDocker">Stop Running Container Process</a></li>
        </ul>
    </li>
    <li><b>Scrapy</b>
        <ul>
            <li><a href="#createProjectScrapy">Create Project</a></li>
            <li><a href="#startShellScrapy">Start Shell</a></li>
            <li><a href="#startCrawlScrapy">Start Crawl</a></li>
        </ul>
    </li>
    <li><b>CSS</b>
        <ul>
            <li><a href="#hoverCSS">Hover CSS</a></li>
        </ul>
    </li>
</ul>

<section>
    <h2 id="usefulWebsite">Useful Websites</h2>
    <ul>
        <li>
            <a href="https://markdownlivepreview.com/" target=_blank>markdownlivepreview</a> : as the name said, live
            preview our markdown code (.md)
        </li>
        <li>
            <a href="https://www.cleanpng.com/" target=_blank>cleanpng</a> : transparent png images for your websites
        </li>
        <li>
            <a href="https://cssgr.id/" target=_blank>cssgr</a> : for rapid CSS grid layout
        </li>
        <li>
            <a href="https://www.colorsandfonts.com/" target=_blank>colorsandfonts</a> : color and typography Tools for
            web developer
        </li>
        <li>
            <a href="https://roadmap.sh/" target=_blank>roadmap</a> : developer roadmap
        </li>
    </ul>
</section>

<section id="nodeJS">
    <div id="initializeProjectNodeJS">
        <h2>NodeJS - Initialize Project</h2>
        <ul>
            <li>
                Initialize NPM
                <pre><code>npm init</code></pre>
            </li>
            <li>
                Initialize NPM with Yes to all question
                <pre><code>npm init -y</code></pre>
            </li>
        </ul>
    </div>
    <div id="gitignoreNodeJS">
        <h2>NodeJS - .gitignore</h2>
        <pre><code># Common
node_modules
build
npm-debug.log
.env
.DS_Store</code></pre>
    </div>
    <div id="deployToHerokuNodeJS">
        <h2>NodeJS - Deploy to HEROKU</h2>
        <ol>
            <li>
                Create Heroku project
                <pre><code>heroku create [PROJECT_NAME]</code></pre>
            </li>
            <li>
                Describe node file to run in <b>package.json</b> on <b>scripts</b> section
                <pre><code>"start": "node src/app.js"</code></pre>
            </li>
            <li>
                Check setting with command
                <pre><code>npm run start</code></pre>
            </li>
            <li>
                Change port at <b>app.js</b>
                <pre><code>const port = process.env.PORT || 3000
app.listen(port, () => {
    console.log('Server is up on port :3000. http://localhost:3000')
})</code></pre>
            </li>
            <li>
                Change localhost <b>base_url</b> if used in your project directory
            </li>
            <li>
                Set config on Heroku
                <pre><code>heroku config:set key=value</code></pre>
            </li>
            <li>
                Initialize git for heroku
                <br><code>git init</code>
                <br><code>heroku git:remote -a [PROJECT_NAME]</code>
                <br><code>git add .</code>
                <br><code>git commit -am "make it better"</code>
                <br><code>git push heroku master</code>
            </li>
        </ol>
    </div>
</section>

<section id="flutter">
    <div id="createProjectFlutter">
        <h2>Flutter - Create Project</h2>
        <pre><code>flutter create [PROJECT_NAME]</code></pre>
    </div>
    <div id="fontAssetsSize">
        <h2>Flutter - Font Assets Size</h2>
        <ul>
            <li>w100 Thin, the least thick</li>
            <li>w200 Extra-light</li>
            <li>w300 Light</li>
            <li>w400 Normal / regular / plain</li>
            <li>w500 Medium</li>
            <li>w600 Semi-bold</li>
            <li>w700 Bold</li>
            <li>w800 Extra-bold</li>
            <li>w900 Black, the most thick</li>
        </ul>
    </div>
    <div id="deployPlayStoreFlutter">
        <h2>Flutter - Deploy Google PlayStore</h2>
        <ul>
            <li>
                Set name of the app: <b>android:label</b>
                <code>android\app\src\main\AndroidManifest.xml</code>
            </li>
            <li>
                Set app permission. Example: <i><uses-permission android:name="android.permission.INTERNET"/></i>
                From: <code>android\app\src\debug\AndroidManifest.xml</code>
                To: <code>android\app\src\main\AndroidManifest.xml</code>
            </li>
            <li>
                Change package indetifier: <b>com.example.name_of_app</b> in all places
            </li>
            <li>
                Setup icons & splash screen
                <ul>
                    <li>Add <b>flutter_launcher_icons</b> package to dev_dependencies</li>
                    <li>Setup configuration on pubspec.yaml <b>flutter_icons</b>: image_path, adaptive_icon_background, adaptive_icon_foreground</li>
                    <li>
                        Generate icons using command
                        <code>flutter pub run flutter_launcher_icons:main</code>
                        The icon will be generated on directory: android\app\src\main\res (android)
                    </li>
                    <li>Configure booting app screen: <b>android\app\src\main\res\drawable\launch_background.xml</b></li>
                    <li>Edit color value: <b>android\app\src\main\res\values\colors.xml</b></li>
                    <li><a href="https://flutter.dev/docs/deployment/android" target="_blank" rel="noopener noreferrer">Sign keystore</a></li>
                    <li>key.properties on android folder</li>
                    <li>Configure signing in gradle</li>
                    <li>Change the version on pubspec.yaml</li>
                    <li>
                        Build app for production
                        <code>flutter build appbundle</code>
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</section>

<section id="react_js">
    <div id="createProjectReact">
        <h2>React JS - Create Project</h2>
        <pre><code>npx create-react-app [PROJECT_NAME]</code></pre>
        <b><i>optional:</i></b>
        <pre><code>npm i react-bootstrap react-icons react-router-dom react-dom redux react-redux redux-thunk</code></pre>
    </div>
    <div id="deployGithubPagesReactJS">
        <h2>React JS - Deploy to Github Pages</h2>
        <ol>
            <li>
                Create your github repository
            </li>
            <li>
                Add remote to your project
            </li>
            <li>
                Install gh-pages as devDependencies
                <pre><code>npm i gh-pages --save-dev</code></pre>
            </li>
            <li>
                Edit your <b>package.json</b> file, add <b>homepage</b> at top
                <pre><code>"homepage": "https://[GITHUB_USERNAME].github.io/[REPOSITORY_NAME]",</code></pre>
            </li>
            <li>
                Add this 2 lines of code on <b>package.json</b>, on <b>scripts</b>
                <pre><code>"predeploy": "npm run build",
"deploy": "gh-pages -d build",</code></pre>
            </li>
            <li>
                Run command
                <pre><code>npm run deploy</code></pre>
            </li>
            <li>
                Push your work to github
            </li>
            <li>
                If you are using <b>create-react-app</b> with <b>routing</b>. Try this: <a target='_blank' href='https://medium.com/@bennirus/deploying-a-create-react-app-with-routing-to-github-pages-f386b6ce84c2'>Referrence</a>
                <pre><code>import { Route, HashRouter } from "react-router-dom";
function App() {
	return (
		< HashRouter basename="/">
			< Route exact path="/" component={HomePage} />
			< Route path="/about" component={AboutPage} />
		< /HashRouter>
	);
}</code></pre>
            </li>
        </ol>
    </div>
    <div id="routerDOMNetlifySettingReactJS">
        <h2>React JS - Router DOM Netlify Setting</h2>
        <ol>
            <li>Create a file with name <b>netlify.toml</b> on your root folder</li>
            <li>
                Add this code
                <pre><code>[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200
  force = false</code></pre>
            </li>
        </ol>
    </div>
</section>

<section id="react_native">
    <div id="createProjectRN">
        <h2>React Native - Create Project</h2>
        <pre><code>expo init [PROJECT_NAME]</code></pre>
    </div>
</section>

<section id="laravel">
    <div id="createProjectLaravel">
        <h2>Laravel - Create Project</h2>
        <pre><code>composer create-project --prefer-dist laravel/laravel [PROJECT_NAME]</code></pre>
    </div>
    <div id="startServerLaravel">
        <h2>Laravel - Start Server</h2>
        <pre><code>php artisan serve</code></pre>
    </div>
    <div id="artisanMakeMigration">
        <h2>Laravel - Make Migration</h2>
        <pre><code>php artisan make:migration [METHOD_NAME]</code></pre>
        example: <code>php artisan make:migration create_users_table --create="users"</code>
        <br>
        example: <code>php artisan make:migration add_votes_to_users_table --table="users"</code>
    </div>
    <div id="artisanMigrate">
        <h2>Laravel - Migrate</h2>
        <pre><code>php artisan migrate</code></pre>
    </div>
</section>

<section id="lumen">
    <div id="createProjectLumen">
        <h2>Lumen - Create Project</h2>
        <pre><code>composer create-project — prefer-dist laravel/lumen [PROJECT_NAME]</code></pre>
    </div>
    <div id="startServerLumen">
        <h2>Lumen - Start Server</h2>
        <pre><code>php -S localhost:8000 -t public</code></pre>
    </div>
</section>

<section id="docker">
    <div id="dockerfiletemplate">
        <h2>Docker - Dockerfile Template</h2>
        <pre><code>FROM node<br>
WORKDIR /app<br>
COPY . /app<br>
RUN npm install<br>
EXPOSE 80<br>
CMD [ "node", "server.js" ]</code></pre>
    </div>
    <div id="buildContainerDocker">
        <h2>Docker - Build Custom Image</h2>
        <pre><code>docker build .</code></pre>
    </div>
    <div id="runBasedOnImage">
        <h2>Docker - Run Container Based on Image</h2>
        <pre><code>docker run -p 3000:80 [IMAGE_ID]</code></pre>
    </div>
    <div id="getRunningProcessDocker">
        <h2>Docker - Get Running Container Process</h2>
        <pre><code>docker ps</code></pre>
    </div>
    <div id="stopProcessDocker">
        <h2>Docker - Stop Running Container Process</h2>
        <pre><code>docker stop [CONTAINER_NAME]</code></pre>
    </div>
</section>

<section id="scrapy">
    <div id="createProjectScrapy">
        <h2>Scrapy - Create Project</h2>
        <pre><code>scrapy startproject [PROJECT_NAME]</code></pre>
    </div>
    <div id="startShellScrapy">
        <h2>Scrapy - Start Shell</h2>
        <pre><code>scrapy shell [URL]</code></pre>
    </div>
    <div id="startCrawlScrapy">
        <h2>Scrapy - Start Crawl</h2>
        <pre><code>scrapy crawl [SPIDER_NAME]</code></pre>
    </div>
</section>

<section id="css">
    <div id="hoverCSS">
        <h2>CSS - Hover CSS</h2>
        If the cube is directly inside the container:
        <pre><code>#container:hover > #cube { background-color: yellow; }</code></pre>
        If cube is next to (after containers closing tag) the container:
        <pre><code>#container:hover + #cube { background-color: yellow; }</code></pre>
        If the cube is somewhere inside the container:
        <pre><code>#container:hover #cube { background-color: yellow; }</code></pre>
        If the cube is a sibling of the container:
        <pre><code>#container:hover ~ #cube { background-color: yellow; }</code></pre>
    </div>
</section>
