# addYear
function addYear(flag){
		var s = document.forms[0].year;
		var val, o;
		if(flag){
			val = s.options[s.length -1].value * 1 + 1;
			o = new Option(val, val, false, true);
			try{
				s.add(o, null);
			}catch(e){
				s.add(o);
			}
		}else{
			val = s.options[0].value * 1 - 1;
			o = new Option(val, val, false, true);
			try{
				s.add(o, s.options[0]);
			}catch(e){
				s.add(o, 0);
			}
		}
	}
