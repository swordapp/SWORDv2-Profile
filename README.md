SWORD 2.0 Profile
=================

The Atom Publishing Protocol provides a simple, extensible mechanism for the creation of Web Resources. The first major version of SWORD [SWORD 1.3] built upon the Resouce creation aspects of AtomPub to enable package deposit onto a server.

This approach of fire-and-forget deposit, where the depositor has no further interaction with the server is of significant value in certain use cases, but there are others where this is insufficient. Consider, for example, that the depositor wishes to construct a digital artifact file by file over a period of time before deciding that it is time to archive it. In these cases, a higher level of interactivity between the participating systems is required, and this is the role that SWORD 2.0 is intended to fulfil.

The SWORD 2.0 profile continues to build upon AtomPub and HTTP ([RFC2616]) through the inclusion of the Create, Retrieve, Update and Delete (CRUD) operations of AtomPub, in order to enable the following kinds of interactions:

* Clients may create resources by sending compound resources, such as archive files (tar, zip).
* Both non-interactive and 3rd party mediated operation are required.
* Workflows which may or may not include manual stages before deposited resources become available as web resources, are acknowledged and supported
* Clients may update or delete the compound resources or associated metadata
* The role that SWORD aims to fulfil is that of a thin integration layer between any two scholarly systems aiming to exchange content, but not to provide tight integration between them. For standards to integrate detailed content management operations it is recommended to look at OASIS CMIS [CMIS], or the GData API [GData]. In contrast to these, SWORD is a deposit lifecycle standard, which supports the users and the participating systems in effectively exchanging content. Most of the enhancements in SWORD 2.0 over SWORD 1.3 are around closing the deposit loop to give the client software the opportunity to provider a richer environment to the user.

The scope of SWORD v2 will be limited to the deposit process between any two scholarly systems or between a user facing system and a service provider. This deposit process is only a portion of the full content lifecycle and does not attempt to provide support for collaborative or distributed authoring environments or policy management; it is focused entirely on the process of moving content from one location to another.

The deposit lifecycle encompasses the process of delivering content to a SWORD server which may have an ingest workflow in place. The content that has been deposited is then considered to be in the deposit process for the duration of that ingest workflow, during which time the client system may wish to interact with the submission. It may be that the client needs to make changes to the submission during the workflow process, either autonomously or when prompted for additional input by the server. Or it may be that the client wants to track the progress of the submission, at its leisure. Eventually the content will be formally accepted into the system and the client needs a way to know that this is happened and a route to follow to locate the deposited content.

The main profile is detailed in SWORDProfile.html

The practical details of the extensions used in the SWORD Profile are provided in the following Internet Drafts:

* Packaged Content Delivery over HTTP [SWORD001.html]
* AtomPub Extensions for Packaged Content [SWORD002.html]
* AtomPub Extensions for Scholarly Systems [SWORD003.html]
* Atom Multipart Extensions for Packaged Content [SWORD004.html]

