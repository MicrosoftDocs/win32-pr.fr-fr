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
# <a name="about-the-query-object"></a><span data-ttu-id="27dd0-111">À propos de l’objet de requête</span><span class="sxs-lookup"><span data-stu-id="27dd0-111">About the Query Object</span></span>

<span data-ttu-id="27dd0-112">L’objet de **requête** représente une requête composée.</span><span class="sxs-lookup"><span data-stu-id="27dd0-112">The **Query** object represents a compound query.</span></span> <span data-ttu-id="27dd0-113">Pour créer un objet de **requête** vide, appelez *mediaCollection*. **CreateQuery**.</span><span class="sxs-lookup"><span data-stu-id="27dd0-113">You create a new, empty **Query** object by calling *mediaCollection*.**createQuery**.</span></span> <span data-ttu-id="27dd0-114">Après avoir créé un objet de **requête** , vous pouvez appeler **addCondition** pour ajouter une condition à la requête composée.</span><span class="sxs-lookup"><span data-stu-id="27dd0-114">After you have created a **Query** object, you can call **addCondition** to add a condition to the compound query.</span></span> <span data-ttu-id="27dd0-115">Chaque appel suivant à **addCondition** ajoute une nouvelle condition à la requête existante à l’aide de et de la logique.</span><span class="sxs-lookup"><span data-stu-id="27dd0-115">Each subsequent call to **addCondition** appends a new condition to the existing query using AND logic.</span></span>

<span data-ttu-id="27dd0-116">Supposons, par exemple, que vous souhaitiez créer une requête qui représente tous les supports numériques où **WM/genre** est égal à « Jazz » et **auteur** contient « Jim ».</span><span class="sxs-lookup"><span data-stu-id="27dd0-116">For example, suppose you want to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim".</span></span> <span data-ttu-id="27dd0-117">Vous pouvez créer une requête composée pour représenter ces conditions à l’aide du code JScript suivant :</span><span class="sxs-lookup"><span data-stu-id="27dd0-117">You could create a compound query to represent these conditions by using the following JScript code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



<span data-ttu-id="27dd0-118">Pour ajouter une condition à une requête composée à l’aide de ou de la logique, vous devez appeler **query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="27dd0-118">To add a condition to a compound query using OR logic, you must call **Query.beginNextGroup**.</span></span> <span data-ttu-id="27dd0-119">Cette méthode signale que le groupe de conditions précédent est terminé et que l’appel suivant à **addCondition** représente le début d’un nouveau groupe de conditions.</span><span class="sxs-lookup"><span data-stu-id="27dd0-119">This method signals that the previous condition group is completed and that the next call to **addCondition** represents the start of a new condition group.</span></span>

<span data-ttu-id="27dd0-120">Par exemple, pour créer une requête qui représente tous les supports numériques où **WM/genre** est égal à « Jazz » et **auteur** contient « Jim » ou **auteur** contient « Dave », vous pouvez utiliser l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="27dd0-120">For example, to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim" or **Author** contains "Dave", you could use the following example code:</span></span>


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



<span data-ttu-id="27dd0-121">Pour exécuter votre requête composée, appelez **MediaCollection. getPlaylistByQuery**.</span><span class="sxs-lookup"><span data-stu-id="27dd0-121">To execute your compound query, call **MediaCollection.getPlaylistByQuery**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27dd0-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27dd0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27dd0-123">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="27dd0-123">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="27dd0-124">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="27dd0-124">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="27dd0-125">**Objet Query**</span><span class="sxs-lookup"><span data-stu-id="27dd0-125">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 




