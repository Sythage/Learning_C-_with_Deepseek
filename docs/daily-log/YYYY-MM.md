## 2023-09-15
### 今日进展
- [x] 完成LeetCode #215 堆排序实现
- [ ] 调试多线程死锁问题

### 代码片段
```cpp
// 快速选择算法实现
int findKthLargest(vector<int>& nums, int k) {
    priority_queue<int, vector<int>, greater<int>> pq;
    for (int num : nums) {
        pq.push(num);
        if (pq.size() > k) pq.pop();
    }
    return pq.top();
}
```

### 遇到的问题
在Linux环境下编译时出现undefined reference错误
- 解决方案：检查CMake链接顺序

