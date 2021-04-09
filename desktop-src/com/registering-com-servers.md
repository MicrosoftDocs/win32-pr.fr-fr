---
title: Inscription des serveurs COM
description: Inscription des serveurs COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102377"
---
# <a name="registering-com-servers"></a><span data-ttu-id="bd1e5-103">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="bd1e5-103">Registering COM Servers</span></span>

<span data-ttu-id="bd1e5-104">Après avoir défini une classe dans le code (en veillant à ce qu’elle implémente [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) et lui ait assigné un CLSID, vous devez placer dans le registre des informations qui permettront à com, à la demande d’un client avec le CLSID, de créer des instances de ses objets.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-104">After you have defined a class in code (ensuring that it implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) and assigned it a CLSID, you need to put information in the registry that will allow COM, on request of a client with the CLSID, to create instances of its objects.</span></span> <span data-ttu-id="bd1e5-105">Ces informations indiquent au système, pour un CLSID donné, où se trouve le code DLL ou EXE de cette classe et comment il doit être lancé.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-105">This information tells the system, for a given CLSID, where the DLL or EXE code for that class is located and how it is to be launched.</span></span>

<span data-ttu-id="bd1e5-106">Il existe plusieurs façons d’inscrire une classe dans le registre.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-106">There is more than one way of registering a class in the registry.</span></span> <span data-ttu-id="bd1e5-107">En outre, il existe d’autres façons d’inscrire une classe dans le système lorsqu’elle s’exécute, de sorte que le système sait qu’un objet en cours d’exécution est actuellement dans le système.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-107">In addition, there are other ways of "registering" a class with the system when it is running, so that the system is aware that a running object is currently in the system.</span></span>

<span data-ttu-id="bd1e5-108">Pour plus d’informations sur l’inscription, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd1e5-108">See the following topics for more information about registering:</span></span>

-   [<span data-ttu-id="bd1e5-109">Inscription d’une classe lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="bd1e5-109">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
-   [<span data-ttu-id="bd1e5-110">Inscription d’un serveur exécutable en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="bd1e5-110">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
-   [<span data-ttu-id="bd1e5-111">Inscription d’objets dans le ROT</span><span class="sxs-lookup"><span data-stu-id="bd1e5-111">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
-   [<span data-ttu-id="bd1e5-112">Inscription automatique</span><span class="sxs-lookup"><span data-stu-id="bd1e5-112">Self-Registration</span></span>](self-registration.md)
-   [<span data-ttu-id="bd1e5-113">Installation d’une application en tant que service</span><span class="sxs-lookup"><span data-stu-id="bd1e5-113">Installing as a Service Application</span></span>](installing-as-a-service-application.md)

## <a name="related-topics"></a><span data-ttu-id="bd1e5-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd1e5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd1e5-115">Responsabilités du serveur COM</span><span class="sxs-lookup"><span data-stu-id="bd1e5-115">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 