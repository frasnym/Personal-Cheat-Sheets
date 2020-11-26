# Personal Cheat Sheets

<ul>
    <li><b>Useful Websites</b>
        <ul>
            <li><a href="#usefulWebsite">Useful Websites</a></li>
        </ul>
    </li>
    <li><b>NodeJS</b>
        <ul>
            <li><a href="#initializeProjectNodeJS">Initialize Project</a></li>
            <li><a href="#deployToHerokuNodeJS">Deploy to HEROKU</a></li>
        </ul>
    </li>
    <li><b>Flutter</b>
        <ul>
            <li><a href="#createProjectFlutter">Create Project</a></li>
            <li><a href="#fontAssetsSize">Font Assets Size</a></li>
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
            <li><a href="#artisanStartProject">Start Server</a></li>
            <li><a href="#artisanMakeMigration">Make Migration</a></li>
            <li><a href="#artisanMigrate">Migrate</a></li>
        </ul>
    </li>
    <li><b>Lumen</b>
        <ul>
            <li><a href="#createProjectLumen">Create Project</a></li>
        </ul>
    </li>
</ul>

<section id="usefulWebsite">
    <h2>Useful Websites</h2>
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
    <div id="artisanStartProject">
        <h2>Laravel - Start Server</h2>
        <pre><code>php -S localhost:8000 -t public</code></pre>
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
</section>
