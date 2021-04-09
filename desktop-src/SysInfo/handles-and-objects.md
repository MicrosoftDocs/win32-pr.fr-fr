---
description: Un objet est une structure de données qui représente une ressource système, telle qu’un fichier, un thread ou une image graphique.
ms.assetid: 26aaad09-c1e1-46e8-9cd3-7d795a10d900
title: Handles et objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b5a35d55571a01f2f186f4e756401582474949f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868166"
---
# <a name="handles-and-objects"></a><span data-ttu-id="01c42-103">Handles et objets</span><span class="sxs-lookup"><span data-stu-id="01c42-103">Handles and Objects</span></span>

<span data-ttu-id="01c42-104">Un *objet* est une structure de données qui représente une ressource système, telle qu’un fichier, un thread ou une image graphique.</span><span class="sxs-lookup"><span data-stu-id="01c42-104">An *object* is a data structure that represents a system resource, such as a file, thread, or graphic image.</span></span> <span data-ttu-id="01c42-105">Une application ne peut pas accéder directement aux données d’objet ou aux ressources système qu’un objet représente.</span><span class="sxs-lookup"><span data-stu-id="01c42-105">An application cannot directly access object data or the system resource that an object represents.</span></span> <span data-ttu-id="01c42-106">Au lieu de cela, une application doit obtenir un *descripteur* d’objet, qu’elle peut utiliser pour examiner ou modifier la ressource système.</span><span class="sxs-lookup"><span data-stu-id="01c42-106">Instead, an application must obtain an object *handle*, which it can use to examine or modify the system resource.</span></span> <span data-ttu-id="01c42-107">Chaque descripteur a une entrée dans une table gérée en interne.</span><span class="sxs-lookup"><span data-stu-id="01c42-107">Each handle has an entry in an internally maintained table.</span></span> <span data-ttu-id="01c42-108">Ces entrées contiennent les adresses des ressources et les moyens d’identifier le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="01c42-108">These entries contain the addresses of the resources and the means to identify the resource type.</span></span>

-   [<span data-ttu-id="01c42-109">À propos des handles et des objets</span><span class="sxs-lookup"><span data-stu-id="01c42-109">About Handles and Objects</span></span>](about-handles-and-objects.md)
-   [<span data-ttu-id="01c42-110">Catégories d’objets</span><span class="sxs-lookup"><span data-stu-id="01c42-110">Object Categories</span></span>](object-categories.md)
-   [<span data-ttu-id="01c42-111">Handle et référence d’objet</span><span class="sxs-lookup"><span data-stu-id="01c42-111">Handle and Object Reference</span></span>](handle-and-object-reference.md)

 

 



