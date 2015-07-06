Campaigns = new Mongo.Collection("campaigns");


// This code only runs on the client
Template.home.helpers({
	showCampaigns: function () {
  		return Campaigns.find({});
	}
});


Template.body.events({
	"submit .placement": function (event) {
	
	var pos = event.target.position.value;
	
	
	Campaigns.insert({
		position: pos,
		createdAt: new Date()
	});
	
	var ele = document.getElementsByName("position");
   	for(var i=0;i<ele.length;i++){
      	ele[i].checked = false;
	}
	
	//console.log(event);
	//document.write('writing:' + pos);
	
	return false;
	
	}
});
