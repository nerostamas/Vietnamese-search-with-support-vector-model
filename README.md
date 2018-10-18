# Simple search engine with python 3
# University Of Information Technology - Ho Chi Minh National University

This mini project will implement a simple search engine using Vector Space Model. The data will be crawled from Vietnamese daily news such as [VnExpress](https://vnexpress.net/), [VietnamNet](http://vietnamnet.vn/), [Thanhnien](https://thanhnien.vn/) and [Laodong](https://laodong.vn/).

## Tools

- Install [Python 3.5+](https://www.python.org/) and [Pip](https://pypi.org/project/pip/) if not installed.
- Use `pip` to install following packages:
    - [`requests`](http://docs.python-requests.org/en/master/) (for making HTTP requests).
    - [`underthesea`](https://github.com/magizbox/underthesea) (Vietnamese NLP toolkit).
    - [`beautifulsoup4`](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) (for parsing HTML and XML).

    ```bash
    $ pip install requests underthesea beautifulsoup4 lxml
    ```

- (Optional) Install `pytest` to run unit tests:

    ```bash
    $ pip install pytest
    $ cd /path/to/project
    $ pytest
    ```

- Install [git](https://git-scm.com/) and clone this project into local machine:

    ```bash
    $ git clone https://github.com/vancanhuit/simple-search-engine.git
    $ cd simple-search-engine
    ```

    > Note: If you run this project on Windows, you must checkout to `windows` branch. This is due to cross-platform issues of [shelve](https://docs.python.org/3/library/shelve.html) module in python (see this [issue](https://stackoverflow.com/questions/8704728/using-python-shelve-cross-platform)):

    ```bash
    $ git checkout windows
    ```

## Usage

- Run `index.py` script to perform indexing data. The indexed data will be created (if not exists) or updated and stored in `db/` directory.

    ```bash
    $ python index.py
    ```

- Run `search.py` script and pass a query string for it.

    ```bash
    $ python search.py "Your query string here"
    ```

    For example:

    ```bash
    $ python search.py "your key words"