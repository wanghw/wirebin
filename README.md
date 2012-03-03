WHAT IS wirebin
---------------

wirebin provides encoding and decoding functions for a speed/CPU optimized binary string representation of basic python types.

HOW TO USE wirebin
------------------

1.  wbin.serialize(object[, callback[, args[, frequency]]]) -> string.

    Given a python object encode it into a python string.

    An optional callback(offset[,args]) will be periodically called with number of bytes so far encoded as the first parameter. The remaining optional parameters to the callback are supplied as an optional args parameter to the serialize function.

    Finally an optional frequency parameter determines approximately how many bytes are encoded between each call to the callback function. (default 8K)

2.  wbin.deserialize(object[, callback[, args[, frequency]]]) -> string.

    Given a python string decode it into a python object.

    An optional callback(offset[,args]) will be periodically called with number of bytes so far encoded as the first parameter. The remaining optional parameters to the callback are supplied as an optional args parameter to the serialize function.

    Finally an optional frequency parameter determines approximately how many bytes are encoded between each call to the callback function. (default 8K)

3.  wbin.utf8_enable() -> None Enable UTF8 encoding support

4.  wbin.utf8_disable() -> None Disable UTF8 encoding support

5.  wbin.utf8_enabled() -> status Returns True if UTF8 encoding is enable

6.  wbin.wls_on() -> None Enable encodable object whitelist (default)

7.  wbin.wls_off() -> None Disable encodable object whitelist (attempt to encode all objects)

8.  wbin.wls_status() -> status Returns encodable object whitelist status

9.  wbin.min_int() -> int Returns smallest integer that can be encoded

10. wbin.max_int() -> int Returns largest integer that can be encoded
