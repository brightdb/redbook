# Problems

Today most data management applications are built upon centralized Web and Cloud services. They fulfill several purposes:

* **Low entry barrier.** Anyone with access to the Internet can reach out to these services.
* **Collaboration.** People can work together on data.
* **Availability.** Cloud services are highly available thanks to fault-tolerant and scalable systems.
* **Data preservation.** User data stored in the Cloud are less likely to vanish due to hardware failures.
* **Large data storage.** Cloud services can store huge amounts of data and make them accessible on storage-constrained devices.

However, these services also come with a bunch of drawbacks:

* **Centralized data storage.** If they get hacked, they might leak loads of unrelated application data.
* **No offline collaboration.** People can only work together on the same data if they are online.
* **Privacy.** Copying data to a third party means losing ultimate control over it.
* **Proprietary data formats.** Data access is only possible through a specific application (vendor lock-in).

## Related Work

* Online storgage (Google Drive, One Drive, Dropbox, ...)
* Notetaking (Evernote, Google Keep, Bear, ...)
* Distributed storage (Lima, Syncthing, Resilio)

# Solution

brightDB tries to solve these issues while offering comparable advantages as Cloud and Web services. 

* **Low entry barrier.** brightDB is a piece of software which can be downloaded and installed from the Internet. It is fully open-source and distributed under GPL.
* **Privacy.** Data is stored on the user's devices only and the ones data is shared with. So users effectively know who can access their data. 
* **Availability.** Since data is stored locally, it is - in its own sense - highly available.
* **Data preservation.** Data is copied among peer devices which share the same data space. Hence peer devices are backing up each other in the case of hardware failures. 
* **Decentralized.** Peer devices are the only place which store user data. If one gets hacked, it could only leak its own data and data shared by others.
* **Open data formats.** brightDB data is represented as RDF. Any application can be built upon its meta data standards and other Web ontologies. 
* **Collaboration.** brightDB allows people to work together on the same data at the same time - online as well as offline. Data is synchronized as soon as devices go online. Leveraging a conflict-free replicated data type brightDB can merge concurrent changes technically without the user's intervention. However, on a semantic level data needs to merged by the user anyway.
* **Large data storage.** brightDB is constrained by the peer devices' storage capacity. However, brightDB can be run on storage servers also. On devices with low storage, only references to large data sets will be kept locally and resolved on demand.

