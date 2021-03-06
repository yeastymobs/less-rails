# less-rails

Plugin for Rails to automatically generate css templates out of less (http://www.lesscss.org) templates.

For this to work you need to have the less gem:

<pre><code>sudo gem install less</code></pre>

This plugin provides you with some configuration options that can be set in either an initializer or an environment file.
The options can be set like this:

<pre><code>Less::Plugin.options[:template_location] = "#{RAILS_ROOT}/app/stylesheets"
Less::Plugin.options[:css_location] = "#{RAILS_ROOT}/public/stylesheets"
Less::Plugin.options[:update] = :when_changed
Less::Plugin.options[:compress] = false</code></pre>

A quick description of the options:

 * :template_location is the location where the *.less files are to be found.
 * :css_location is the location where the generated *.css files are to be put.
 * :update defines when to update the *.css files, you have three options:
   * :never : never update the css files automatically.
   * :when_changed : update the css files when the corresponding less file is newer than the generated css file.
   * :always : update the css files on every request.
 * :compress : turns less's built-in compress functionality on or off.

The options as listed in the example code are the defaults that less-rails uses.

# Contributors

* Karst Hammer
* Mathieu Fosse
* Nicolas Mérouze
* Tim Harvey

# License

Copyright (c) 2009, Karst Hammer <karst (at) motorzweefschool (dot) demon (dot) nl>
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.