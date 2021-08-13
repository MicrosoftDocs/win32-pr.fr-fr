---
title: À propos de l’objet de requête
description: À propos de l’objet de requête
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Lecteur Windows Media, objet de requête
- Lecteur Windows Media modèle objet, Query (objet)
- modèle objet, objet Query
- Lecteur Windows Media ActiveX contrôle, objet de requête
- contrôle ActiveX, objet Query
- Lecteur Windows Media contrôle Mobile ActiveX, objet Query
- Lecteur Windows Media Mobile, objet de requête
- Objet de requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d649263f981d02e106466c6e0fcada99c316054d4bf6e0acc0faca641c75dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470399"
---
# <a name="about-the-query-object"></a>À propos de l’objet de requête

L’objet de **requête** représente une requête composée. Pour créer un objet de **requête** vide, appelez *mediaCollection*. **CreateQuery**. Après avoir créé un objet de **requête** , vous pouvez appeler **addCondition** pour ajouter une condition à la requête composée. Chaque appel suivant à **addCondition** ajoute une nouvelle condition à la requête existante à l’aide de et de la logique.

Supposons, par exemple, que vous souhaitiez créer une requête qui représente tous les supports numériques où **WM/genre** est égal à « Jazz » et **auteur** contient « Jim ». vous pouvez créer une requête composée pour représenter ces conditions en utilisant le code JScript suivant :


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Pour ajouter une condition à une requête composée à l’aide de ou de la logique, vous devez appeler **query. beginNextGroup**. Cette méthode signale que le groupe de conditions précédent est terminé et que l’appel suivant à **addCondition** représente le début d’un nouveau groupe de conditions.

Par exemple, pour créer une requête qui représente tous les supports numériques où **WM/genre** est égal à « Jazz » et **auteur** contient « Jim » ou **auteur** contient « Dave », vous pouvez utiliser l’exemple de code suivant :


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



Pour exécuter votre requête composée, appelez **MediaCollection. getPlaylistByQuery**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objet Query**](query-object.md)
</dt> </dl>

 

 




