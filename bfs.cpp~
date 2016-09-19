#include<iostream>


using namespace std;

#define max 10

int adj[max] [max];

class graph
{
	char vertex[max],visited[max];
	public:
	void creategraph(int);
	void breadthfirst(int);
	void depthfirst(int);
	void dfs(int,int);
};

void graph::creategraph(int v)
{
	int i,j;
	for(i=0;i<v;i++)
	{
		cout<<"\n\tEnter the node value:";
		cin>>vertex[i];
		visited[i]=0;
	}
	cout<<endl;
	cout<<"\n\tEnter the adjacement vertex list for each vertex of the graph";
	int n,k;
	for(i=0;i<v;i++)
	{
		cout<<"\n\tEnter the no of adjecent nodes for the vertex:";
		cout<<vertex[i]<<":";
		cin>>n;
		for(j=0;j<n;j++)
		{
			cout<<"\n\tEnter the adjecent nodes:";
			cin>>k;
			adj[i+1][k+1]=1;
		}
	}
	cout<<"\n\tGraph with no of nodes="<<v;
	cout<<"\n\tThe adjecent matrix"<<"\n\n";
	for(i=0;i<v;i++)
	{
		for(j=0;j<v;j++)
			cout<<adj[i][j]<<"\t";
			cout<<endl;
	}	
}

void graph::breadthfirst(int v)
{
	int i,j;
	for(i=0;i<v;i++)
	visited[i]=0;
	cout<<"\n\tBreadfirst Traversal:";
	cout<<vertex[0]<<"==>";
	visited[0]=1;
	for(i=0;i<v;i++)
		for(j=0;j<v;j++)
			if(adj[i][j]==1)
				if(visited[j]==0)
				{
					cout<<vertex[j]<<"==>";
					visited[j]=1;
				}
}

void graph::depthfirst(int v)
{
	int i;
	for(i=0;i<v;i++)
		visited[i]=0;
	cout<<"\n\tDepthfirst Traversal:";
	cout<<vertex[0]<<"==>>";
	visited[0]=1;
	dfs(0,v);
}

void graph::dfs(int ad,int v)
{
	int i,j;
	for(i=ad;i<v;i++)
		for(j=0;j<v;j++)
			if(adj[i][j]==1)
				if(visited[j]==0)
				{
					visited[j]=1;
					cout<<vertex[j]<<"==>>";
					dfs(j,v);
				}
}

int main()
{
	graph g;
	int ch,v;
	
	cout<<"\n\tGraph Traversal"<<endl;
	cout<<"\n\t*************************"<<endl;
	cout<<"\n\t1.Create Graph";
	cout<<"\n\t2.Breathfirst Traversal";
	cout<<"\n\t3.Depthfirst Traversal";
	cout<<"\n\t4.Exit";
	do
	{
		cout<<"\n\tEnter your choice:";
		cin>>ch;
	switch(ch)
	{
		case 1:
				cout<<"\n\tGraph creation";
				cout<<"\n\t*************";
				cout<<"\n\tEnter the no of vertices to be created:";
				cin>>v;
				g.creategraph(v);
				
				break;
		case 2:
				g.breadthfirst(v);
				
				break;
		case 3:
				g.depthfirst(v);
				
				break;
		case 4:
				break;
	}
	}while(ch!=4);

	return 0;
}