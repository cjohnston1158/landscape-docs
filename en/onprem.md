Title: Landscape On-Premises
## Landscape On-Premises

Landscape On-Premises, is the standalone version of Landscape that you can install on your own network.

Each major Landscape version is supported for a period of one year after release. Here are the current supported releases:

| **major version**                  | **Release date** | **Supported until** | **Version of Ubuntu**  |
| ----------------------             | ---------------- | ------------------- | ---------------------  |
| [18.03](./ReleaseNotes18.03.md)  | 2018-Jun         | **2019-Jun**        | 16.04 LTS or 18.04 LTS |
| [17.03](./ReleaseNotes17.03.md)  | 2017-Mar         | **2019-Mar**        | 16.04 LTS              |


### Installation

Landscape On-Premises consists of two parts:

 * **application server**
 * **database server**

Depending on your deployment method, these may live on the same machine or different machines. Here is how you can get started:

#### Quickstart

**[Quickstart](./landscape-install-quickstart.md)**, for when you don't have Juju but quickly want to check out OPL. Not recommended for production environments when having more than 500 clients.

#### Juju deployed

**[Juju deployed](./landscape-install-juju.md)** for a truly scalable deployment. Select the bundle that best serves your environment:


#### Manual installation

**[Manual installation](./landscape-install-manual.md)**: for when you don't have a suitable Juju environment but need a scalable deployment.

### Installation requirements

#### Network access

The machine(s) running as the application service will need the following network access:

 * http access to `usn.ubuntu.com` in order to download the USN database and detect security updates. Without this, the available updates won't be distinguished between security related and regular updates
 * http access to the public Ubuntu archives and `changelogs.ubuntu.com`, in order to update the hash-id-database files and detect new distribution releases. Without this, the release upgrade feature won't work
 * https access to `landscape.canonical.com` in order to query for available LDS releases. If this access is not given, the only drawback is that LDS won't display a note about the available releases in the account page.
