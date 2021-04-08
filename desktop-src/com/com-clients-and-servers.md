---
title: Clients et serveurs COM
description: L’un des aspects essentiels de COM est la façon dont les clients et les serveurs interagissent.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673513"
---
# <a name="com-clients-and-servers"></a><span data-ttu-id="3d9e0-103">Clients et serveurs COM</span><span class="sxs-lookup"><span data-stu-id="3d9e0-103">COM Clients and Servers</span></span>

<span data-ttu-id="3d9e0-104">L’un des aspects essentiels de COM est la façon dont les clients et les serveurs interagissent.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-104">A critical aspect of COM is how clients and servers interact.</span></span> <span data-ttu-id="3d9e0-105">Un *client com* est le code ou l’objet qui obtient un pointeur vers un serveur com et utilise ses services en appelant les méthodes de ses interfaces.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-105">A *COM client* is whatever code or object gets a pointer to a COM server and uses its services by calling the methods of its interfaces.</span></span> <span data-ttu-id="3d9e0-106">Un *serveur com* est un objet qui fournit des services aux clients. ces services se présentent sous la forme d’implémentations d’interface COM qui peuvent être appelées par n’importe quel client capable d’obtenir un pointeur vers l’une des interfaces sur l’objet serveur.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-106">A *COM server* is any object that provides services to clients; these services are in the form of COM interface implementations that can be called by any client that is able to get a pointer to one of the interfaces on the server object.</span></span>

<span data-ttu-id="3d9e0-107">Il existe deux principaux types de serveurs : *in-process* et *out-of-process*.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-107">There are two main types of servers, *in-process* and *out-of-process*.</span></span> <span data-ttu-id="3d9e0-108">Les serveurs in-process sont implémentés dans une bibliothèque liée dynamique (DLL) et les serveurs hors processus sont implémentés dans un fichier exécutable (EXE).</span><span class="sxs-lookup"><span data-stu-id="3d9e0-108">In-process servers are implemented in a dynamic linked library (DLL), and out-of-process servers are implemented in an executable file (EXE).</span></span> <span data-ttu-id="3d9e0-109">Les serveurs hors processus peuvent résider sur l’ordinateur local ou sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-109">Out-of-process servers can reside either on the local computer or on a remote computer.</span></span> <span data-ttu-id="3d9e0-110">En outre, COM fournit un mécanisme qui permet à un serveur in-process (une DLL) de s’exécuter dans un processus EXE de substitution pour tirer parti de la possibilité d’exécuter le processus sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-110">In addition, COM provides a mechanism that allows an in-process server (a DLL) to run in a surrogate EXE process to gain the advantage of being able to run the process on a remote computer.</span></span> <span data-ttu-id="3d9e0-111">Pour plus d’informations, consultez [substituts de dll](dll-surrogates.md).</span><span class="sxs-lookup"><span data-stu-id="3d9e0-111">For more information, see [DLL Surrogates](dll-surrogates.md).</span></span>

<span data-ttu-id="3d9e0-112">Les constructions et le modèle de programmation COM ont été étendus pour que les clients et les serveurs COM puissent travailler ensemble sur le réseau, et pas seulement au sein d’un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-112">The COM programming model and constructs have now been extended so that COM clients and servers can work together across the network, not just within a given computer.</span></span> <span data-ttu-id="3d9e0-113">Cela permet aux applications existantes d’interagir avec de nouvelles applications et entre elles sur des réseaux avec une administration correcte, et de nouvelles applications peuvent être écrites pour tirer parti des fonctionnalités de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-113">This enables existing applications to interact with new applications and with each other across networks with proper administration, and new applications can be written to take advantage of networking features.</span></span>

<span data-ttu-id="3d9e0-114">Les applications clientes COM n’ont pas besoin de savoir comment les objets serveur sont empaquetés, qu’ils soient empaquetés en tant qu’objets in-process (dans des dll) ou en tant qu’objets locaux ou distants (dans les fichiers exe).</span><span class="sxs-lookup"><span data-stu-id="3d9e0-114">COM client applications do not need to be aware of how server objects are packaged, whether they are packaged as in-process objects (in DLLs) or as local or remote objects (in EXEs).</span></span> <span data-ttu-id="3d9e0-115">Le modèle COM distribué permet d’empaqueter des objets en tant qu’applications de service, en synchronisant COM avec les puissantes fonctionnalités d’administration et d’intégration système de Windows.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-115">Distributed COM further allows objects to be packaged as service applications, synchronizing COM with the rich administrative and system-integration capabilities of Windows.</span></span>

> [!Note]  
> <span data-ttu-id="3d9e0-116">Dans cette documentation, l’acronyme COM est utilisé de préférence à DCOM.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-116">Throughout this documentation the acronym COM is used in preference to DCOM.</span></span> <span data-ttu-id="3d9e0-117">Cela est dû au fait que DCOM n’est pas séparé ; il s’agit simplement de COM avec un câble plus long.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-117">This is because DCOM is not separate;it is just COM with a longer wire.</span></span> <span data-ttu-id="3d9e0-118">Dans les cas où la description est une opération à distance, le terme *com distribué* est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-118">In cases where what is being described is specifically a remote operation, the term *distributed COM* is used.</span></span>

 

<span data-ttu-id="3d9e0-119">COM est conçu pour permettre l’ajout de la prise en charge de la transparence d’emplacement qui s’étend sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-119">COM is designed to make it possible to add the support for location transparency that extends across a network.</span></span> <span data-ttu-id="3d9e0-120">Il permet aux applications écrites pour des ordinateurs uniques de s’exécuter sur un réseau et fournit des fonctionnalités qui étendent ces fonctionnalités et ajoutent à la sécurité nécessaire dans un réseau.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-120">It allows applications written for single computers to run across a network and provides features that extend these capabilities and add to the security necessary in a network.</span></span> <span data-ttu-id="3d9e0-121">(Pour plus d’informations, consultez [sécurité dans com](security-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="3d9e0-121">(For more information, see [Security in COM](security-in-com.md).)</span></span>

<span data-ttu-id="3d9e0-122">COM spécifie un mécanisme par lequel le code de la classe peut être utilisé par de nombreuses applications différentes.</span><span class="sxs-lookup"><span data-stu-id="3d9e0-122">COM specifies a mechanism by which the class code can be used by many different applications.</span></span>

<span data-ttu-id="3d9e0-123">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d9e0-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3d9e0-124">Obtention d’un pointeur vers un objet</span><span class="sxs-lookup"><span data-stu-id="3d9e0-124">Getting a Pointer to an Object</span></span>](getting-a-pointer-to-an-object.md)
-   [<span data-ttu-id="3d9e0-125">Création d’un objet à l’aide d’un objet de classe</span><span class="sxs-lookup"><span data-stu-id="3d9e0-125">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
-   [<span data-ttu-id="3d9e0-126">Responsabilités du serveur COM</span><span class="sxs-lookup"><span data-stu-id="3d9e0-126">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
-   [<span data-ttu-id="3d9e0-127">État persistant de l’objet</span><span class="sxs-lookup"><span data-stu-id="3d9e0-127">Persistent Object State</span></span>](persistent-object-state.md)
-   [<span data-ttu-id="3d9e0-128">Fournir des informations sur la classe</span><span class="sxs-lookup"><span data-stu-id="3d9e0-128">Providing Class Information</span></span>](providing-class-information.md)
-   [<span data-ttu-id="3d9e0-129">Communication entre les objets</span><span class="sxs-lookup"><span data-stu-id="3d9e0-129">Inter-Object Communication</span></span>](inter-object-communication.md)

## <a name="related-topics"></a><span data-ttu-id="3d9e0-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d9e0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d9e0-131">Synchronisation des appels</span><span class="sxs-lookup"><span data-stu-id="3d9e0-131">Call Synchronization</span></span>](call-synchronization.md)
</dt> <dt>

[<span data-ttu-id="3d9e0-132">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="3d9e0-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




