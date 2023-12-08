# StreamDiffusionLeaked
10ms, sd-turbo, 512x512, batch size 1, txt2img on consumer hardware

Sucks doesn't it.

Various AI demos on the socials, whitepapers with code "coming soon".

The community has two main issues here that need to be addressed;

- Proof of concept or GTFO
- Python devs really need to add the Python version to their documentation, but seem incapable to do so

That's all. Below is a guide for newcomers and developers in the space.


## Guide to setting up an AI Python project

### The problem
For those that are new to Python, there exists many different versions of it.

Often you will pick up a 3rd party repository from Github here, and will be instructed to run the following;

```bash 
pip install requirements.txt
```

The problem here is that the modules listed in the requirements have only been tested on one of the many different versions of Python.
If the developer hasn't listed which version, you may be banging your head on a wall for some time.

### The solution

You can create a "virtual environment" for a project by using `conda` or `venv`, effectively creating a sandbox for that version.

Determine from the readme (good luck with that), or raise a github issue asking which version of Python the author used.

Install that version of Python on your system.

Now leverage `venv` to target that version of Python. 

Reviewed on Ubuntu, will probably work for Macs and Windows(WSL).

```bash
# observe the path of python binary of your system-wide install
which python
# target the python version and create the virtual environment
python3.8 -m venv ./.venv
# activate the virtual environment
source ./.venv/bin/activate
# observe the path of python binary contained within your virtual environment
which python
# now install the intended requirements for the intended version
pip install -r requirments.txt
```