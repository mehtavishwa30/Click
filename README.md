# Click
Click - Python library for Command Line Interfaces

Click is a Python package for creating beautiful command line interfaces in a composable way with as little code as necessary.

Sample code for Click:

    import click

    @click.command()
    @click.option('--count', default=1, help='Number of greetings.')
    @click.option('--name', prompt='Your name',
                  help='The person to greet.')
    def hello(count, name):
        """Simple program that greets NAME for a total of COUNT times."""
        for x in range(count):
            click.echo('Hello %s!' % name)

    if __name__ == '__main__':
        hello()
    
    
Outpt of the sample code:

    $ python hello.py --count=3
    Your name: John
    Hello John!
    Hello John!
    Hello John!
    
It also produces nicely formatted help pages by deafult:
    
    $ python hello.py --help
    Usage: hello.py [OPTIONS]

    Simple program that greets NAME for a total of COUNT times.

    Options:
    --count INTEGER  Number of greetings.
    --name TEXT      The person to greet.
    --help           Show this message and exit.
