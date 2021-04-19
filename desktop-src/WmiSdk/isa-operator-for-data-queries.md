---
description: Utilisez l’opérateur ISA dans la clause WHERE d’une requête de données pour demander des objets incorporés dans une hiérarchie de classes.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Opérateur ISA pour les requêtes de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521074"
---
# <a name="isa-operator-for-data-queries"></a><span data-ttu-id="ea601-103">Opérateur ISA pour les requêtes de données</span><span class="sxs-lookup"><span data-stu-id="ea601-103">ISA Operator for Data Queries</span></span>

<span data-ttu-id="ea601-104">Utilisez l’opérateur ISA dans la clause WHERE d’une requête de données pour demander des objets incorporés dans une hiérarchie de classes.</span><span class="sxs-lookup"><span data-stu-id="ea601-104">Use the ISA operator in the WHERE clause of a data query to request embedded objects in a class hierarchy.</span></span>

<span data-ttu-id="ea601-105">L’exemple suivant illustre la syntaxe permettant de demander des objets incorporés dans une hiérarchie de classes.</span><span class="sxs-lookup"><span data-stu-id="ea601-105">The following example shows the syntax to request embedded objects in a class hierarchy.</span></span>


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



<span data-ttu-id="ea601-106">Le résultat comprend des instances de **classe** qui ont des objets incorporés dérivés de **ParentClass** dans la propriété **EmbeddedProp** .</span><span class="sxs-lookup"><span data-stu-id="ea601-106">The result includes instances of **Class** having embedded objects that are derived from **ParentClass** in the **EmbeddedProp** property.</span></span> <span data-ttu-id="ea601-107">Les instances de l’objet de **classe** ne sont pas toutes dérivées de **ParentClass**, mais le résultat retourne les objets incorporés dérivés de **ParentClass**.</span><span class="sxs-lookup"><span data-stu-id="ea601-107">Not every instance of the **Class** object is derived from **ParentClass**, but the result returns the embedded objects that are derived from **ParentClass**.</span></span>

<span data-ttu-id="ea601-108">Par exemple, dans la requête suivante, **classa** comprend la propriété **EmbeddedObj** faiblement typée.</span><span class="sxs-lookup"><span data-stu-id="ea601-108">For example, in the following query, **ClassA** includes the weakly typed **EmbeddedObj** property.</span></span> <span data-ttu-id="ea601-109">La classe **classa** comporte dix instances.</span><span class="sxs-lookup"><span data-stu-id="ea601-109">The **ClassA** class has ten instances.</span></span> <span data-ttu-id="ea601-110">Cinq de ces instances ont des objets incorporés avec un type dérivé de **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="ea601-110">Five of those instances have embedded objects with a type derived from **ClassZ**.</span></span> <span data-ttu-id="ea601-111">Les cinq autres ont des objets incorporés d’autres types.</span><span class="sxs-lookup"><span data-stu-id="ea601-111">The other five have embedded objects of other types.</span></span>

<span data-ttu-id="ea601-112">L’exemple suivant montre la requête qui retourne les cinq instances, qui incluent les objets dérivés de **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="ea601-112">The following example shows the query that returns the five instances, which include the objects that are derived from **ClassZ**.</span></span>


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



