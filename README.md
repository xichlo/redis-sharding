redis-sharding
===========

  A consistent sharding library for redis in node. Using 'crc32', 'hashring'.
	
    var SgameRedis = require('redis-sharding');

	var options = { servers: [ 'redis01.sdev.local:6379', 'redis02.sdev.local:6379' ], password : 'abc@123' };
	var redis = new RedisSharding(options);

	// Get
	redis.hgetall('news:5108a1c1f7d59de21d000000', function (err, reply) {
		console.log(reply);
	});
