---
description: Vous avez plusieurs options pour le formulaire qu’une requête prend lors de l’interrogation d’une classe d’événements qui contient des objets incorporés. Les résultats retournés par la requête varient en fonction de la forme de la requête que vous utilisez.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Interrogation d’objets incorporés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755053"
---
# <a name="querying-embedded-objects"></a>Interrogation d’objets incorporés

Vous avez plusieurs options pour le formulaire qu’une requête prend lors de l’interrogation d’une classe d’événements qui contient des objets incorporés. Les résultats retournés par la requête varient en fonction de la forme de la requête que vous utilisez.

## <a name="class-definitions"></a>Définitions de classe

L’exemple suivant montre les définitions de classe utilisées pour les requêtes WQL dans cette rubrique.

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a>Exemples

La requête suivante retourne à la fois les classes incorporées, **E1** et **E2**, qui ont chacune une propriété **Prop1** et **Prop2** remplie avec des données.

`SELECT * FROM MyEvent`

La requête ci-dessous retourne l’objet incorporé **E1** , mais sans la valeur **Prop1** ou **Prop2** remplie avec des données.

`SELECT E1 FROM MyEvent`

La requête suivante retourne la classe incorporée **E1** avec un seul **Prop1** rempli de données.

`SELECT E1.Prop1 FROM MyEvent`

La requête suivante retourne à la fois les classes incorporées, **E1** et **E2**, qui ont chacune une propriété **Prop1** et **Prop2** remplie avec des données.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Cela équivaut à la première requête utilisant l’astérisque ( \* ) au lieu de spécifier chaque objet et propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interrogation avec WQL](querying-with-wql.md)
</dt> </dl>

 

 



