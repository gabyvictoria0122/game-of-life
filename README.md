# Gaby's Game of Life

It is a cellular automaton devised by the British mathematician John Horton Conway in 1970.   
Based on some mathematical rules, cells can live, die or multiply.

## Vue.js Version:

[ click here ](https://game-of-life-gv.vercel.app/)

![image](https://user-images.githubusercontent.com/104435995/210425695-631c3d0a-dbb4-472b-ac16-7da3e0b97b98.png)


### Setup:

```  cd vue/life-in-vue  ```  
```  npm run serve  ```


## Python 3.8.10 Version:

https://user-images.githubusercontent.com/104435995/209340952-48a61ffb-019f-4107-951e-f7e1c544b59e.mp4

### Setup:

```  cd python  ```  
```  pip install -r requirements.txt  ```  
```  python main.py  ```  



## Game rules:

* To be born:  
Each cell with three neighbors is born.

* To die:  
 Each cell with one or no neighbors dies, as if by solitude.   
 Each cell with four or more neighbors dies, as if by overpopulation.

* To stay alive:   
Each cell with two or three neighbors survives.

