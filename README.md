# student-list

if [ "$(curl -X GET http://172.18.0.1:80/health)" = "ok" ]; then echo "test OK"; exit 0; else echo "test KO"; exit 1; fi

00 -Pour student-list
if [ "$(curl -u toto:python -X GET http://172.31.57.44:800/pozos/api/v1.0/get_student_ages | python 
	 -c "import sys, json; print json.load(sys.stdin)['student_ages']['bob']")" = "13" ] &&
	 [ "$(curl -u toto:python -X GET http://172.17.0.1:5000/pozos/api/v1.0/get_student_ages | python
	 -c "import sys, json; print json.load(sys.stdin)['student_ages']['alice']")" = "12" ]; 
	 then echo "test OK"; exit 0; else echo "test KO"; exit 1; fi
