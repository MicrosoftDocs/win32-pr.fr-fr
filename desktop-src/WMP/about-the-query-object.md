---
title: À propos de l’objet de requête
description: À propos de l’objet de requête
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Lecteur Windows Media, objet de requête
- Modèle d’objet du lecteur Windows Media, objet de requête
- modèle objet, objet Query
- Contrôle ActiveX du lecteur Windows Media, objet de requête
- Contrôle ActiveX, objet de requête
- Contrôle ActiveX Windows Media Player Mobile, Query (objet)
- Windows Media Player Mobile, objet de requête
- Objet de requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673394"
---
# <a name="about-the-query-object"></a>À propos de l’objet de requête

L’objet de **requête** représente une requête composée. Pour créer un objet de **requête** vide, appelez *mediaCollection*. **CreateQuery**. Après avoir créé un objet de **requête** , vous pouvez appeler **addCondition** pour ajouter une condition à la requête composée. Chaque appel suivant à **addCondition** ajoute une nouvelle condition à la requête existante à l’aide de et de la logique.

Supposons, par exemple, que vous souhaitiez créer une requête qui représente tous les supports numériques où **WM/genre** est égal à « Jazz » et **auteur** contient « Jim ». Vous pouvez créer une requête composée pour représenter ces conditions à l’aide du code JScript suivant :


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

 

 




