---
description: Moniteur réseau transmet toutes les trames d’une capture aux analyseurs, puis commence à appeler la fonction de désinscription pour tous les protocoles qu’elle identifie. Chaque DLL de l’analyseur doit implémenter une fonction de désinscription pour chaque protocole pris en charge par la DLL de l’analyseur.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implémentation de l’annulation de l’inscription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512954"
---
# <a name="implementing-deregister"></a><span data-ttu-id="f6473-104">Implémentation de l’annulation de l’inscription</span><span class="sxs-lookup"><span data-stu-id="f6473-104">Implementing Deregister</span></span>

<span data-ttu-id="f6473-105">Moniteur réseau transmet toutes les trames d’une capture aux analyseurs, puis commence à appeler la fonction de [**désinscription**](deregister.md) pour tous les protocoles qu’elle identifie.</span><span class="sxs-lookup"><span data-stu-id="f6473-105">Network Monitor passes all the frames of a capture to the parsers, and then starts calling the [**Deregister**](deregister.md) function for all the protocols it identifies.</span></span> <span data-ttu-id="f6473-106">Chaque DLL de l’analyseur doit implémenter une fonction de **désinscription** pour chaque protocole pris en charge par la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="f6473-106">Each parser DLL must implement a **Deregister** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="f6473-107">Chaque implémentation de la fonction de [**désinscription**](deregister.md) doit appeler la fonction [**DestroyProtocolDatabase**](destroypropertydatabase.md) pour libérer les ressources utilisées pour créer la base de données.</span><span class="sxs-lookup"><span data-stu-id="f6473-107">Each implementation of the [**Deregister**](deregister.md) function must call the [**DestroyProtocolDatabase**](destroypropertydatabase.md) function to release the resources that are used to create the database.</span></span>

<span data-ttu-id="f6473-108">La procédure suivante identifie la seule étape nécessaire à l’implémentation de l’annulation de l' [**inscription**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="f6473-108">The following procedure identifies the one step necessary to implement [**Deregister**](deregister.md).</span></span>

<span data-ttu-id="f6473-109">**Pour implémenter l’annulation de l’inscription pour un protocole**</span><span class="sxs-lookup"><span data-stu-id="f6473-109">**To implement Deregister for one protocol**</span></span>

-   <span data-ttu-id="f6473-110">Appelez [**DestroyProtocolDatabase**](destroypropertydatabase.md) pour libérer les ressources de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f6473-110">Call [**DestroyProtocolDatabase**](destroypropertydatabase.md) to release the database resources.</span></span>

<span data-ttu-id="f6473-111">Voici une implémentation de base de l' [**annulation**](deregister.md)de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="f6473-111">The following is a basic implementation of [**Deregister**](deregister.md).</span></span> <span data-ttu-id="f6473-112">Notez que l’exemple de code montre la mise en sortie des ressources utilisées pour créer une base de données de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f6473-112">Note that the code example shows the release of resources that are used to create a property database.</span></span>

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



