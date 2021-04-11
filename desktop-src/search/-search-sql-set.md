---
description: L’instruction SET spécifie les options PROPERTYNAME et RANKMETHOD pour la requête.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Instruction SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112414"
---
# <a name="set-statement"></a><span data-ttu-id="217a5-103">Instruction SET</span><span class="sxs-lookup"><span data-stu-id="217a5-103">SET Statement</span></span>

<span data-ttu-id="217a5-104">L’instruction SET spécifie les options PROPERTYNAME et RANKMETHOD pour la requête.</span><span class="sxs-lookup"><span data-stu-id="217a5-104">The SET statement specifies PROPERTYNAME and RANKMETHOD options for the query.</span></span>

## <a name="propertyname"></a><span data-ttu-id="217a5-105">PROPERTYNAME</span><span class="sxs-lookup"><span data-stu-id="217a5-105">PROPERTYNAME</span></span>

<span data-ttu-id="217a5-106">Vous pouvez associer une propriété à un alias convivial pour la requête à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="217a5-106">You can associate a property with a friendly alias for the query by using the following syntax:</span></span>


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a><span data-ttu-id="217a5-107">RANKMETHOD</span><span class="sxs-lookup"><span data-stu-id="217a5-107">RANKMETHOD</span></span>

<span data-ttu-id="217a5-108">Vous pouvez spécifier la méthode rank pour les requêtes avec le terme ISABOUT à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="217a5-108">You can specify the rank method for queries with the ISABOUT term by using the following syntax:</span></span>


```
SET RANKMETHOD <rankmethod>      
```



<span data-ttu-id="217a5-109">Les méthodes RANKMETHOD qui peuvent être spécifiées à l’aide de l’instruction SET sont le coefficient JACCARD, le coefficient des dés et le produit interne.</span><span class="sxs-lookup"><span data-stu-id="217a5-109">The RANKMETHOD methods that can be specified by using the SET statement are JACCARD COEFFICIENT, DICE COEFFICIENT, and INNER PRODUCT.</span></span>

 

 



