---
title: Passage à l’État en cours d’exécution
description: Passage à l’État en cours d’exécution
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939903"
---
# <a name="entering-the-running-state"></a><span data-ttu-id="628ea-103">Passage à l’État en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="628ea-103">Entering the Running State</span></span>

<span data-ttu-id="628ea-104">Lorsqu’un objet incorporé effectue la transition vers l’État en cours d’exécution, le gestionnaire d’objets doit localiser et exécuter l’application serveur afin d’utiliser les services fournis par le serveur.</span><span class="sxs-lookup"><span data-stu-id="628ea-104">When an embedded object makes the transition to the running state, the object handler must locate and run the server application in order to utilize the services that only the server provides.</span></span> <span data-ttu-id="628ea-105">Les objets incorporés sont placés à l’État en cours d’exécution, soit explicitement via une requête du conteneur, par exemple, il est nécessaire de dessiner un format qui n’est pas actuellement mis en cache, ou implicitement par OLE en réponse à l’appel d’une opération, par exemple lorsqu’un utilisateur du conteneur double-clique sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="628ea-105">Embedded objects are placed in the running state either explicitly through a request by the container, such as a need to draw a format not currently cached, or implicitly by OLE in response to invoking some operation, such as when a user of the container double-clicks the object.</span></span>

<span data-ttu-id="628ea-106">Lorsqu’un objet lié rend la transition à l’État en cours d’exécution, le processus est appelé *liaison*.</span><span class="sxs-lookup"><span data-stu-id="628ea-106">When a linked object makes the transition into the running state, the process is known as *binding*.</span></span> <span data-ttu-id="628ea-107">Dans le processus de liaison, le gestionnaire d’objets demande à son moniker stocké de localiser les données du lien, puis exécute l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="628ea-107">In the process of binding, the object handler asks its stored moniker to locate the link's data, then runs the server application.</span></span>

<span data-ttu-id="628ea-108">À première vue, la liaison d’un objet lié semble ne pas être plus compliquée que l’exécution d’un objet incorporé.</span><span class="sxs-lookup"><span data-stu-id="628ea-108">At first glance, binding a linked object appears to be no more complicated than running an embedded object.</span></span> <span data-ttu-id="628ea-109">Toutefois, les points suivants compliquent le processus :</span><span class="sxs-lookup"><span data-stu-id="628ea-109">However, the following points complicate the process:</span></span>

-   <span data-ttu-id="628ea-110">Un lien peut faire référence à un objet, ou une partie de celui-ci, qui est incorporé dans un autre conteneur.</span><span class="sxs-lookup"><span data-stu-id="628ea-110">A link can refer to an object, or a portion thereof, that is embedded in another container.</span></span> <span data-ttu-id="628ea-111">Cette fonctionnalité implique un potentiel pour les incorporations imbriquées.</span><span class="sxs-lookup"><span data-stu-id="628ea-111">This capability implies a potential for nested embeddings.</span></span> <span data-ttu-id="628ea-112">Pour résoudre les références à une telle hiérarchie, vous devez parcourir de manière récursive un *moniker composite*, en commençant par le membre le plus à droite.</span><span class="sxs-lookup"><span data-stu-id="628ea-112">Resolving references to such a hierarchy requires recursively traversing a *composite moniker*, beginning with the rightmost member.</span></span>
-   <span data-ttu-id="628ea-113">Lorsque la source de la liaison est en cours d’exécution, OLE se lie à l’instance en cours d’exécution de l’objet au lieu d’exécuter une autre instance.</span><span class="sxs-lookup"><span data-stu-id="628ea-113">When the link source is running, OLE binds to the running instance of the object rather than running another instance.</span></span> <span data-ttu-id="628ea-114">Dans le cas d’objets incorporés imbriqués, dont l’un est la source de la liaison, OLE doit être en mesure d’effectuer une liaison à un objet déjà en cours d’exécution à tout moment.</span><span class="sxs-lookup"><span data-stu-id="628ea-114">In the case of nested embedded objects, one of which is the link source, OLE must be able to bind to an already running object at any point.</span></span>
-   <span data-ttu-id="628ea-115">L’exécution d’un objet requiert l’accès à la zone de stockage pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="628ea-115">Running an object requires accessing the storage area for the object.</span></span> <span data-ttu-id="628ea-116">Lorsqu’un objet incorporé est exécuté, OLE reçoit un pointeur vers le stockage pendant le processus de chargement, qu’il transmet à l’application serveur OLE.</span><span class="sxs-lookup"><span data-stu-id="628ea-116">When an embedded object is run, OLE receives a pointer to the storage during the load process, which it passes on to the OLE server application.</span></span> <span data-ttu-id="628ea-117">Toutefois, pour les objets liés, il n’existe pas d’interface standard pour accéder au stockage.</span><span class="sxs-lookup"><span data-stu-id="628ea-117">For linked objects, however, there is no standard interface for accessing storage.</span></span> <span data-ttu-id="628ea-118">L’application serveur OLE peut utiliser l’interface du système de fichiers ou un autre mécanisme.</span><span class="sxs-lookup"><span data-stu-id="628ea-118">The OLE server application may use the file system interface or some other mechanism.</span></span>

 

 




