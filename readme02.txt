import json

import requests
for i in range(10000):
    data1 = {'resp': '{}'.format(i), 'url': '111'}
    json_ = {'data': json.dumps(data1)}
    # resp = requests.post('http://127.0.0.1:5555/girl',data=json.dumps(data))
    resp = requests.post('http://127.0.0.1:5555/json', json=json_)
    print(resp.text)
    print('-'*100)
    data2 = {'resp': '{}'.format(i*i), 'url': '222'}
    json_ = {'data': json.dumps(data2)}
    resp = requests.post('http://127.0.0.1:5555/json', json=json_)
    print(resp.text)
    print('-'*100)
    data3 = {'resp': '222', 'url': '999'}
    json_ = {'data': json.dumps(data3)}
    resp = requests.post('http://127.0.0.1:5555/json', json=json_)
    print(resp.text)
