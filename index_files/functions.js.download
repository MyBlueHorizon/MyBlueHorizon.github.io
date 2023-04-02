function getElement(id) {
    return document.getElementById(id);
}

function getInnerHTML(id) {
    return getElement(id).innerHTML;
}

function setInnerHTML(id, v) {
    getElement(id).innerHTML = v;
}

function getValue(id) {
    return getElement(id).value;
}

function setValue(id, v) {
    getElement(id).value = v;
}

String.prototype.trim = function() {
    return this.replace(/^(\s|\u00A0)+/,'').replace(/(\s|\u00A0)+$/,'');
}

function setCookie(name, val, expires, path) {
	if (!path) path = "/";
	var exp = new Date();
	exp.setTime(exp.getTime() + expires*1000);
	document.cookie = name + "=" + escape(val) + ";expires=" + exp.toGMTString() + ";path=" + path;
}

function getCookie(name) {
	var arr, reg = new RegExp("(^| )" + name + "=([^;]*)(;|$)");
	if (arr = document.cookie.match(reg)) {
		if (arr[2][0] == '"') arr[2] = arr[2].substr(1, arr[2].length - 2);
		return unescape(arr[2]);
	}
	return null;
}

function delCookie(name, path) {
	if (!path) path = "/";
	var exp = new Date();
	exp.setTime(exp.getTime() - 1);
	var cval = getCookie(name);
	if (cval != null) document.cookie = name + "=" + escape(cval) + ";expires=" + exp.toGMTString() + ";path=" + path;
}