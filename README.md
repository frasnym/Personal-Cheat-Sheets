# Personal Cheat Sheets

<ul>
    <li><b>Useful Websites</b>
        <ul>
            <li><a href="#usefulWebsite">Useful Websites</a></li>
        </ul>
    </li>
    <li><b>Flutter</b>
        <ul>
            <li><a href="#fontAssetsSize">Font Assets Size</a></li>
        </ul>
    </li>
    <li><b>Laravel</b>
        <ul>
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

<h2 id="usefulWebsite">Useful Websites</h2>
<ul>
    <li>
        <a href="https://markdownlivepreview.com/" target=_blank>markdownlivepreview</a> : as the name said, live preview our markdown code (.md)
    </li>
    <li>
        <a href="https://www.cleanpng.com/" target=_blank>cleanpng</a> : transparent png images for your websites
    </li>
    <li>
        <a href="https://cssgr.id/" target=_blank>cssgr</a> : for rapid CSS grid layout
    </li>
    <li>
        <a href="https://www.colorsandfonts.com/" target=_blank>colorsandfonts</a> : color and typography Tools for web developer
    </li>
</ul>


<h2 id="fontAssetsSize">Flutter - Font Assets Size</h2>

* w100 Thin, the least thick
* w200 Extra-light
* w300 Light
* w400 Normal / regular / plain
* w500 Medium
* w600 Semi-bold
* w700 Bold
* w800 Extra-bold
* w900 Black, the most thick

<h2 id="artisanStartProject">Laravel - Start Server</h2>
<pre><code>php -S localhost:8000 -t public</code></pre>

<h2 id="artisanMakeMigration">Laravel - Make Migration</h2>
<pre><code>php artisan make:migration [METHOD_NAME]</code></pre>
example: <code>php artisan make:migration create_users_table --create="users"</code>
<br>
example: <code>php artisan make:migration add_votes_to_users_table --table="users"</code>

<h2 id="artisanMigrate">Laravel - Migrate</h2>
<pre><code>php artisan migrate</code></pre>

<h2 id="createProjectLumen">Lumen - Create Project</h2>
<pre><code>composer create-project — prefer-dist laravel/lumen [PROJECT_NAME]</code></pre>
