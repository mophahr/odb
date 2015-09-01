###installation:
	virtualenv opendata_environment
	source opendata_environment/bin/activate
	pip install ipython[notebook] matplotlib numpy scipy pandas redis statsmodels nose seaborn bokeh
	mkdir ./.ipython
	export IPYTHONDIR=./.ipython
	ipython profile create
	chmod +x run_ipynb.sh
	deactivate

Now create your list of apikeys:
	
	mkdir ./.private
	touch ./.private/apikeys.py

This is where you store all your apikeys. The file should contain entries like this example:

	openweathermap = "55cXXXXXXXXXXXXXXXXXXXXXXXXXX007"	

###running the notebooks:
	source opendata_environment/bin/activate
	./run_ipynb.sh
