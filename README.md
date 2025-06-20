# setup-python-win7

GitHub action that sets up a Windows7–compatible version of Python.

## Usage

```yaml
- name: Setup Python for Windows7  
  uses: LorenEteval/setup-python-win7@v1
  with:
    # required: "3.x" or "3.x.y"
    python-version: "3.11"
    # optional: freethreaded version or not, default is false
    freethreaded: false
    # optional: amd64 or arm64, default is amd64. 
    architecture: amd64
    # optional: setup python for windows7 from this repo
    github-repo: adang1345/PythonWin7
    # optional: setup python for windows7 from this repo branch
    github-repo-branch: "master"
- name: Check Python for Windows7 version
  shell: bash
  run: |
    echo $PYTHON_WIN7_HOME
    python -c "import sys; print(sys.version)"
```
