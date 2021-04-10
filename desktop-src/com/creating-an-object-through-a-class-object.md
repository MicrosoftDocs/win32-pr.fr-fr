---
title: Création d’un objet à l’aide d’un objet de classe
description: Création d’un objet à l’aide d’un objet de classe
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940315"
---
# <a name="creating-an-object-through-a-class-object"></a><span data-ttu-id="c7966-103">Création d’un objet à l’aide d’un objet de classe</span><span class="sxs-lookup"><span data-stu-id="c7966-103">Creating an Object Through a Class Object</span></span>

<span data-ttu-id="c7966-104">Avec l’importance croissante des réseaux informatiques, il est devenu nécessaire que les clients et les serveurs interagissent aisément et efficacement, qu’ils se trouvent sur le même ordinateur ou sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="c7966-104">With the increasing importance of computer networks, it has become necessary for clients and servers to interact easily and efficiently, whether they reside on the same machine or across a network.</span></span> <span data-ttu-id="c7966-105">L’un des aspects essentiels est la possibilité pour un client de lancer un serveur, de créer une instance de l’objet du serveur et d’avoir accès aux méthodes des interfaces sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="c7966-105">Crucial to this is a client's ability to launch a server, create an instance of the server's object, and have access to the methods of the interfaces on the object.</span></span>

<span data-ttu-id="c7966-106">COM fournit des extensions à ce processus COM de base qui le rend quasiment transparent sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="c7966-106">COM provides extensions to this basic COM process that make it virtually seamless across a network.</span></span> <span data-ttu-id="c7966-107">Si un client est en mesure d’identifier le serveur via son CLSID, l’appel de quelques fonctions simples permet à COM d’effectuer tout le travail de recherche et de lancement du serveur et d’activation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c7966-107">If a client is able to identify the server through its CLSID, calling a few simple functions permit COM to do all the work of locating and launching the server and activating the object.</span></span> <span data-ttu-id="c7966-108">Les sous-clés du registre permettent aux serveurs distants d’inscrire leur emplacement, de sorte que le client n’a pas besoin de ces informations.</span><span class="sxs-lookup"><span data-stu-id="c7966-108">Subkeys in the registry allow remote servers to register their location, so the client does not require that information.</span></span> <span data-ttu-id="c7966-109">Pour les applications qui souhaitent tirer parti des fonctionnalités de mise en réseau, les fonctions de création d’objets COM offrent davantage de flexibilité et d’efficacité.</span><span class="sxs-lookup"><span data-stu-id="c7966-109">For applications that want to take advantage of networking features, the COM object creation functions allow more flexibility and efficiency.</span></span>

<span data-ttu-id="c7966-110">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7966-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c7966-111">Objets de classe COM et CLSID</span><span class="sxs-lookup"><span data-stu-id="c7966-111">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
-   [<span data-ttu-id="c7966-112">Localisation d’un objet distant</span><span class="sxs-lookup"><span data-stu-id="c7966-112">Locating a Remote Object</span></span>](locating-a-remote-object.md)
-   [<span data-ttu-id="c7966-113">Fonctions d’assistance pour la création d’instances</span><span class="sxs-lookup"><span data-stu-id="c7966-113">Instance Creation Helper Functions</span></span>](instance-creation-helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="c7966-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7966-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7966-115">Clients et serveurs COM</span><span class="sxs-lookup"><span data-stu-id="c7966-115">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




