
=========
Changelog
=========

.. http://keepachangelog.com/en/1.0.0/

[Unreleased - coming in the future]
-----------------------------------
- handling of very large files, eg for streaming (see https://github.com/tudelft3d/cityjson/issues/6)
- ADE or mechanisms to extend the CityJSON data model in a structured and document way
- binary encoding of JSON, with either `CBOR <http://cbor.io>`_ or `BSON <http://bsonspec.org>`_

----

[0.6] - 2018-04-11
------------------
Added
*****
- support for Geometry Templates (aka Implicit Geometries)
- support for City Object Groups
- any members at the root of CityJSON are now allowed (but might be ignored by parser)
- each City Object can have a "bbox" member

Changed
*******
- the schema is now split into different schemas that are linked together
- the schema validator (software cjvalschema) is now in Python and improved, thus everyone can run it easily
- cjcompress does a better job and bugs have been removed
- textures are not forced to be in the folder 'appearances' anymore, any link to an image will do (useful for WFS for instance).


[0.5] - 2017-11-14 
------------------

Added
*****
- handling of ``null`` values at any level in a nested arrays is now supported in the schema
- CityGML module 'Transportation' added
- CityGML module 'Bridge' added, thus the 4 classes: Bridge, BridgePart, BridgeInstallation, and BridgeConstructionElement 
- CityGML module 'Tunnel' added, thus the 4 classes: Tunnel, TunnelPart, and TunnelInstallation

Changed
*******
- the way semantics is stored for the surface is completely changed and breaks previous version
- material now can be per surface ``"values": []`` or ``"value": 2`` 

----

[0.3] - 2017-10-12
------------------

Added
*****
- utility cityjson-valschema now ensures that no two City Objects have the same ID/key
- the schema now has depths of Geometry Objects for "texture", "material", and "semantics" arrays.
- the schema and the validator are generally better
- clear use of null and empty {} where appropriate

Changed
*******
- change to "header" and versioning of the file
- >1 textures and materials per geometry

----

[0.2] - 2017-09-05
------------------

Added
*****
- Semantics Objects, so that Semantic Surfaces have specific attributes 
- software to validate the schema + other properties impossible represent with the schema, eg warning users of "soft" errors like attributes not in CityGML

Changed
*******
- metadata now ISO19115 compliant 💥
- materials now use X3D mechanism, same as CityGML
- textures now use COLLADA mechanism, same as CityGML
- improved greatly the schema (more is validated) 

----

[0.1] - 2017-08-01 
------------------
Added
*****
- first beta release of CityJSON


