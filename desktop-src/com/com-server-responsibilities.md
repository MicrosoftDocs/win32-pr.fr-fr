---
title: Responsabilités du serveur COM
description: Responsabilités du serveur COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382959"
---
# <a name="com-server-responsibilities"></a><span data-ttu-id="cd165-103">Responsabilités du serveur COM</span><span class="sxs-lookup"><span data-stu-id="cd165-103">COM Server Responsibilities</span></span>

<span data-ttu-id="cd165-104">L’une des façons les plus importantes pour un client d’obtenir un pointeur vers un objet est que le client demande qu’un serveur soit lancé et qu’une instance de l’objet fourni par le serveur soit créée et activée.</span><span class="sxs-lookup"><span data-stu-id="cd165-104">One of the most important ways for a client to get a pointer to an object is for the client to ask that a server be launched and that an instance of the object provided by the server be created and activated.</span></span> <span data-ttu-id="cd165-105">Il incombe au serveur de s’assurer que cela se produit correctement.</span><span class="sxs-lookup"><span data-stu-id="cd165-105">It is the responsibility of the server to ensure that this happens properly.</span></span> <span data-ttu-id="cd165-106">Il existe plusieurs parties importantes.</span><span class="sxs-lookup"><span data-stu-id="cd165-106">There are several important parts to this.</span></span>

<span data-ttu-id="cd165-107">Le serveur doit implémenter le code d’un objet de classe par le biais d’une implémentation de l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .</span><span class="sxs-lookup"><span data-stu-id="cd165-107">The server must implement code for a class object through an implementation of either the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface.</span></span>

<span data-ttu-id="cd165-108">Le serveur doit inscrire son CLSID dans le registre système sur l’ordinateur sur lequel il se trouve et il est également possible de publier son emplacement d’ordinateur sur d’autres systèmes sur un réseau pour permettre aux clients de l’appeler sans que le client ait besoin de connaître l’emplacement du serveur.</span><span class="sxs-lookup"><span data-stu-id="cd165-108">The server must register its CLSID in the system registry on the machine on which it resides and further, has the option of publishing its machine location to other systems on a network to allow clients to call it without requiring the client to know the server's location.</span></span>

<span data-ttu-id="cd165-109">Le serveur est principalement responsable de la sécurité ; autrement dit, dans la plupart des cas, le serveur détermine s’il doit fournir un pointeur vers l’un de ses objets à un client.</span><span class="sxs-lookup"><span data-stu-id="cd165-109">The server is primarily responsible for security; that is, for the most part, the server determines whether it will provide a pointer to one of its objects to a client.</span></span>

<span data-ttu-id="cd165-110">Les serveurs in-process doivent implémenter et exporter certaines fonctions qui permettent au processus client de les instancier.</span><span class="sxs-lookup"><span data-stu-id="cd165-110">In-process servers should implement and export certain functions that allow the client process to instantiate them.</span></span>

<span data-ttu-id="cd165-111">Les rubriques suivantes détaillent les responsabilités du serveur COM :</span><span class="sxs-lookup"><span data-stu-id="cd165-111">The following topics detail the responsibilities of the COM server:</span></span>

-   [<span data-ttu-id="cd165-112">Implémentation de IClassFactory</span><span class="sxs-lookup"><span data-stu-id="cd165-112">Implementing IClassFactory</span></span>](implementing-iclassfactory.md)
-   [<span data-ttu-id="cd165-113">Licences et IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="cd165-113">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
-   [<span data-ttu-id="cd165-114">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="cd165-114">Registering COM Servers</span></span>](registering-com-servers.md)
-   [<span data-ttu-id="cd165-115">Assistances pour l’implémentation de serveur hors processus</span><span class="sxs-lookup"><span data-stu-id="cd165-115">Out-of-Process Server Implementation Helpers</span></span>](out-of-process-server-implementation-helpers.md)
-   [<span data-ttu-id="cd165-116">Création et optimisations de GUID</span><span class="sxs-lookup"><span data-stu-id="cd165-116">GUID Creation and Optimizations</span></span>](guid-creation-and-optimizations.md)

## <a name="related-topics"></a><span data-ttu-id="cd165-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd165-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd165-118">Clients et serveurs COM</span><span class="sxs-lookup"><span data-stu-id="cd165-118">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 