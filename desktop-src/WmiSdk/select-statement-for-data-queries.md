---
description: Décrivez l’instruction SELECT pour une requête de données.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Instruction SELECT pour les requêtes de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527810"
---
# <a name="select-statement-for-data-queries"></a><span data-ttu-id="7b3e6-103">Instruction SELECT pour les requêtes de données</span><span class="sxs-lookup"><span data-stu-id="7b3e6-103">SELECT Statement for Data Queries</span></span>

<span data-ttu-id="7b3e6-104">Vous pouvez utiliser diverses instructions SELECT pour demander des informations.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-104">You can use a variety of SELECT statements to query for information.</span></span> <span data-ttu-id="7b3e6-105">Les instructions peuvent être des instructions de base ou elles peuvent être plus restrictives pour limiter le jeu de résultats retourné par la requête.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="7b3e6-106">L’exemple suivant est une instruction SELECT de base utilisée pour interroger des données.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-106">The following example is a basic SELECT statement that is used to query for data.</span></span>


```sql
SELECT * FROM Class
```



<span data-ttu-id="7b3e6-107">Cette instruction retourne les instances de la classe spécifiée et l’une de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-107">This statement returns instances of the specified class and any of its subclasses.</span></span> <span data-ttu-id="7b3e6-108">Toutes les propriétés système et définies par l’utilisateur pour les classes sont incluses.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-108">All of the system and user-defined properties for the classes are included.</span></span> <span data-ttu-id="7b3e6-109">Si une propriété système n’est pas pertinente pour une requête particulière, elle contient la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-109">If a system property is not relevant for a particular query, it contains **NULL**.</span></span>

<span data-ttu-id="7b3e6-110">Vous pouvez utiliser plusieurs techniques pour réduire la bande passante nécessaire à la récupération du jeu de résultats, si l’exécution de la requête entraîne une surcharge excessive et que l’utilisateur est uniquement intéressé par un sous-ensemble des propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-110">You can use several techniques to reduce the bandwidth required to retrieve the result set, if the execution of the query results in too much overhead and the user is only interested in a subset of the properties.</span></span> <span data-ttu-id="7b3e6-111">Tout d’abord, les requêtes peuvent remplacer l’astérisque par les propriétés souhaitées.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-111">First, queries can replace the asterisk with the desired properties.</span></span>

<span data-ttu-id="7b3e6-112">L’exemple suivant montre comment interroger des propriétés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-112">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM class
```



<span data-ttu-id="7b3e6-113">Le jeu de résultats comprend toutes les propriétés système et les propriétés non système spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-113">The result set includes all system properties and the specified nonsystem properties.</span></span>

<span data-ttu-id="7b3e6-114">Une autre technique pour limiter l’étendue du jeu de résultats d’une requête consiste à utiliser la propriété système de [**\_ \_ classe**](wmi-system-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="7b3e6-114">Another technique for narrowing the scope of a query's result set is to use the [**\_\_CLASS**](wmi-system-properties.md) system property.</span></span> <span data-ttu-id="7b3e6-115">Par défaut, les requêtes retournent toutes les instances de la classe spécifiée et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-115">Queries by default return all instances of the specified class and its subclasses.</span></span> <span data-ttu-id="7b3e6-116">Vous pouvez utiliser la propriété système de **\_ \_ classe** pour demander uniquement des instances de la classe spécifiée, à l’exclusion de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-116">You can use the **\_\_CLASS** system property to request only instances of the specified class, excluding its subclasses.</span></span>

<span data-ttu-id="7b3e6-117">L’exemple suivant montre comment utiliser la propriété système de [**\_ \_ classe**](wmi-system-properties.md) dans une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-117">The following example shows how to use the [**\_\_CLASS**](wmi-system-properties.md) system property in a WHERE clause.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



<span data-ttu-id="7b3e6-118">Vous pouvez également utiliser la propriété système de [**\_ \_ classe**](wmi-system-properties.md) pour limiter le jeu de résultats aux instances de sous-classes particulières.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-118">You can also use the [**\_\_CLASS**](wmi-system-properties.md) system property to restrict the result set to instances of particular subclasses.</span></span>

<span data-ttu-id="7b3e6-119">L’exemple suivant montre comment limiter le jeu de résultats aux instances de sous-classes particulières.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-119">The following example shows how to restrict the result set to instances of particular subclasses.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> <span data-ttu-id="7b3e6-120">Si vous construisez une requête avec un chemin d’accès non valide pour un objet incorporé, votre requête ne retourne pas d’erreur ou de résultats.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-120">If you construct a query with an invalid path for an embedded object, your query does not return an error or any results.</span></span>

 

<span data-ttu-id="7b3e6-121">L’exemple suivant retourne une instance de **MainClass**, en supposant qu’il existe une instance de **MainClass** contenant l’objet incorporé **EmbedObj** avec une propriété **P \_ UInt32** égale à « 70011 ».</span><span class="sxs-lookup"><span data-stu-id="7b3e6-121">The following example returns an instance of **MainClass**, assuming that an instance of **MainClass** exists containing the embedded object **EmbedObj** with a property **P\_Uint32** that is equal to "70011".</span></span>


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



<span data-ttu-id="7b3e6-122">L’exemple suivant ne retourne aucun résultat et ne retourne pas d’erreur, en supposant que l’objet incorporé **EmbedObj** dans l’instance de **MainClass** n’a pas de propriété **non valide**.</span><span class="sxs-lookup"><span data-stu-id="7b3e6-122">The following example returns no results and does not return an error, assuming that the embedded object **EmbedObj** in the instance of **MainClass** does not have a property **INVALID**.</span></span>


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



