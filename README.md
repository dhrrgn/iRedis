#iRedis

iRedis is a simple and fast Redis PHP library.  It has been modeled after Redisent, and infact contains some Redisent code (copyrights remain).

iRedis was created because Redisent has stopped active development and was in need of a facelift.

##Usage

Basic Usage

    include 'iredis.php';
    
    $redis = new iRedis();

By default iRedis will use a hostname of 'localhost' and a port of 6379.  If you would like to use a different server or port you can send a config array to the constructor.

    $redis = new iRedis(array('hostname' => 'redis.foo.com', 'port' => 6425));

To run commands simply call that method on the iRedis object:

    $redis->set('myval', 'Hello World!');

    echo $redis->get('myval'); // Outputs 'Hello World!'

##Requirements

iRedis requires Redis version 1.2 and greater.  This is because it uses the Unified Request protocol.