## Copyright (C) 2021 Victor Rico
##
## This program is free software: you can redistribute it and/or modify
## it under the terms of the GNU General Public License as published by
## the Free Software Foundation, either version 3 of the License, or
## (at your option) any later vers
##
## This program is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU General Public License for more details.
##
## You should have received a copy of the GNU General Public License
## along with this program.  If not, see <https://www.gnu.org/licenses/>.

## -*- texinfo -*-
## @deftypefn {} {@var{retval} =} eros (@var{input1}, @var{input2})
##
## @seealso{}
## @end deftypefn

## Author: Victor Rico <Victor Rico@DESKTOP-KABB007>
## Created: 2021-03-10

    function img = eros (arch_o)
    img_o=imread(arch_o);
    [x,y]=size(img_o);
    contador=0;
    calculo=0;
    cuenta=0;
    c=0;
    for (j=1: y)

    contador = contador + 1;
    %almacenando en memorias
    switch (contador)
      case{1}
        if(cuenta==1)
          for (i=1: x)
            M0(i) = img_o(i,j);
            calculo = calculo+1;
            %comparando memorias para guardar en registros
            switch (calculo)
              case{1}
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RA=1;
                  else  
                    RA=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                elseif(M0(i)&&M1(i)&&M2(i))
                      RA=1;
                    else  
                      RA=0;
                endif
              case{2}
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RB=1;
                  else  
                    RB=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                elseif(M0(i)&&M1(i)&&M2(i))
                      RB=1;
                    else
                      RB=0;
                endif
              case{3}
                c= 1;
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RC=1;
                  else  
                    RC=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                endif
                calculo = 0;      
            endswitch
          endfor
          c=0;
        else
          for (i=1: x)
            M0(i) = img_o(i,j);
            
          endfor
        endif
        
      case{2}
        if(cuenta==1)
          for (i=1: x)
            M1(i) = img_o(i,j);
            calculo = calculo+1;
            %comparando memorias para guardar en registros
            switch (calculo)
              case{1}
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RA=1;
                  else  
                    RA=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                elseif(M0(i)&&M1(i)&&M2(i))
                      RA=1;
                    else  
                      RA=0;
                endif  
              case{2}
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RB=1;
                  else  
                    RB=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                elseif(M0(i)&&M1(i)&&M2(i))
                      RB=1;
                    else  
                      RB=0;
                endif  
              case{3}
                c= 1;
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RC=1;
                  else  
                    RC=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                endif   
                calculo = 0;   
            endswitch
          endfor
          c=0;
        else
          for (i=1: x)
            M1(i) = img_o(i,j);
          endfor
        endif
        
      case{3}
        cuenta = 1;
        if(cuenta==1)
          for (i=1: x)
            M2(i) = img_o(i,j);
            calculo = calculo + 1;
            %comparando memorias para guardar en registros
            switch (calculo)
              case{1}
                  if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RA=1;
                  else  
                    RA=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                elseif(M0(i)&&M1(i)&&M2(i))
                      RA=1;
                    else  
                      RA=0;
                endif
              case{2}
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RB=1;
                  else  
                    RB=0;
                  endif  
                  %comparando Registros para colocar 0¥s o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                elseif(M0(i)&&M1(i)&&M2(i))
                      RB=1;
                    else  
                      RB=0;
                endif 
              case{3}
                c= 1;
                if(c==1)
                  if(M0(i)&&M1(i)&&M2(i))
                    RC=1;
                  else  
                    RC=0;
                  endif  
                  %comparando Registros para colocar 0's o 1¥s en img_d
                  if(RA&&RB&&RC)
                    img_d(i-1,j-1)=1;
                  else
                    img_d(i-1,j-1)=0;
                  endif
                endif 
                calculo = 0;     
            endswitch
          endfor
          c=0;
        endif  
        contador = 0;
    endswitch
    endfor    
    %imshow(img_d);
    logical(img_d);  
    img=img_d;     
    imshow(img);
    endfunction
