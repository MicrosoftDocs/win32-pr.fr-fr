---
title: Tri (ADSI)
description: Un client peut demander à un serveur de trier le jeu de résultats.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "106509021"
---
# <a name="sorting-adsi"></a><span data-ttu-id="46fa6-103">Tri (ADSI)</span><span class="sxs-lookup"><span data-stu-id="46fa6-103">Sorting (ADSI)</span></span>

<span data-ttu-id="46fa6-104">Un client peut demander à un serveur de trier le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="46fa6-104">A client can request a server to sort the result set.</span></span> <span data-ttu-id="46fa6-105">Vous pouvez spécifier les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="46fa6-105">You can specify:</span></span>

-   <span data-ttu-id="46fa6-106">Ordre de tri : l’ordre de tri croissant ou décroissant peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="46fa6-106">Sort order: Either ascending or descending sort order can be specified.</span></span>
-   <span data-ttu-id="46fa6-107">Attributs de tri : plusieurs attributs peuvent être spécifiés dans une chaîne de tri.</span><span class="sxs-lookup"><span data-stu-id="46fa6-107">Sort attributes: Multiple attributes can be specified in a sort string.</span></span> <span data-ttu-id="46fa6-108">Par exemple, triez par nom, puis par prénom.</span><span class="sxs-lookup"><span data-stu-id="46fa6-108">For example, sort by Last Name, then First Name.</span></span>

<span data-ttu-id="46fa6-109">Lorsque vous spécifiez l’ordre de tri, vous devez essayer d’utiliser l’un des attributs indexés.</span><span class="sxs-lookup"><span data-stu-id="46fa6-109">When you specify sort order, you should try to use one of the indexed attributes.</span></span> <span data-ttu-id="46fa6-110">Dans le cas contraire, le serveur doit calculer un jeu de résultats complet avant de l’envoyer au client.</span><span class="sxs-lookup"><span data-stu-id="46fa6-110">Otherwise, the server must calculate a complete result set before sending it to the client.</span></span> <span data-ttu-id="46fa6-111">Cela est vrai même si vous avez demandé une recherche paginée et spécifié une taille de page.</span><span class="sxs-lookup"><span data-stu-id="46fa6-111">This is true even if you have requested a paged search and specified a page size.</span></span>

> [!Note]  
> <span data-ttu-id="46fa6-112">Tous les serveurs d’annuaire ne prennent pas en charge plusieurs tris d’attribut ou ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="46fa6-112">Not all directory servers support multiple attribute sorts or sort order.</span></span>

 

 

 




