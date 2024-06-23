# sdk_practice
Learning how to create an SDK and publish it on PyPi


Steps
- Do all the necessary stuff to build the sdk using poetry
    - Be sensitive to the difference between poetry add <dependency> and poetry add --dev <dev-dependency>
- Make sure pyproject.toml [tool.poetry] look like what it is here
- `poetry build`
- Test whether the .whl file can be installed locally `pip install dist/my_sdk-0.1.0-py3-none-any.whl`
- `poetry config pypi-token.pypi <your-pypi-token>`
- poetry publish --build
- Verify installing from PyPI somewhere else (poetry add <sdk_name>/pip install <sdk_name>)

Maintenance
- Increment the version number in `pyproject.toml` and repeat the build and publish steps to release updates


