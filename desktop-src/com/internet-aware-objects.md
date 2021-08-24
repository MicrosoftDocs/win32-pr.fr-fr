---
title: Objets Internet-Aware
description: Objets Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280141d4bc9cb1a6a6c685c4badde0b24609996683e73c74f69637440b39ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756149"
---
# <a name="internet-aware-objects"></a>Objets Internet-Aware

Certaines catégories sont identifiées pour couvrir les interfaces persistances ; celles-ci ont été identifiées à la suite de la définition de la façon dont les contrôles fonctionnent sur Internet. Un conteneur qui ne prend pas en charge la plage complète d’interfaces persistance doit s’assurer qu’il n’héberge pas un contrôle qui requiert une combinaison d’interfaces qu’il ne prend pas en charge.

Les tableaux suivants décrivent la signification de différentes catégories à la fois comme catégories implémentées et requises.



| Catégories requises                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, catidd \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Chacune de ces catégories s’exclut mutuellement et n’est utilisée que lorsqu’un objet ne prend en charge qu’un seul mécanisme de persistance (par conséquent, l’exclusion mutuelle). Les conteneurs qui ne prennent pas en charge le mécanisme de persistance décrit par l’une de ces catégories doivent empêcher eux-mêmes de créer des objets de classes donc marqués.<br/> |
| RequiresDataPathHost CATID \_<br/>                                                                                                                                                             | L’objet nécessite la possibilité d’enregistrer des données dans un ou plusieurs chemins d’accès et requiert l’implication d’un conteneur, ce qui nécessite une prise en charge de conteneur pour [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).<br/>                                                                                                                                  |



 



| Catégories implémentées                                                                                                                                                                            | Description                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, catidd \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | L’objet prend en charge le mécanisme IPersist correspondant \* pour la catégorie.<br/> |



 

Le tableau suivant fournit le CATID exact affecté à chaque catégorie :



| Category                                | CATID                                           |
|-----------------------------------------|-------------------------------------------------|
| RequiresDataPathHost CATID \_<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToMoniker CATID \_ <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStorage CATID \_ <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStreamInit CATID \_ <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStream CATID \_ <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToMemory CATID \_ <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToFile CATID \_ <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToPropertyBag CATID \_<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

