## grep -r Recursive
To search all files in all subdirectories of a folder using -r
```
grep chemical -r berlitz1
```
![image](https://user-images.githubusercontent.com/53378715/218615561-51205ec5-db3a-41c1-a4eb-813a08fbdc77.jpeg)

```
grep Municipal -r berlitz2
```
![image](https://user-images.githubusercontent.com/53378715/218615548-c004efa4-3b2c-4094-b066-f73c8e868963.jpeg)


## grep -r -i
Sometimes you don't care whether a string is lowercase or uppercase using -i for case-insentivity
```
grep Inspector -i -r berlitz2
```
![image](https://user-images.githubusercontent.com/53378715/218615214-56da8c56-6bd9-475e-83a6-6f4a7fcac450.jpeg)

```
grep ecological -i -r berlitz1
```
![image](https://user-images.githubusercontent.com/53378715/218615192-9a16b932-c65c-456d-8146-26d7411e74b7.jpeg)

## grep -r -l (File with Matches)
You can get just teh file's name that containes matches with -l

```
grep science -r -l berlitz1
```
![image](https://user-images.githubusercontent.com/53378715/218614848-ade279cd-cb3d-4961-a64e-4dfba5e91fdf.jpeg)

```
grep agriculture -r -l berlitz1
```
![image](https://user-images.githubusercontent.com/53378715/218615970-4f9bf000-123f-462b-9a41-9f5f3d848ced.jpeg)

 
## grep -r -o
The -o option prints only the matching part of a line
```
grep -r -o life Rybczynski
```
![image](https://user-images.githubusercontent.com/53378715/218614130-96b77b6e-cd77-4535-83c5-48a006758b7e.jpeg)

```
grep -r -o ancient Fletcher
```
![image](https://user-images.githubusercontent.com/53378715/218614319-b2f41fc9-7776-45a8-b641-5d2e2e3b4b9a.jpeg)


# References 
[Redhat How to use Grep Guide](https://www.redhat.com/sysadmin/how-to-use-grep)

[Official Gnu Grep Docs](https://www.gnu.org/software/grep/manual/grep.html)
