
# INSTALLATION

Installation is the same as any vim syntax file, and is not complex. Move the
`Whiley.vim` file to

    $VIMRUNTIME/syntax/Whiley.vim

for a system wide install, or to

    ~/.vim[files]/syntax/Whiley.vim

for a single user install. NOTE: You may have to create the `syntax/` directory
in your `~/.vim/` directory.

Once you have moved the syntax file into the correct directory, open up your
`.vimrc` and add the following line:

    "Recognize whiley file type
    augroup filetypedetect
    au BufNewFile,BufRead *.whiley  setf whiley
    augroup END


this should set everything up properly, so that you can see Whiley syntax
highlighting in `.whiley` files.

To enable highlighting of trailing whitespace, and tabs mixed with spaces, type
the following into vim:

    :let whiley_space_error_highlighting=1
    :set syntax=whiley

To disable it again, type this:

    :unlet whiley_space_error_highlighting
    :set syntax=whiley

The reason you have to type `:set syntax=whiley` each time is to force vim to
reload the syntax definitions from file, and rehighlight the contents of the
buffer.
