# testdriven.io-blog-modern-tdd-testdriven.io-blog-modern-tdd-Real-Application-blog_app

## Coverage

Now, with our application tested, it's the time to check code coverage. So let's install a pytest plugin for coverage called pytest-cov:

```bash
(venv) yusuke.sato@app-0001-dev ~/courses/testdriven.io/blog/modern-tdd/Real-Application/blog_app (main) 
$ pip install pytest-cov
```

After the plugin is installed, we can check code coverage of our blog application like this:

```python
(venv) yusuke.sato@app-0001-dev ~/courses/testdriven.io/blog/modern-tdd/Real-Application/blog_app (main) 
$ python -m pytest tests --cov=blog
=============================================================================================== test session starts ===============================================================================================
platform linux -- Python 3.8.6, pytest-6.2.2, py-1.10.0, pluggy-0.13.1
rootdir: /home/ys-office.me/yusuke.sato/courses/testdriven.io/blog/modern-tdd/Real-Application/blog_app/tests, configfile: pytest.ini
plugins: cov-2.11.1
collected 10 items                                                                                                                                                                                                

tests/test_article/test_app.py ......                                                                                                                                                                       [ 60%]
tests/test_article/test_commands.py ..                                                                                                                                                                      [ 80%]
tests/test_article/test_queries.py ..                                                                                                                                                                       [100%]

----------- coverage: platform linux, python 3.8.6-final-0 -----------
Name               Stmts   Miss  Cover
--------------------------------------
blog/__init__.py       0      0   100%
blog/app.py           25      1    96%
blog/commands.py      16      0   100%
blog/models.py        57      1    98%
blog/queries.py       12      0   100%
--------------------------------------
TOTAL                110      2    98%


=============================================================================================== 10 passed in 0.40s ================================================================================================
```
