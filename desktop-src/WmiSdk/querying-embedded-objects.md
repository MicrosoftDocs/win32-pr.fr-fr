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
# <a name="querying-embedded-objects"></a><span data-ttu-id="ed47c-104">Interrogation d’objets incorporés</span><span class="sxs-lookup"><span data-stu-id="ed47c-104">Querying Embedded Objects</span></span>

<span data-ttu-id="ed47c-105">Vous avez plusieurs options pour le formulaire qu’une requête prend lors de l’interrogation d’une classe d’événements qui contient des objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="ed47c-105">You have several options as to the form a query takes when querying an event class that contains embedded objects.</span></span> <span data-ttu-id="ed47c-106">Les résultats retournés par la requête varient en fonction de la forme de la requête que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ed47c-106">The results returned by the query vary, depending on the form of the query you use.</span></span>

## <a name="class-definitions"></a><span data-ttu-id="ed47c-107">Définitions de classe</span><span class="sxs-lookup"><span data-stu-id="ed47c-107">Class Definitions</span></span>

<span data-ttu-id="ed47c-108">L’exemple suivant montre les définitions de classe utilisées pour les requêtes WQL dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ed47c-108">The following example shows the class definitions that are used for the WQL queries in this topic.</span></span>

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

## <a name="examples"></a><span data-ttu-id="ed47c-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="ed47c-109">Examples</span></span>

<span data-ttu-id="ed47c-110">La requête suivante retourne à la fois les classes incorporées, **E1** et **E2**, qui ont chacune une propriété **Prop1** et **Prop2** remplie avec des données.</span><span class="sxs-lookup"><span data-stu-id="ed47c-110">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`SELECT * FROM MyEvent`

<span data-ttu-id="ed47c-111">La requête ci-dessous retourne l’objet incorporé **E1** , mais sans la valeur **Prop1** ou **Prop2** remplie avec des données.</span><span class="sxs-lookup"><span data-stu-id="ed47c-111">The following query returns the **E1** embedded object, but with neither **Prop1** nor **Prop2** populated with data.</span></span>

`SELECT E1 FROM MyEvent`

<span data-ttu-id="ed47c-112">La requête suivante retourne la classe incorporée **E1** avec un seul **Prop1** rempli de données.</span><span class="sxs-lookup"><span data-stu-id="ed47c-112">The following query returns the embedded class **E1** with only **Prop1** populated with data.</span></span>

`SELECT E1.Prop1 FROM MyEvent`

<span data-ttu-id="ed47c-113">La requête suivante retourne à la fois les classes incorporées, **E1** et **E2**, qui ont chacune une propriété **Prop1** et **Prop2** remplie avec des données.</span><span class="sxs-lookup"><span data-stu-id="ed47c-113">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

<span data-ttu-id="ed47c-114">Cela équivaut à la première requête utilisant l’astérisque ( \* ) au lieu de spécifier chaque objet et propriété.</span><span class="sxs-lookup"><span data-stu-id="ed47c-114">This is equivalent to the first query using the asterisk (\*) instead of specifying each object and property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed47c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed47c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed47c-116">Interrogation avec WQL</span><span class="sxs-lookup"><span data-stu-id="ed47c-116">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

 



