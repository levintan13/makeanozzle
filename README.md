# makeanozzle
draws a nozzle according to Dobrovolsky's "Liquid propellant rocket engines", page 45

1. look at Soplo class: change g (isentropic expansion factor), T_k (temperature in chamber), and phi_ras (dissipation loss factor) if needed;
2. create class object using s = Soplo(p_k, p_a, F_cr), where p_k and p_a - pressure in chamber and nozzle exit, F_cr - critical section area;
3. call s.__dict__ to see current nozzle parameters. to use the graphs on p.46 _rad_ratio and _theta_a are needed;
4. call s.add_params_46(theta_m, lenrat). parameters are obtained from p.46;
5. call s.__dict__ to get all nozzle parameters;
6. in cell #6 choose number of points to divide the basic lines;
7. after points_finder function call you will see full construction geometry;
8. run all cells to the end;
9. enjoy

comment on Dobrovolsky's p.46: the graph is also attached to this repository.
comment on points_finder:
it "builds" the construction lines and then checks their overlap points. for each line the overlap point with the lowest y is chosen.
works better with larger n value


