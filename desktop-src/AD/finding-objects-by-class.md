---
title: Rechercher des objets par classe
description: Requête de recherche classique pour une classe d’objet spécifique.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Recherche d’objets par classe AD
- Active Directory, utiliser, Rechercher, par classe
- objet AD, recherche par classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512637"
---
# <a name="finding-objects-by-class"></a><span data-ttu-id="fb57f-106">Rechercher des objets par classe</span><span class="sxs-lookup"><span data-stu-id="fb57f-106">Finding Objects by Class</span></span>

<span data-ttu-id="fb57f-107">Requête de recherche classique pour une classe d’objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="fb57f-107">A typical search queries for a specific object class.</span></span> <span data-ttu-id="fb57f-108">L’exemple de code suivant recherche des ordinateurs avec l’emplacement dans Building 7N.</span><span class="sxs-lookup"><span data-stu-id="fb57f-108">The following code example searches for computers with location in Building 7N.</span></span>


```C++
(&(objectCategory=computer)(location=Building 7N))
```



<span data-ttu-id="fb57f-109">Pensez à la raison pour laquelle **objectClass** n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="fb57f-109">Consider why **objectClass** is not used.</span></span> <span data-ttu-id="fb57f-110">N’utilisez pas **objectClass** sans une autre comparaison qui contient un attribut indexé.</span><span class="sxs-lookup"><span data-stu-id="fb57f-110">Do not use **objectClass** without another comparison that contains an indexed attribute.</span></span> <span data-ttu-id="fb57f-111">Les attributs d’index peuvent accroître l’efficacité d’une requête.</span><span class="sxs-lookup"><span data-stu-id="fb57f-111">Index attributes can increase the efficiency of a query.</span></span> <span data-ttu-id="fb57f-112">L’attribut **objectClass** est à valeurs multiples et n’est pas indexé.</span><span class="sxs-lookup"><span data-stu-id="fb57f-112">The **objectClass** attribute is multi-valued and not indexed.</span></span> <span data-ttu-id="fb57f-113">Pour spécifier le type ou la classe d’un objet, utilisez **objectCategory**.</span><span class="sxs-lookup"><span data-stu-id="fb57f-113">To specify the type or class of an object, use **objectCategory**.</span></span>

<span data-ttu-id="fb57f-114">Moins efficace :</span><span class="sxs-lookup"><span data-stu-id="fb57f-114">Less efficient:</span></span>


```C++
(objectClass=computer)
```



<span data-ttu-id="fb57f-115">Plus efficace :</span><span class="sxs-lookup"><span data-stu-id="fb57f-115">More Efficient:</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="fb57f-116">Sachez qu’il existe des situations où une combinaison de **objectClass** et **objectCategory** doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="fb57f-116">Be aware that there are some cases where a combination of **objectClass** and **objectCategory** must be used.</span></span> <span data-ttu-id="fb57f-117">La classe utilisateur et la classe contact doivent être spécifiées comme suit.</span><span class="sxs-lookup"><span data-stu-id="fb57f-117">The user class and contact class should be specified as follows.</span></span>


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



<span data-ttu-id="fb57f-118">N’oubliez pas que vous pouvez rechercher les utilisateurs et les contacts avec les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="fb57f-118">Be aware that you could search for both users and contacts with the following.</span></span>


```C++
(objectCategory=person)
```



 

 




