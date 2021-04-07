---
title: Gestionnaire par défaut et gestionnaires personnalisés
description: Gestionnaire par défaut et gestionnaires personnalisés
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939787"
---
# <a name="the-default-handler-and-custom-handlers"></a><span data-ttu-id="61476-103">Gestionnaire par défaut et gestionnaires personnalisés</span><span class="sxs-lookup"><span data-stu-id="61476-103">The Default Handler and Custom Handlers</span></span>

<span data-ttu-id="61476-104">Le gestionnaire par défaut, une implémentation fournie par OLE, est utilisé par la plupart des applications comme gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="61476-104">The default handler, an implementation provided by OLE, is used by most applications as the handler.</span></span> <span data-ttu-id="61476-105">Une application implémente un gestionnaire personnalisé lorsque les fonctionnalités du gestionnaire par défaut sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="61476-105">An application implements a custom handler when the default handler's capabilities are insufficient.</span></span> <span data-ttu-id="61476-106">Un gestionnaire personnalisé peut remplacer complètement le gestionnaire par défaut ou utiliser des parties de la fonctionnalité qu’il fournit, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="61476-106">A custom handler can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="61476-107">Dans ce dernier cas, le gestionnaire d’application est implémenté comme un objet d’agrégation composé d’un nouvel objet de contrôle et du gestionnaire par défaut.</span><span class="sxs-lookup"><span data-stu-id="61476-107">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="61476-108">Les gestionnaires d’applications/par défaut combinés sont également appelés *gestionnaires in-process*.</span><span class="sxs-lookup"><span data-stu-id="61476-108">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="61476-109">Le *Gestionnaire de communication à distance* est utilisé pour les objets qui ne sont pas affectés à un CLSID dans le registre système ou qui n’ont pas de gestionnaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="61476-109">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="61476-110">Tout ce qui est nécessaire à partir d’un gestionnaire pour ces types d’objets est qu’ils passent des informations à travers la limite de processus.</span><span class="sxs-lookup"><span data-stu-id="61476-110">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61476-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61476-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61476-112">Gestionnaires d’objets</span><span class="sxs-lookup"><span data-stu-id="61476-112">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




