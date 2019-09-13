postfix=-template

main: ${postfix} 

${postfix}: master${postfix}.ipynb
	./sep.py master${postfix}.ipynb

strip:
	nbstripout *${postfix}.ipynb

clean:
	rm -f solution${postfix}.ipynb
	rm -f assignment${postfix}.ipynb
