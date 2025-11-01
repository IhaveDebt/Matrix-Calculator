#include <iostream>
#include <vector>
using namespace std;

vector<vector<int>> add(const vector<vector<int>>& A, const vector<vector<int>>& B) {
    vector<vector<int>> C(A.size(), vector<int>(A[0].size()));
    for (size_t i = 0; i < A.size(); i++)
        for (size_t j = 0; j < A[0].size(); j++)
            C[i][j] = A[i][j] + B[i][j];
    return C;
}

void display(const vector<vector<int>>& M) {
    for (auto& row : M) {
        for (auto& val : row) cout << val << " ";
        cout << endl;
    }
}

int main() {
    vector<vector<int>> A = {{1,2,3},{4,5,6},{7,8,9}};
    vector<vector<int>> B = {{9,8,7},{6,5,4},{3,2,1}};
    auto C = add(A,B);
    cout << "Matrix Addition Result:\n";
    display(C);
}
