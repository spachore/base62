# base62

A 2-digit base62 nubmer system with alphanumeric character set in this order [0-9][a-z][A-Z]

A simple number increment function to get next base62 number.

An additional function to support running legacy systems, which treats numbers [00-99] as base10 numbers and then starts base62 numbers [a0-ZZ].



00 01 02 03 04 05 06 07 08 09 

10 11 12 13 14 15 16 17 18 19 

20 21 22 23 24 25 26 27 28 29 

30 31 32 33 34 35 36 37 38 39 

40 41 42 43 44 45 46 47 48 49 

50 51 52 53 54 55 56 57 58 59 

60 61 62 63 64 65 66 67 68 69 

70 71 72 73 74 75 76 77 78 79 

80 81 82 83 84 85 86 87 88 89 

90 91 92 93 94 95 96 97 98 99 

a0 a1 a2 a3 a4 a5 a6 a7 a8 a9 aa ab ac ad ae af ag ah ai aj ak al am an ao ap aq ar as at au av aw ax ay az aA aB aC aD aE aF aG aH aI aJ aK aL aM aN aO aP aQ aR aS aT aU aV aW aX aY aZ 

b0 b1 b2 b3 b4 b5 b6 b7 b8 b9 ba bb bc bd be bf bg bh bi bj bk bl bm bn bo bp bq br bs bt bu bv bw bx by bz bA bB bC bD bE bF bG bH bI bJ bK bL bM bN bO bP bQ bR bS bT bU bV bW bX bY bZ 

c0 c1 c2 c3 c4 c5 c6 c7 c8 c9 ca cb cc cd ce cf cg ch ci cj ck cl cm cn co cp cq cr cs ct cu cv cw cx cy cz cA cB cC cD cE cF cG cH cI cJ cK cL cM cN cO cP cQ cR cS cT cU cV cW cX cY cZ 

d0 d1 d2 d3 d4 d5 d6 d7 d8 d9 da db dc dd de df dg dh di dj dk dl dm dn do dp dq dr ds dt du dv dw dx dy dz dA dB dC dD dE dF dG dH dI dJ dK dL dM dN dO dP dQ dR dS dT dU dV dW dX dY dZ 

e0 e1 e2 e3 e4 e5 e6 e7 e8 e9 ea eb ec ed ee ef eg eh ei ej ek el em en eo ep eq er es et eu ev ew ex ey ez eA eB eC eD eE eF eG eH eI eJ eK eL eM eN eO eP eQ eR eS eT eU eV eW eX eY eZ 

f0 f1 f2 f3 f4 f5 f6 f7 f8 f9 fa fb fc fd fe ff fg fh fi fj fk fl fm fn fo fp fq fr fs ft fu fv fw fx fy fz fA fB fC fD fE fF fG fH fI fJ fK fL fM fN fO fP fQ fR fS fT fU fV fW fX fY fZ 

g0 g1 g2 g3 g4 g5 g6 g7 g8 g9 ga gb gc gd ge gf gg gh gi gj gk gl gm gn go gp gq gr gs gt gu gv gw gx gy gz gA gB gC gD gE gF gG gH gI gJ gK gL gM gN gO gP gQ gR gS gT gU gV gW gX gY gZ 

h0 h1 h2 h3 h4 h5 h6 h7 h8 h9 ha hb hc hd he hf hg hh hi hj hk hl hm hn ho hp hq hr hs ht hu hv hw hx hy hz hA hB hC hD hE hF hG hH hI hJ hK hL hM hN hO hP hQ hR hS hT hU hV hW hX hY hZ 

i0 i1 i2 i3 i4 i5 i6 i7 i8 i9 ia ib ic id ie if ig ih ii ij ik il im in io ip iq ir is it iu iv iw ix iy iz iA iB iC iD iE iF iG iH iI iJ iK iL iM iN iO iP iQ iR iS iT iU iV iW iX iY iZ 

j0 j1 j2 j3 j4 j5 j6 j7 j8 j9 ja jb jc jd je jf jg jh ji jj jk jl jm jn jo jp jq jr js jt ju jv jw jx jy jz jA jB jC jD jE jF jG jH jI jJ jK jL jM jN jO jP jQ jR jS jT jU jV jW jX jY jZ 

k0 k1 k2 k3 k4 k5 k6 k7 k8 k9 ka kb kc kd ke kf kg kh ki kj kk kl km kn ko kp kq kr ks kt ku kv kw kx ky kz kA kB kC kD kE kF kG kH kI kJ kK kL kM kN kO kP kQ kR kS kT kU kV kW kX kY kZ 

l0 l1 l2 l3 l4 l5 l6 l7 l8 l9 la lb lc ld le lf lg lh li lj lk ll lm ln lo lp lq lr ls lt lu lv lw lx ly lz lA lB lC lD lE lF lG lH lI lJ lK lL lM lN lO lP lQ lR lS lT lU lV lW lX lY lZ 

m0 m1 m2 m3 m4 m5 m6 m7 m8 m9 ma mb mc md me mf mg mh mi mj mk ml mm mn mo mp mq mr ms mt mu mv mw mx my mz mA mB mC mD mE mF mG mH mI mJ mK mL mM mN mO mP mQ mR mS mT mU mV mW mX mY mZ 

n0 n1 n2 n3 n4 n5 n6 n7 n8 n9 na nb nc nd ne nf ng nh ni nj nk nl nm nn no np nq nr ns nt nu nv nw nx ny nz nA nB nC nD nE nF nG nH nI nJ nK nL nM nN nO nP nQ nR nS nT nU nV nW nX nY nZ 

o0 o1 o2 o3 o4 o5 o6 o7 o8 o9 oa ob oc od oe of og oh oi oj ok ol om on oo op oq or os ot ou ov ow ox oy oz oA oB oC oD oE oF oG oH oI oJ oK oL oM oN oO oP oQ oR oS oT oU oV oW oX oY oZ 

p0 p1 p2 p3 p4 p5 p6 p7 p8 p9 pa pb pc pd pe pf pg ph pi pj pk pl pm pn po pp pq pr ps pt pu pv pw px py pz pA pB pC pD pE pF pG pH pI pJ pK pL pM pN pO pP pQ pR pS pT pU pV pW pX pY pZ 

q0 q1 q2 q3 q4 q5 q6 q7 q8 q9 qa qb qc qd qe qf qg qh qi qj qk ql qm qn qo qp qq qr qs qt qu qv qw qx qy qz qA qB qC qD qE qF qG qH qI qJ qK qL qM qN qO qP qQ qR qS qT qU qV qW qX qY qZ 

r0 r1 r2 r3 r4 r5 r6 r7 r8 r9 ra rb rc rd re rf rg rh ri rj rk rl rm rn ro rp rq rr rs rt ru rv rw rx ry rz rA rB rC rD rE rF rG rH rI rJ rK rL rM rN rO rP rQ rR rS rT rU rV rW rX rY rZ 

s0 s1 s2 s3 s4 s5 s6 s7 s8 s9 sa sb sc sd se sf sg sh si sj sk sl sm sn so sp sq sr ss st su sv sw sx sy sz sA sB sC sD sE sF sG sH sI sJ sK sL sM sN sO sP sQ sR sS sT sU sV sW sX sY sZ 

t0 t1 t2 t3 t4 t5 t6 t7 t8 t9 ta tb tc td te tf tg th ti tj tk tl tm tn to tp tq tr ts tt tu tv tw tx ty tz tA tB tC tD tE tF tG tH tI tJ tK tL tM tN tO tP tQ tR tS tT tU tV tW tX tY tZ 

u0 u1 u2 u3 u4 u5 u6 u7 u8 u9 ua ub uc ud ue uf ug uh ui uj uk ul um un uo up uq ur us ut uu uv uw ux uy uz uA uB uC uD uE uF uG uH uI uJ uK uL uM uN uO uP uQ uR uS uT uU uV uW uX uY uZ 

v0 v1 v2 v3 v4 v5 v6 v7 v8 v9 va vb vc vd ve vf vg vh vi vj vk vl vm vn vo vp vq vr vs vt vu vv vw vx vy vz vA vB vC vD vE vF vG vH vI vJ vK vL vM vN vO vP vQ vR vS vT vU vV vW vX vY vZ 

w0 w1 w2 w3 w4 w5 w6 w7 w8 w9 wa wb wc wd we wf wg wh wi wj wk wl wm wn wo wp wq wr ws wt wu wv ww wx wy wz wA wB wC wD wE wF wG wH wI wJ wK wL wM wN wO wP wQ wR wS wT wU wV wW wX wY wZ 

x0 x1 x2 x3 x4 x5 x6 x7 x8 x9 xa xb xc xd xe xf xg xh xi xj xk xl xm xn xo xp xq xr xs xt xu xv xw xx xy xz xA xB xC xD xE xF xG xH xI xJ xK xL xM xN xO xP xQ xR xS xT xU xV xW xX xY xZ 

y0 y1 y2 y3 y4 y5 y6 y7 y8 y9 ya yb yc yd ye yf yg yh yi yj yk yl ym yn yo yp yq yr ys yt yu yv yw yx yy yz yA yB yC yD yE yF yG yH yI yJ yK yL yM yN yO yP yQ yR yS yT yU yV yW yX yY yZ 

z0 z1 z2 z3 z4 z5 z6 z7 z8 z9 za zb zc zd ze zf zg zh zi zj zk zl zm zn zo zp zq zr zs zt zu zv zw zx zy zz zA zB zC zD zE zF zG zH zI zJ zK zL zM zN zO zP zQ zR zS zT zU zV zW zX zY zZ 

A0 A1 A2 A3 A4 A5 A6 A7 A8 A9 Aa Ab Ac Ad Ae Af Ag Ah Ai Aj Ak Al Am An Ao Ap Aq Ar As At Au Av Aw Ax Ay Az AA AB AC AD AE AF AG AH AI AJ AK AL AM AN AO AP AQ AR AS AT AU AV AW AX AY AZ 

B0 B1 B2 B3 B4 B5 B6 B7 B8 B9 Ba Bb Bc Bd Be Bf Bg Bh Bi Bj Bk Bl Bm Bn Bo Bp Bq Br Bs Bt Bu Bv Bw Bx By Bz BA BB BC BD BE BF BG BH BI BJ BK BL BM BN BO BP BQ BR BS BT BU BV BW BX BY BZ 

C0 C1 C2 C3 C4 C5 C6 C7 C8 C9 Ca Cb Cc Cd Ce Cf Cg Ch Ci Cj Ck Cl Cm Cn Co Cp Cq Cr Cs Ct Cu Cv Cw Cx Cy Cz CA CB CC CD CE CF CG CH CI CJ CK CL CM CN CO CP CQ CR CS CT CU CV CW CX CY CZ 

D0 D1 D2 D3 D4 D5 D6 D7 D8 D9 Da Db Dc Dd De Df Dg Dh Di Dj Dk Dl Dm Dn Do Dp Dq Dr Ds Dt Du Dv Dw Dx Dy Dz DA DB DC DD DE DF DG DH DI DJ DK DL DM DN DO DP DQ DR DS DT DU DV DW DX DY DZ 

E0 E1 E2 E3 E4 E5 E6 E7 E8 E9 Ea Eb Ec Ed Ee Ef Eg Eh Ei Ej Ek El Em En Eo Ep Eq Er Es Et Eu Ev Ew Ex Ey Ez EA EB EC ED EE EF EG EH EI EJ EK EL EM EN EO EP EQ ER ES ET EU EV EW EX EY EZ 

F0 F1 F2 F3 F4 F5 F6 F7 F8 F9 Fa Fb Fc Fd Fe Ff Fg Fh Fi Fj Fk Fl Fm Fn Fo Fp Fq Fr Fs Ft Fu Fv Fw Fx Fy Fz FA FB FC FD FE FF FG FH FI FJ FK FL FM FN FO FP FQ FR FS FT FU FV FW FX FY FZ 

G0 G1 G2 G3 G4 G5 G6 G7 G8 G9 Ga Gb Gc Gd Ge Gf Gg Gh Gi Gj Gk Gl Gm Gn Go Gp Gq Gr Gs Gt Gu Gv Gw Gx Gy Gz GA GB GC GD GE GF GG GH GI GJ GK GL GM GN GO GP GQ GR GS GT GU GV GW GX GY GZ 

H0 H1 H2 H3 H4 H5 H6 H7 H8 H9 Ha Hb Hc Hd He Hf Hg Hh Hi Hj Hk Hl Hm Hn Ho Hp Hq Hr Hs Ht Hu Hv Hw Hx Hy Hz HA HB HC HD HE HF HG HH HI HJ HK HL HM HN HO HP HQ HR HS HT HU HV HW HX HY HZ 

I0 I1 I2 I3 I4 I5 I6 I7 I8 I9 Ia Ib Ic Id Ie If Ig Ih Ii Ij Ik Il Im In Io Ip Iq Ir Is It Iu Iv Iw Ix Iy Iz IA IB IC ID IE IF IG IH II IJ IK IL IM IN IO IP IQ IR IS IT IU IV IW IX IY IZ 

J0 J1 J2 J3 J4 J5 J6 J7 J8 J9 Ja Jb Jc Jd Je Jf Jg Jh Ji Jj Jk Jl Jm Jn Jo Jp Jq Jr Js Jt Ju Jv Jw Jx Jy Jz JA JB JC JD JE JF JG JH JI JJ JK JL JM JN JO JP JQ JR JS JT JU JV JW JX JY JZ 

K0 K1 K2 K3 K4 K5 K6 K7 K8 K9 Ka Kb Kc Kd Ke Kf Kg Kh Ki Kj Kk Kl Km Kn Ko Kp Kq Kr Ks Kt Ku Kv Kw Kx Ky Kz KA KB KC KD KE KF KG KH KI KJ KK KL KM KN KO KP KQ KR KS KT KU KV KW KX KY KZ 

L0 L1 L2 L3 L4 L5 L6 L7 L8 L9 La Lb Lc Ld Le Lf Lg Lh Li Lj Lk Ll Lm Ln Lo Lp Lq Lr Ls Lt Lu Lv Lw Lx Ly Lz LA LB LC LD LE LF LG LH LI LJ LK LL LM LN LO LP LQ LR LS LT LU LV LW LX LY LZ 

M0 M1 M2 M3 M4 M5 M6 M7 M8 M9 Ma Mb Mc Md Me Mf Mg Mh Mi Mj Mk Ml Mm Mn Mo Mp Mq Mr Ms Mt Mu Mv Mw Mx My Mz MA MB MC MD ME MF MG MH MI MJ MK ML MM MN MO MP MQ MR MS MT MU MV MW MX MY MZ 

N0 N1 N2 N3 N4 N5 N6 N7 N8 N9 Na Nb Nc Nd Ne Nf Ng Nh Ni Nj Nk Nl Nm Nn No Np Nq Nr Ns Nt Nu Nv Nw Nx Ny Nz NA NB NC ND NE NF NG NH NI NJ NK NL NM NN NO NP NQ NR NS NT NU NV NW NX NY NZ 

O0 O1 O2 O3 O4 O5 O6 O7 O8 O9 Oa Ob Oc Od Oe Of Og Oh Oi Oj Ok Ol Om On Oo Op Oq Or Os Ot Ou Ov Ow Ox Oy Oz OA OB OC OD OE OF OG OH OI OJ OK OL OM ON OO OP OQ OR OS OT OU OV OW OX OY OZ 

P0 P1 P2 P3 P4 P5 P6 P7 P8 P9 Pa Pb Pc Pd Pe Pf Pg Ph Pi Pj Pk Pl Pm Pn Po Pp Pq Pr Ps Pt Pu Pv Pw Px Py Pz PA PB PC PD PE PF PG PH PI PJ PK PL PM PN PO PP PQ PR PS PT PU PV PW PX PY PZ 

Q0 Q1 Q2 Q3 Q4 Q5 Q6 Q7 Q8 Q9 Qa Qb Qc Qd Qe Qf Qg Qh Qi Qj Qk Ql Qm Qn Qo Qp Qq Qr Qs Qt Qu Qv Qw Qx Qy Qz QA QB QC QD QE QF QG QH QI QJ QK QL QM QN QO QP QQ QR QS QT QU QV QW QX QY QZ 

R0 R1 R2 R3 R4 R5 R6 R7 R8 R9 Ra Rb Rc Rd Re Rf Rg Rh Ri Rj Rk Rl Rm Rn Ro Rp Rq Rr Rs Rt Ru Rv Rw Rx Ry Rz RA RB RC RD RE RF RG RH RI RJ RK RL RM RN RO RP RQ RR RS RT RU RV RW RX RY RZ 

S0 S1 S2 S3 S4 S5 S6 S7 S8 S9 Sa Sb Sc Sd Se Sf Sg Sh Si Sj Sk Sl Sm Sn So Sp Sq Sr Ss St Su Sv Sw Sx Sy Sz SA SB SC SD SE SF SG SH SI SJ SK SL SM SN SO SP SQ SR SS ST SU SV SW SX SY SZ 

T0 T1 T2 T3 T4 T5 T6 T7 T8 T9 Ta Tb Tc Td Te Tf Tg Th Ti Tj Tk Tl Tm Tn To Tp Tq Tr Ts Tt Tu Tv Tw Tx Ty Tz TA TB TC TD TE TF TG TH TI TJ TK TL TM TN TO TP TQ TR TS TT TU TV TW TX TY TZ 

U0 U1 U2 U3 U4 U5 U6 U7 U8 U9 Ua Ub Uc Ud Ue Uf Ug Uh Ui Uj Uk Ul Um Un Uo Up Uq Ur Us Ut Uu Uv Uw Ux Uy Uz UA UB UC UD UE UF UG UH UI UJ UK UL UM UN UO UP UQ UR US UT UU UV UW UX UY UZ 

V0 V1 V2 V3 V4 V5 V6 V7 V8 V9 Va Vb Vc Vd Ve Vf Vg Vh Vi Vj Vk Vl Vm Vn Vo Vp Vq Vr Vs Vt Vu Vv Vw Vx Vy Vz VA VB VC VD VE VF VG VH VI VJ VK VL VM VN VO VP VQ VR VS VT VU VV VW VX VY VZ 

W0 W1 W2 W3 W4 W5 W6 W7 W8 W9 Wa Wb Wc Wd We Wf Wg Wh Wi Wj Wk Wl Wm Wn Wo Wp Wq Wr Ws Wt Wu Wv Ww Wx Wy Wz WA WB WC WD WE WF WG WH WI WJ WK WL WM WN WO WP WQ WR WS WT WU WV WW WX WY WZ 

X0 X1 X2 X3 X4 X5 X6 X7 X8 X9 Xa Xb Xc Xd Xe Xf Xg Xh Xi Xj Xk Xl Xm Xn Xo Xp Xq Xr Xs Xt Xu Xv Xw Xx Xy Xz XA XB XC XD XE XF XG XH XI XJ XK XL XM XN XO XP XQ XR XS XT XU XV XW XX XY XZ 

Y0 Y1 Y2 Y3 Y4 Y5 Y6 Y7 Y8 Y9 Ya Yb Yc Yd Ye Yf Yg Yh Yi Yj Yk Yl Ym Yn Yo Yp Yq Yr Ys Yt Yu Yv Yw Yx Yy Yz YA YB YC YD YE YF YG YH YI YJ YK YL YM YN YO YP YQ YR YS YT YU YV YW YX YY YZ 

Z0 Z1 Z2 Z3 Z4 Z5 Z6 Z7 Z8 Z9 Za Zb Zc Zd Ze Zf Zg Zh Zi Zj Zk Zl Zm Zn Zo Zp Zq Zr Zs Zt Zu Zv Zw Zx Zy Zz ZA ZB ZC ZD ZE ZF ZG ZH ZI ZJ ZK ZL ZM ZN ZO ZP ZQ ZR ZS ZT ZU ZV ZW ZX ZY ZZ 


