Simple plugin that uses Conque-Shell to run tests from a grails app. To use this
you need to have conque-shell installed beforehand. I recommend using [pathogen](https://github.com/tpope/vim-pathogen "Pathogen").

If thats the case you can do:
<code>
cd ~/.vim/bundle
git clone https://github.com/rosenfeld/conque-term.git
git clone https://github.com/hoffoo/vim-grails-console.git
</code>

You can either run the entire file or the test function under your cursor. 

Example mappings:

To start the grails shell - 
<code>:StartGrailsConque</code>

Map to run the whole file - 
<code>map <F12> :RunGrailsTestFile</code>


Map to run the Test under the cursor -
<code>map <F11> :RunSingleGrailsTest</code>

You can also override the shell name and the path to the executable using:

<code>let g:GrailsShellName = "grails"</code>
<code>let g:GrailsShellExecutable = "grails"</code>

By default they are both grails - name will be the buffer name and executable
can be the full path.

![Screenshot](http://i.imgur.com/eOxz0d3.png)

TODO:

- Easy close of the buffer after it has exited
- Search upwards if we are in a sub directory of a grails project

Resources:
http://www.objectpartners.com/2012/02/28/using-vim-as-your-grails-ide-part-2/ - mostly modified the test script from here
