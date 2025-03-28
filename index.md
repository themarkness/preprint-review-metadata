---
layout: post
title: Preprint Review Metadata Modelling
bluesky_post_uri: https://bsky.app/profile/mark2d2.bsky.social/post/3llh4uahxbk2v
---

{% include sidebar.html %}

##  **Inputs**

### PID of preprint reviewed (essential 🟢)

#### Description/Meaning

The persistent identifier of the preprint eg. ([doi.org](http://doi.org)) formatted as \`https://doi.org/10.1101/2024.02.28.24303482\`

#### **🤖**Examples

*code example of fields the metadata can be mapped to and how to retrieve an example*

##### Crossref

###### ***Deposit***

```
<inter_work_relation relationship-type="isReviewOf" identifier-type="doi">10.1186/s12895-016-0051-4</inter_work_relation>
```

See [Peer reviews markup guide](https://www.crossref.org/documentation/schema-library/markup-guide-record-types/peer-reviews/#00077)

###### ***Retrieval***

```
{'is-review-of': [
{'asserted-by': 'subject',
'id': '10.7554/eLife.91327.4',
'id-type': 'doi'
}
]}
```

##### DataCite ***Deposit***

| relatedIdentifiers: \[{relationType: "Reviews",relatedIdentifier: "10.12688/verixiv.77.3",relatedIdentifierType: "DOI"}\], |
| :---- |

#####  ***Retrieval***

```
https://api.datacite.org/dois/10.21956/verixiv.511.r193

JSON:

relatedIdentifiers: [
{
relationType: "Reviews",
relatedIdentifier: "10.12688/verixiv.77.3",
relatedIdentifierType: "DOI"
}
],

XML:

<relatedIdentifiers>
    <relatedIdentifier relatedIdentifierType="DOI" relationType="Reviews">10.12688/verixiv.77.3</relatedIdentifier>
  </relatedIdentifiers>
```

##### DocMaps

A field "doi" on the input of the first step (see [full example](https://data-hub-api.elifesciences.org/enhanced-preprints/docmaps/v2/by-publisher/elife/get-by-manuscript-id?manuscript_id=86824)).

```
{
  ...
  "steps": {    "_:b0": {      "inputs": [{
        "type": "preprint",
        "doi": "10.1101/2022.05.16.492226",
        ...
     }
    }
  }
}
```

#### 🙏Who is currently depositing/retrieving this metadata and can help others? 

| Organisation and contact email | Workflow example |
| :---- | :---- |
| Copernicus GmbH | [5\. Open Research platform](https://osf.io/preprints/metaarxiv/yu4sm_v1)  |
| eLife Sciences Publications, | [6\. Publish-Review-Curate platform](https://osf.io/preprints/metaarxiv/yu4sm_v1) |
| Qeios | [1\. Preprint server with an integrated review option](https://osf.io/preprints/metaarxiv/yu4sm_v1) |
| Microbiology Society | [5\. Open Research platform](https://osf.io/preprints/metaarxiv/yu4sm_v1) |
| Review Commons | [6\. Publish-Review-Curate platform](https://osf.io/preprints/metaarxiv/yu4sm_v1) |
| ScienceOpen | [1\. Preprint server with an integrated review option](https://osf.io/preprints/metaarxiv/yu4sm_v1) |
| RR/ID | [3\. Preprint review platform registering DOIs](https://osf.io/preprints/metaarxiv/yu4sm_v1) |
| Peer Community In | [3\. Preprint review platform registering DOIs](https://osf.io/preprints/metaarxiv/yu4sm_v1) |
| F1000, michael.evans@f1000.com | [5\. Open Research platform](https://osf.io/preprints/metaarxiv/yu4sm_v1) |

#### 💪Actions/updates from the community 