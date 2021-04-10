---
title: Stockage persistant sur le serveur
description: Vous pouvez optimiser votre application afin que le stub serveur ne libère pas la mémoire sur le serveur à la fin d’un appel de procédure distante.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940145"
---
# <a name="persistent-storage-on-the-server"></a><span data-ttu-id="a2254-103">Stockage persistant sur le serveur</span><span class="sxs-lookup"><span data-stu-id="a2254-103">Persistent Storage on the Server</span></span>

<span data-ttu-id="a2254-104">Vous pouvez optimiser votre application afin que le stub serveur ne libère pas la mémoire sur le serveur à la fin d’un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a2254-104">You can optimize your application so the server stub does not free memory on the server at the conclusion of a remote procedure call.</span></span> <span data-ttu-id="a2254-105">Par exemple, lorsqu’un descripteur de contexte est manipulé par plusieurs procédures distantes, vous pouvez utiliser l’attribut ACF **\[ allocate (ne pas \_ libérer) \]** pour conserver la mémoire allouée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a2254-105">For example, when a context handle will be manipulated by several remote procedures, you can use the ACF attribute **\[allocate(dont\_free)\]** to retain the allocated memory on the server.</span></span>

<span data-ttu-id="a2254-106">L’attribut **\[ allocate (ne pas \_ libérer) \]** est ajouté à la déclaration de **typedef** ACF dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="a2254-106">The **\[allocate(dont\_free)\]** attribute is added to the ACF **typedef** declaration in the ACF.</span></span> <span data-ttu-id="a2254-107">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a2254-107">For example:</span></span>

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

<span data-ttu-id="a2254-108">Lorsque l’attribut **\[ allocate (ne pas \_ libérer) \]** est spécifié, la structure des données de l’arborescence est allouée, mais pas libérée, par le stub serveur.</span><span class="sxs-lookup"><span data-stu-id="a2254-108">When the **\[allocate(dont\_free)\]** attribute is specified, the tree data structure is allocated, but not freed, by the server stub.</span></span> <span data-ttu-id="a2254-109">Lorsque vous rendez les pointeurs vers des zones de données persistantes disponibles pour d’autres routines, par exemple en copiant les pointeurs vers des variables globales, les données conservées sont accessibles aux autres fonctions serveur.</span><span class="sxs-lookup"><span data-stu-id="a2254-109">When you make the pointers to such persistent data areas available to other routines—for example, by copying the pointers to global variables—the retained data is accessible to other server functions.</span></span> <span data-ttu-id="a2254-110">L’attribut **\[ allocate (ne pas \_ libérer) \]** est particulièrement utile pour gérer les structures de pointeur persistantes dans le cadre des informations d’État du serveur associées à un type de handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="a2254-110">The **\[allocate(dont\_free)\]** attribute is particularly useful for maintaining persistent pointer structures as part of the server state information associated with a context-handle type.</span></span>

 

 




