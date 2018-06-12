# the-longest-sequence
finds the length of the longest sequence with '1' in a row

#include <iostream>

using namespace std;

int main(){
	
	FILE* input = fopen("INPUT.TXT", "r");
	FILE* output = fopen("OUTPUT.TXT", "w");
	
	int count = 0, ans = 0;
	char c;
	while (fscanf(input, "%c", &c) != EOF){
		
		if (c == '1'){
			
			count++;
			if (count > ans) ans = count;
		}
		else count = 0;
	}
	
	fprintf(output, "%d", ans);
	
	fclose(input);
	fclose(output);
}
