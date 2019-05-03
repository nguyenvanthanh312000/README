//cho  n bai hat , het dung luong cua moi bai
// bh : 0     1    2      3       4       5        6      7 
// dl : 150  200  240     50      90      10     45     190
// moi dia CD co dung luong P = 210
// - Hãy luu cac bhat len it dia CD nhat
// - Moi bai hat thi nam trong trong 1 dia

#include <stdio.h>
#include <conio.h>

int bh[]={120,400,300,150,280,50,70,130};
int n= sizeof(bh)/sizeof(bh[0]);

int ten[100]; //Ten bai hat
int bhd[100]; // bhd[i]=j bai hat i ghi o dia j

int M=410; // dung luong 1 dia
int dg[100]; // so dia toi thieu 
int sd=0; // ghi nhan trang thai bai hat (=1 : bai hat da duoc ghi)

int main()
{
	int i,j,tam;int d=0;
	int du=0;
	//gan ten cac bai hat
	for(i=0;i<n;i++)
		ten[i]=i;
	//sapxep theo thu tu dung luong giam dan
	for(i=0;i<n-1;i++)
		for(j=i+1;j<n;j++)
			if(bh[ten[i]]<bh[ten[j]])
			{
				tam=ten[i];
				ten[i]=ten[j];
				ten[j]=tam;
			}
	for(i=0;i<n-1;i++)
	{
		d=d+1;
		dg[ten[i]]=1;
		bhd[ten[i]]=d;
			du=M-bh[ten[i]];
		for(j=i+1;j<n;j++)
		{
			if((bh[ten[j]]<=du)&&(dg[ten[j]]==0))
			{
				dg[ten[j]]=1;
				bhd[ten[j]]=d;
				du=du-bh[ten[j]];
			}
		}
	}
	for(j=0;j<n;j++)
	{
		printf("\nBai %d, dia %d", ten[j],bhd[ten[j]]);
	}
	printf("\n So dia %d",d);
	getch();
	return 0;
}
