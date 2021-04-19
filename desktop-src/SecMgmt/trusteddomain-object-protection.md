---
description: Lorsqu’un objet TrustedDomain est créé, une protection standard lui est affectée.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Protection des objets TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515628"
---
# <a name="trusteddomain-object-protection"></a><span data-ttu-id="6c7aa-103">Protection des objets TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="6c7aa-103">TrustedDomain Object Protection</span></span>

<span data-ttu-id="6c7aa-104">Lorsqu’un objet [**trustedDomain**](trusteddomain-object.md) est créé, une protection standard lui est assignée comme suit :</span><span class="sxs-lookup"><span data-stu-id="6c7aa-104">When a [**TrustedDomain**](trusteddomain-object.md) object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="6c7aa-105">L’accès en exécution générique est accordé au groupe WORLD local \_ .</span><span class="sxs-lookup"><span data-stu-id="6c7aa-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="6c7aa-106">Le groupe local d’administration local reçoit un \_ \_ accès en suppression, en lecture générique, en \_ écriture générique et en \_ Exécution générique.</span><span class="sxs-lookup"><span data-stu-id="6c7aa-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="6c7aa-107">Le \_ groupe local administrateur local est affecté en tant que propriétaire et groupe principal de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6c7aa-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 



