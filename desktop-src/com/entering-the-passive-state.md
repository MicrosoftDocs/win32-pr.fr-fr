---
title: Passage à l’état passif
description: Passage à l’état passif
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840665"
---
# <a name="entering-the-passive-state"></a><span data-ttu-id="3ab58-103">Passage à l’état passif</span><span class="sxs-lookup"><span data-stu-id="3ab58-103">Entering the Passive State</span></span>

<span data-ttu-id="3ab58-104">La fermeture d’objet force un objet incorporé ou lié à l’état passif.</span><span class="sxs-lookup"><span data-stu-id="3ab58-104">Object closure forces an embedded or linked object into the passive state.</span></span> <span data-ttu-id="3ab58-105">Elle est généralement lancée à partir de l’interface utilisateur de l’application serveur OLE, par exemple lorsque l’utilisateur sélectionne la commande fichier fermer.</span><span class="sxs-lookup"><span data-stu-id="3ab58-105">It is typically initiated from the OLE server application's user interface, such as when the user selects the File Close command.</span></span> <span data-ttu-id="3ab58-106">Dans ce cas, l’application serveur OLE notifie le conteneur, ce qui libère son décompte de références sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ab58-106">In this case, the OLE server application notifies the container, which releases its reference count on the object.</span></span> <span data-ttu-id="3ab58-107">Lorsque toutes les références à l’objet ont été libérées, l’objet peut être libéré.</span><span class="sxs-lookup"><span data-stu-id="3ab58-107">When all references to the object have been released, the object can be freed.</span></span> <span data-ttu-id="3ab58-108">Lorsque tous les objets ont été libérés, l’application serveur OLE peut se terminer en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="3ab58-108">When all objects have been freed, the OLE server application can safely terminate.</span></span>

<span data-ttu-id="3ab58-109">Une application conteneur peut également initier la fermeture de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ab58-109">A container application can also initiate object closure.</span></span> <span data-ttu-id="3ab58-110">Pour fermer un objet, le conteneur libère son décompte de références après avoir effectué une opération d’enregistrement facultative.</span><span class="sxs-lookup"><span data-stu-id="3ab58-110">To close an object, the container releases its reference count after completing an optional save operation.</span></span> <span data-ttu-id="3ab58-111">Vous pouvez concevoir des conteneurs pour libérer des objets lorsqu’ils sont en cours de désactivation après une session d’activation sur place, ce qui permet à l’utilisateur de cliquer à l’extérieur de l’objet sans perdre la session de modification active.</span><span class="sxs-lookup"><span data-stu-id="3ab58-111">You can design containers to release objects when they are deactivating after an in-place activation session, allowing the user to click outside the object without losing the active editing session.</span></span>

 

 




