---
title: Serveurs In-Process
description: Serveurs In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196734"
---
# <a name="in-process-servers"></a><span data-ttu-id="aefc3-103">Serveurs In-Process</span><span class="sxs-lookup"><span data-stu-id="aefc3-103">In-Process Servers</span></span>

<span data-ttu-id="aefc3-104">Si vous implémentez une application serveur OLE en tant que serveur in-process, une DLL s’exécutant dans l’espace de processus de l’application conteneur, plutôt qu’en tant que serveur local, un EXE qui s’exécute dans son propre espace de processus, la communication entre le conteneur et le serveur est simplifiée, car la communication entre les deux peut prendre la forme d’appels de fonction normaux.</span><span class="sxs-lookup"><span data-stu-id="aefc3-104">If you implement an OLE server application as an in-process server — a DLL running in the process space of the container application — rather than as a local server — an EXE running in its own process space — communication between container and server is simplified because communication between the two can take the form of normal function calls.</span></span> <span data-ttu-id="aefc3-105">Les appels de procédure distante ne sont pas nécessaires, car les deux applications s’exécutent dans le même espace de processus.</span><span class="sxs-lookup"><span data-stu-id="aefc3-105">Remote procedure calls are not required because the two applications run in the same process space.</span></span> <span data-ttu-id="aefc3-106">Comme vous pouvez vous y attendre, les objets qui gèrent le marshaling des paramètres sont également inutiles, bien qu’ils puissent être agrégés dans la DLL sans interférer avec la communication entre le conteneur et le serveur.</span><span class="sxs-lookup"><span data-stu-id="aefc3-106">As you would expect, the objects that manage the marshaling of parameters are also unnecessary, although they may be aggregated within the DLL without interfering with the communication between container and server.</span></span>

<span data-ttu-id="aefc3-107">Lorsqu’une application serveur OLE est implémentée en tant que serveur in-process, un gestionnaire d’objets distinct n’est pas nécessaire, car le serveur lui-même réside dans l’espace de processus du client.</span><span class="sxs-lookup"><span data-stu-id="aefc3-107">When an OLE server application is implemented as an in-process server, a separate object handler is not required because the server itself lives in the client's process space.</span></span> <span data-ttu-id="aefc3-108">La principale différence entre un serveur in-process et un gestionnaire d’objets est que le serveur est en mesure de gérer l’objet dans un État en cours d’exécution alors que le gestionnaire ne le peut pas.</span><span class="sxs-lookup"><span data-stu-id="aefc3-108">The main difference between an in-process server and object handler is that the server is able to manage the object in a running state while the handler cannot.</span></span> <span data-ttu-id="aefc3-109">L’une des conséquences de cette différence est qu’un serveur doit fournir une interface utilisateur pour manipuler l’objet en cours d’exécution, tandis qu’un gestionnaire délègue cette exigence au serveur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aefc3-109">One consequence of this difference is that a server must provide a user interface for manipulating the running object, while a handler delegates this requirement to the object's server.</span></span> <span data-ttu-id="aefc3-110">Lors de la création d’un serveur in-process, vous pouvez effectuer un agrégat sur le gestionnaire OLE par défaut, ce qui lui permet de gérer les tâches de base, telles que l’affichage, le stockage et les notifications, lorsque vous implémentez uniquement les services que le gestionnaire ne fournit pas ou n’implémente pas de la façon dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="aefc3-110">In creating an in-process server, you can aggregate on the OLE default handler, letting it handle basic chores, such as display, storage, and notifications while you implement only those services that the handler either does not provide or does not implement in the way you require.</span></span>

<span data-ttu-id="aefc3-111">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="aefc3-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="aefc3-112">Avantages</span><span class="sxs-lookup"><span data-stu-id="aefc3-112">Advantages</span></span>](advantages.md)
-   [<span data-ttu-id="aefc3-113">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="aefc3-113">Disadvantages</span></span>](disadvantages.md)

## <a name="related-topics"></a><span data-ttu-id="aefc3-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aefc3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aefc3-115">Documents composés</span><span class="sxs-lookup"><span data-stu-id="aefc3-115">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




