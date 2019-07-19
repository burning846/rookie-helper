# Multiprocessing



在多核服务器上多进程分块处理一批很大的数据，可以极大地提高运行效率。

### Example

```python
import multiprocessing as mp

def job(q, data):
    res = data # process data
    q.put(res)    

q = mp.Queue() # queue
process_cnt = 16 # num of processes
processes = []
result = []
data_len = 1000 # length of data
data = [x for x in range(data_len)]
part_len = data_len // process_cnt

# create processes and start
for i in range(process_cnt):
    if i == process_cnt - 1:
    	part_data = data[part_len*i:]
    else:
        part_data = data[part_len*i:part_len*(i+1)]
    p = mp.Process(target=job,args=(q, data[data_len], ))
    p.start()
    processes.append(p)
    
# wait for end
for i in range(process_cnt):
    processes[i].join()
    res = q.get()
    result.append(res)

# process all result
print(result)
```

