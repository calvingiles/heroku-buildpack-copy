# heroku-buildpack-copy

Add support for file-based config files.

This borrows heavily from [ddollar/heroku-buildpack-apt](https://github.com/ddollar/heroku-buildpack-apt) and is designed to work alongside it.

## Usage

This buildpack works best with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) so that it can be used with your app's existing buildpacks.

Include a list of files and destinations to copy in a file names `Copyfile`.

## Example

#### .buildpacks

    https://github.com/calvingiles/heroku-buildpack-copy
    https://github.com/ddollar/heroku-buildpack-apt
    https://github.com/heroku/heroku-buildpack-python

#### Copyfile

    freedts.conf:/etc/freetds/
    odbcinst.ini:/etc/
    odbc.ini /etc/

#### Aptfile

    unixodbc
    unixodbc-dev
    freetds-dev
    tdsodbc

#### requirements.txt

    https://pyodbc.googlecode.com/files/pyodbc-3.0.7.zip

## License

MIT
