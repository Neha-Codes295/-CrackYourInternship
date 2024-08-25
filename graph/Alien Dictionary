class Solution {
  public:
    string findOrder(string dict[], int n, int k) {
        //build graph
        vector<int> vis(26, 0);
        vector<unordered_set<int>> adj(26);
        
        for (int i = 0; i < n - 1; i++) {
            int sz = min(dict[i].size(), dict[i + 1].size());
            for (int j = 0; j < sz; j++) {
                if (dict[i][j] != dict[i + 1][j]) {
                    int u = dict[i][j] - 'a';
                    int v = dict[i + 1][j] - 'a';
                    if (adj[u].find(v) == adj[u].end()) {
                        adj[u].insert(v);
                    }
                    break;
                }
            }
        }
        // Perform topological sorting using BFS
        vector<int> indegree(26, 0);
        for (int i = 0; i < 26; i++) {
            for (int j : adj[i]) {
                indegree[j]++;
            }
        }
        
        queue<int> q;
        for (int i = 0; i < 26; i++) {
            if (indegree[i] == 0) {
                q.push(i);
            }
        }
        
        string order;
        while (!q.empty()) {
            int node = q.front();
            q.pop();
            order += 'a' + node;
            for (int neighbor : adj[node]) {
                indegree[neighbor]--;
                if (indegree[neighbor] == 0) {
                    q.push(neighbor);
                }
            }
        }
        
        return order;
    }
};
