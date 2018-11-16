let downloadCSV = function(csv) {
	let encodedCSV = encodeURI(csv);
	window.open(encodedCSV);
};

let makeCSV = function(arr) {
	let csv = "data:text/csv;charset=utf-8,";
	arr.forEach((arr) => {
		//gross windows line endings.
		csv += arr.join(",") + "\r\n";
	});
	return csv;
}

let makeArray = function(name) {
	let it = document.getElementById(name);
	let children = it.children;
	let length = children.length - 1;
	let result = [
		["link", "level", "result", "voted", "date", "reward", "person"]
	];

	for (let i = 0; i < length; i++) {
		let entry = ["", "", "", "", "", "", ""];
	
		let child = children[i];
		let grands = child.children;
		
		entry[0] =  (grands[0].firstChild ? grands[0].firstChild.href : "");
		entry[1] = (grands[1].firstChild ? grands[1].firstChild.innerHTML : "");
		entry[2] = (grands[2].firstChild ? grands[2].firstChild.innerHTML : "");
		entry[3] = (grands[3].firstChild ? grands[3].firstChild.innerHTML : "");
		entry[4] = (grands[4] ? grands[4].innerHTML : "");
		entry[5] = (grands[5] ? grands[5].innerHTML : "");
		entry[6] = (grands[6] ? grands[6].innerHTML : "");

		result.push(entry);
	}

	return result;
}
