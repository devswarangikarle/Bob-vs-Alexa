# Bob-vs-Alexa

#include <iostream>
#include <string>

using namespace std;

bool isSubsequence(const string& A, const string& B) {
    int m = A.length();
    int n = B.length();
    int i = 0, j = 0;

    while (i < m && j < n) {
        if (A[i] == B[j]) {
            j++;
        }
        i++;
    }

    return (j == n);
}

int main() {
    string A, B;

    // Input
    getline(cin, A);
    getline(cin, B);

    // Output
    if (isSubsequence(A, B)) {
        cout << "Yes" << endl;
    } else {
        cout << "No" << endl;
    }

    return 0;
}
