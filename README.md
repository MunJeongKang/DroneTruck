## "An Exact Algorithm for Heterogeneous Drone-Truck Routing Problem" <br>(published in *Transportation Science* https://doi.org/10.1287/trsc.2021.1055)

#### by Munjeong Kang<sup>1</sup> and Chungmok Lee <sup>2</sup>

#### <sup>1</sup> LG Display Co., Republic of Korea, mj0225868@gmail.com

#### <sup>2</sup> Department of Industrial and Management Engineering, Hankuk University of Foreign Studies, Youngin-si, Republic of Korea, chungmok@hufs.ac.kr

------------------------------------------------------------------------

We used randomly generated instances from two real-life use cases.

#### Instances
+ #### All results are given in `.vrp` format.
+ #### The sizes of problem are 20, 30, 40, and 50 nodes, and each size contains ten instances. Therefore there are total 80 instances (=2 areas × 4 sizes × 10 instances)
+ #### /CPS
  + An area near CVS Pharmacy store in Cary, N.C., U.S. (Latitude, Lon- gitude)=(35.7910400, -78.8465283)
  + Instance name: `|N|_|A|_|K|_C_F.lp`

+ #### /WM
  + An area near WakeMed hospital campus in Raleigh, N.C., U.S.(Latitude, Longitude)=(35.7825655, -78.5881280)
  + Instance name: `|N|_|A|_|K|_C_F.lp`




<figure class="half">
    <img src="[CVS_all](https://user-images.githubusercontent.com/36038222/202480117-58bdcf04-b7b7-4871-af8e-c3d9d29c16f8.png)">
    <img src="[WM_all](https://user-images.githubusercontent.com/36038222/202480144-3c1a3bc9-405d-4322-9fba-14b82546d9ac.png)">
figure>


#### 2. Results

+ #### All results are given in `.json` format.
+ #### Instance name: `instancename_method_benderstype_cuttype.json`
  + method: benders, mip
  + benderstype: bnc, tb
  + cuttype: classical, magnanti, yang, fischetti, closest

```vrpc
{
	"probname": instance name,
	"results": [
		{
			"subtime": time spent in solving the Benders subproblems,
			"totaltime": total computational time,
			"nnodes": number of nodes,
			"x0time": time spent in obtaining the feasible point x0,
			"iteration": number of iterations,
			"objval": objective value,
			"feascutnum": number of feasibility cuts,
			"optcutnum": number of optimality cuts
		}
	],
	"algorithm": [
		{
			"cuttype": cut type,
			"benderstype": benders type
		}
	]
}
```
