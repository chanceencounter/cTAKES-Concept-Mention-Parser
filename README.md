# cTAKES Concept Mention Parser

This is a child component of https://github.com/GoTeamEpsilon/cTAKES-Intelligent-Chart-Summarization-Solution, the user-friendly, native EMR NLP solution.

## Responsibilites

This container, when given an XMI result from cTAKES, puts together a nice JSON representation of the concept mentions with medical codes and text. When the processing is done, the JSON is sent to a container that communicates back to the EMR.



## Install

_(Note that this will be taken care of in the parent via `docker-compose`)_

```
$ sudo pip install xmltodict
$ sudo pip install watchdog
```

## Demonstration

![gif](https://github.com/MatthewVita/cTAKES-Concept-Mention-Parser/blob/master/demo.gif?raw=true)

As an example, some fake data (credit: https://www.med.unc.edu/medselect/resources/sample-notes/sample-initial-visit-note-1) has been checked into the samples folder to get and idea of the output quality:

> Mr. Smith is a 56-year-old gentleman formally followed at Carolina Premier who presents to obtain a new primary care physician secondary to insurance changes. He has a past medical history significant for a myocardial infarction in 1994. His cholesterol has been fine. Catheterization showed a possible "kink" in one of his vessels and it was thought that he had a possible "eddy" of current which led to a clot. He has been on Coumadin since then as well as a calcium channel blocker with the thought that there may have been a superimposed spasm. He has had several unremarkable stress tests since then. He works out on a Nordic-Track three times a week without any chest pain or shortness of breath. He has a history of possible peptic ulcer disease in 1981. He was treated with H2 blockers and his symptoms resolved. He has never had any bleeding to his knowledge. He had a hernia repair bilaterally in 1989 and surgery for a right knee cyst in 1999, all of which went well. He also has about a year long history of right buttock pain. This happens only when he is sitting for some time and does not change position. It does not happen when he is walking or exercising. He wonders if it might be pyriformis syndrome. If he changes positions frequently or stretches his legs, this seems to help. He has no acute complaints today and is here to get plugged into the system. He does wonder if there is anything else that can be done about his buttock pain.

`$ vi samples/data.json` to see

## TODOs

- Set up solution in a Docker container
- Make the lookup O(1) by indexing on XML ID
- Switch to Python3/pep
- Unit tests

## LICENSE

MIT
