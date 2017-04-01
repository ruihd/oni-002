
#include <iostream>
#include <vector>


using namespace std;

int main() {

    int N;
    char lado;
    int n;
    int l;
    int K;
    int c;
    int I;
    char b;
    char y = 'T';
    vector<int> k;
    cin >> N >> K >> I;
    for (int a = 0; a < N; a++){
        cin >> b;
        if(b == y){
            c = 1;
        }
        else{
            c = 0;
        }
        k.push_back(c);
    }
    l = K;
    int soma = k[K -1];
    k[K -1] = 0;
    for(int d = 0; d < I; d++){
        cin >> lado >> n;
        if(lado == 'E'){
            n = n*-1;
        }
        l = l + n;
        soma = soma + k[l -1];
        if (k[l -1] == 1){
            k[l -1] = 0;
        }
    }
    cout << soma << endl;
	return 0;
}



#include <iostream>
#include <vector>
using namespace std;

int main() {
    
    int N;
    int Q;
    cin >> N >> Q;
    int x;
    int p;
    int l;
    int total = 0;
    vector<int> n;
    for(int a = 0; a < N*4; a++){
        cin >> x; 
        n.push_back(x);
    }
    for(int b = 0; b < Q; b++){
        cin >> p;
        for(int c = 0; c < N; c++){
            if(p < n[c*4+2] && p >= n[c*4]){
            l = n[c*4+3] - n[c*4+1];
            total = total + l;
            }
        }
        cout << total << endl;
        total = 0;
    }
	return 0;
}
