class Solution {
  public:
    // Function to return Breadth First Traversal of given graph.
    vector<int> bfsOfGraph(int V, vector<int> adj[]) {
        // Code here
        vector<int>solution;
        queue<int>q;
        q.push(0);
        vector<bool>vis(V,false);
        vis[0]=true;
        while(!q.empty())
        {
            int node = q.front();
            q.pop();
            solution.push_back(node);
            
            for(int a :adj[node])
            {
                if(!vis[a])
                {
                    q.push(a);
                    vis[a]=true;
                }
            }
        }
        return solution;
    }
};
