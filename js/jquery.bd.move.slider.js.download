/**
 * @name jQuery move slider 
 * ©copyright - http://bdeveloper.ru/
 *
 * depend on jQuery
*/
(function(e){e(document).data("bd_innner_timer",true);e.fn.bdmoveSlider=function(t){function h(){p()}function p(e){if(t.clickBtn)t.clickBtn();var u=parseInt(r.css("left")),a=n.find(t.crop),f=t.crop?Math.round((a.length?a.outerWidth():n.outerWidth())/s):1,l=-(s*(i.length-f)),c=0,h=false;if(this.className){var p=this.className.split(" ");for(var v=0;v<p.length;v++){if(p[v]==t.prev.slice(1)){h=p[v];break}}}if(h){if(u>=c){d(l)}else{if(u>=-(s*t.step))d(0);else d("+="+o)}}else{if(u>l){if(u<=l+s*t.step)d(l);else d("-="+o)}else{d(0)}}}function d(n){function a(){r.animate({left:n},t.durationMove,t.easingMove,function(){e(this).stop(true);if(t.timer){clearInterval(c);c=setInterval(h,t.interval)}if(t.info||t.slidenator)o=Math.round(-parseInt(r.css("left"))/s);if(t.slidenator)e(u.find(t.slidenatorItem).get(o)).addClass(t.slidenatorActive.slice(1));if(t.info)e(i.get(o)).find(t.info).fadeIn(t.infoShowDuration,t.easingInfo,function(){e(this).stop(true)});if(t.endMove)t.endMove()})}if(t.info||t.slidenator)var o=Math.round(-parseInt(r.css("left"))/s);if(t.info){e(i.get(o)).find(t.info).fadeOut(t.infoHideDuration,t.easingInfo,function(){e(this).stop(true);if(t.slidenator)e(u.find(t.slidenatorItem).get(o)).removeClass(t.slidenatorActive.slice(1));a()})}else{if(t.slidenator)e(u.find(t.slidenatorItem).get(o)).removeClass(t.slidenatorActive.slice(1));a()}}function v(){var t=e(this).index(),n=-(t*s),i=Math.round(-parseInt(r.css("left"))/s);if(i!=t)d(n)}if(!t)t={};t=e.extend({container:false,fullScreen:false,minWidth:0,start:0,lastPos:false,prev:(t.container||this.selector)+"__prev",next:(t.container||this.selector)+"__next",changeByBtn:true,list:(t.container||this.selector)+"__list",listWidth:false,item:(t.container||this.selector)+"__item",itemWidth:false,step:1,margin:false,info:false,infoHideDuration:300,infoShowDuration:300,durationMove:300,slidenator:false,slidenatorItem:(t.container||this.selector)+"__slidenator__item",slidenatorItemIn:"",slidenatorActive:(t.container||this.selector)+"__slidenator__item_active",slidenatorAfter:false,insertSlidenatorTo:false,timer:false,interval:5e3,timerToggle:(t.container||this.selector)+"__timer-toggle",easingMove:"swing",easingInfo:"swing",crop:false,clickBtn:false,endMove:false},t);var n=this,r=n.find(t.list),i=n.find(t.item);if(t.fullScreen){var s=e(window).width()>t.minWidth?e(window).width():t.minWidth;i.width(s);e(window).on("resize",function(){if(e(document).data("bd_innner_timer")){e(document).data("bd_innner_timer",false);setTimeout(function(){e(document).data("bd_innner_timer",true);n.find(t.prev).off("click");n.find(t.next).off("click");e(t.slidenator).remove();n.bdmoveSlider(t)},100)}})}else{s=t.itemWidth||i.eq(1).outerWidth(t.margin)}var o=s*t.step;if(i.length==1)return false;r.width(t.listWidth||s*(i.length+3)).css({position:"relative",left:-(t.start*s)});if(t.itemWidth){i.width(s)}if(t.info){n.find(t.info).hide().eq(t.start).show()}if(t.slidenator){var u=e('<span class="'+t.slidenator.slice(1)+'"></span>');for(var a=0;a<i.length;a++){u.append('<span class="'+t.slidenatorItem.slice(1)+'">'+t.slidenatorItemIn+"</span>")}if(t.slidenatorAfter)u.after(t.slidenatorAfter);u.find(t.slidenatorItem).eq(t.start).addClass(t.slidenatorActive.slice(1));u.on("click",t.slidenatorItem,v);if(t.insertSlidenatorTo)e(t.insertSlidenatorTo).append(u);else n.append(u)}if(t.changeByBtn){var f=n.find(t.prev),l=n.find(t.next);f.on("click",p);l.on("click",p)}if(t.timer){var c=setInterval(h,t.interval);e(t.timerToggle).toggle(function(){clearInterval(c)},function(){c=setInterval(h,t.interval)})}return this}})(jQuery);

/*
 * jQuery Easing v1.3 - http://gsgd.co.uk/sandbox/jquery/easing/
*/
jQuery.easing.jswing=jQuery.easing.swing;jQuery.extend(jQuery.easing,{def:"easeOutQuad",swing:function(e,f,a,h,g){return jQuery.easing[jQuery.easing.def](e,f,a,h,g)},easeInQuad:function(e,f,a,h,g){return h*(f/=g)*f+a},easeOutQuad:function(e,f,a,h,g){return -h*(f/=g)*(f-2)+a},easeInOutQuad:function(e,f,a,h,g){if((f/=g/2)<1){return h/2*f*f+a}return -h/2*((--f)*(f-2)-1)+a},easeInCubic:function(e,f,a,h,g){return h*(f/=g)*f*f+a},easeOutCubic:function(e,f,a,h,g){return h*((f=f/g-1)*f*f+1)+a},easeInOutCubic:function(e,f,a,h,g){if((f/=g/2)<1){return h/2*f*f*f+a}return h/2*((f-=2)*f*f+2)+a},easeInQuart:function(e,f,a,h,g){return h*(f/=g)*f*f*f+a},easeOutQuart:function(e,f,a,h,g){return -h*((f=f/g-1)*f*f*f-1)+a},easeInOutQuart:function(e,f,a,h,g){if((f/=g/2)<1){return h/2*f*f*f*f+a}return -h/2*((f-=2)*f*f*f-2)+a},easeInQuint:function(e,f,a,h,g){return h*(f/=g)*f*f*f*f+a},easeOutQuint:function(e,f,a,h,g){return h*((f=f/g-1)*f*f*f*f+1)+a},easeInOutQuint:function(e,f,a,h,g){if((f/=g/2)<1){return h/2*f*f*f*f*f+a}return h/2*((f-=2)*f*f*f*f+2)+a},easeInSine:function(e,f,a,h,g){return -h*Math.cos(f/g*(Math.PI/2))+h+a},easeOutSine:function(e,f,a,h,g){return h*Math.sin(f/g*(Math.PI/2))+a},easeInOutSine:function(e,f,a,h,g){return -h/2*(Math.cos(Math.PI*f/g)-1)+a},easeInExpo:function(e,f,a,h,g){return(f==0)?a:h*Math.pow(2,10*(f/g-1))+a},easeOutExpo:function(e,f,a,h,g){return(f==g)?a+h:h*(-Math.pow(2,-10*f/g)+1)+a},easeInOutExpo:function(e,f,a,h,g){if(f==0){return a}if(f==g){return a+h}if((f/=g/2)<1){return h/2*Math.pow(2,10*(f-1))+a}return h/2*(-Math.pow(2,-10*--f)+2)+a},easeInCirc:function(e,f,a,h,g){return -h*(Math.sqrt(1-(f/=g)*f)-1)+a},easeOutCirc:function(e,f,a,h,g){return h*Math.sqrt(1-(f=f/g-1)*f)+a},easeInOutCirc:function(e,f,a,h,g){if((f/=g/2)<1){return -h/2*(Math.sqrt(1-f*f)-1)+a}return h/2*(Math.sqrt(1-(f-=2)*f)+1)+a},easeInElastic:function(f,h,e,l,k){var i=1.70158;var j=0;var g=l;if(h==0){return e}if((h/=k)==1){return e+l}if(!j){j=k*0.3}if(g<Math.abs(l)){g=l;var i=j/4}else{var i=j/(2*Math.PI)*Math.asin(l/g)}return -(g*Math.pow(2,10*(h-=1))*Math.sin((h*k-i)*(2*Math.PI)/j))+e},easeOutElastic:function(f,h,e,l,k){var i=1.70158;var j=0;var g=l;if(h==0){return e}if((h/=k)==1){return e+l}if(!j){j=k*0.3}if(g<Math.abs(l)){g=l;var i=j/4}else{var i=j/(2*Math.PI)*Math.asin(l/g)}return g*Math.pow(2,-10*h)*Math.sin((h*k-i)*(2*Math.PI)/j)+l+e},easeInOutElastic:function(f,h,e,l,k){var i=1.70158;var j=0;var g=l;if(h==0){return e}if((h/=k/2)==2){return e+l}if(!j){j=k*(0.3*1.5)}if(g<Math.abs(l)){g=l;var i=j/4}else{var i=j/(2*Math.PI)*Math.asin(l/g)}if(h<1){return -0.5*(g*Math.pow(2,10*(h-=1))*Math.sin((h*k-i)*(2*Math.PI)/j))+e}return g*Math.pow(2,-10*(h-=1))*Math.sin((h*k-i)*(2*Math.PI)/j)*0.5+l+e},easeInBack:function(e,f,a,i,h,g){if(g==undefined){g=1.70158}return i*(f/=h)*f*((g+1)*f-g)+a},easeOutBack:function(e,f,a,i,h,g){if(g==undefined){g=1.70158}return i*((f=f/h-1)*f*((g+1)*f+g)+1)+a},easeInOutBack:function(e,f,a,i,h,g){if(g==undefined){g=1.70158}if((f/=h/2)<1){return i/2*(f*f*(((g*=(1.525))+1)*f-g))+a}return i/2*((f-=2)*f*(((g*=(1.525))+1)*f+g)+2)+a},easeInBounce:function(e,f,a,h,g){return h-jQuery.easing.easeOutBounce(e,g-f,0,h,g)+a},easeOutBounce:function(e,f,a,h,g){if((f/=g)<(1/2.75)){return h*(7.5625*f*f)+a}else{if(f<(2/2.75)){return h*(7.5625*(f-=(1.5/2.75))*f+0.75)+a}else{if(f<(2.5/2.75)){return h*(7.5625*(f-=(2.25/2.75))*f+0.9375)+a}else{return h*(7.5625*(f-=(2.625/2.75))*f+0.984375)+a}}}},easeInOutBounce:function(e,f,a,h,g){if(f<g/2){return jQuery.easing.easeInBounce(e,f*2,0,h,g)*0.5+a}return jQuery.easing.easeOutBounce(e,f*2-g,0,h,g)*0.5+h*0.5+a}});


/* |===============| Инициализация |===============| */
$(function() {
	$('.slider').bdmoveSlider({
		//easingMove: 'easeOutBounce',
		durationMove: 1200,
		slidenator: '.slider__slidenator',
		fullScreen: true,
		minWidth: 1181
	});
	
	$('.p-box_products').bdmoveSlider({
		container: '.p-box',
		//easingMove: 'easeOutBounce',
		durationMove: 800,
		margin: true,
		crop: true
	});
	
	$('.p-box_comments').bdmoveSlider({
		container: '.p-box',
		//easingMove: 'easeInOutBack',
		durationMove: 600,
		margin: true,
		crop: true
	});
});
	
