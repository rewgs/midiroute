# midiroute

`midiroute` is a wonderful little package I found on [PyPi](https://pypi.org/project/midiroute/) that allows you to route one MIDI port to another, and optionally monitor the data.

I did not write this -- all credit goes to user atticave. I would have forked it, but it appears that its GitHub repo has been deleted, and I can't find any other git repo or even the original author anywhere. So, I `pip install`'d the package and copied the source code.

I plan to add some features, such as CC/note filtering, MIDI scaling, etc.

## Description (original README)

`midiroute` is a command line utility for routing MIDI streams between input and output ports on your computer. `midiroute` can route an incoming MIDI stream to multiple output ports. The stream can also be monitored in the terminal.

### Installation and usage

#### Installation

`pip install midiroute`

`midiroute` requires Python 3.8.0 or later.

#### Usage

To list the available input and output ports on your system:

`midiroute list-ports`

Route messages from an input to an output port with monitoring enabled:

`midiroute run -i "Oxygen 61 0" -o "Microsoft GS Wavetable Synth 0" -m`

#### Command line options

You can list the command line options by running `midiroute --help`:

```bash

Usage: midiroute [OPTIONS] COMMAND [ARGS]...

  CLI entry-point.

Options:
  --help  Show this message and exit.

Commands:
  list-ports  List available input and output ports.
  run         Run the MIDI router.
```

To get help on a specific command run `midiroute <command> --help`:

```bash
$ midiroute run --help
Usage: midiroute run [OPTIONS]

  Run the MIDI router.

Options:
  -i, --input-port PORT_NAME    Select the input port.
  -o, --output-ports PORT_NAME  Select one or more output ports in a comma
                                separated list.
  -m, --monitor                 Enable monitoring of MIDI activity on the
                                selected ports.
  --help                        Show this message and exit.
```

### License

MIT
