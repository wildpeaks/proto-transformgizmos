# TransformGizmos

VRML PROTO that provides a 3D object to **edit the position/rotation of another object** with.

	EXTERNPROTO TransformGizmos [
		exposedField  SFInt32     type
		exposedField  SFNode      target
		eventIn       SFTime      forceUpdate
	] "proto.Tooltip.wrl#Tooltip"


-------------------------------------------------------------------------------

## Property `type`

Specifies the kind of transformation (**translation** vs **rotation**)
and coordinate system (**global** vs **local**).

Definition:
 - Field Type: `exposedField`
 - Data Type: `SFInt32`
 - Default Value: `-1`

Valid values are:
 - `-1`: no tranformation
 - `0`: translate (global)
 - `1`: rotate (global)
 - `2`: translate (local)
 - `3`: rotate (local)


-------------------------------------------------------------------------------

## Property `target`

Transform-like **object that is edited** by the gizmos.

Definition:
 - Field Type: `exposedField`
 - Data Type: `SFNode`
 - Default Value: `NULL`


-------------------------------------------------------------------------------

## Event `forceUpdate`

Call this even when `target` changes position/rotation for another reason than the gizmos.

Definition:
 - Field Type: `eventIn`
 - Data Type: `SFTime`


-------------------------------------------------------------------------------
