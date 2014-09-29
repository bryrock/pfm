pfm
===

Pure Freakin' Magic - A Drupal developer utility for working with entity metadata wrappers.

This is a debugging tool for use when working in Drupal with entity_metadata_wrapper.

Wrapped entities in Drupal contain protected functions, which prevents casual viewing inside them with Devel's dsm/dpm functions.

pfm is a simple function that will reveal the values contained in a wrapped entity, then return those with dpm.

EASY SYNTAX
-----------

It's use is simple, as the only required argument is the wrapped entity:

pfm($wrapper);

An optional second argument modifies the defaul output.

pfm($wrapper, 'my wrapped entity');

EXAMPLE USAGE
-------------
$node_wrapper = entity_metadata_wrapper('node',$nid);

pfm($node_wrapper);

OR

pfm($node_wrapper,'This node contains');