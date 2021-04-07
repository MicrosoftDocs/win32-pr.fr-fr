---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671034"
---
# <a name="microsoft-rpc"></a><span data-ttu-id="fc7de-103">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="fc7de-103">Microsoft RPC</span></span>

<span data-ttu-id="fc7de-104">Microsoft RPC est un modèle de programmation dans un environnement informatique distribué.</span><span class="sxs-lookup"><span data-stu-id="fc7de-104">Microsoft RPC is a model for programming in a distributed computing environment.</span></span> <span data-ttu-id="fc7de-105">L’objectif de RPC est de fournir une communication transparente afin que le client semble communiquer directement avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="fc7de-105">The goal of RPC is to provide transparent communication so that the client appears to be directly communicating with the server.</span></span> <span data-ttu-id="fc7de-106">L’implémentation de RPC de Microsoft est compatible avec le RPC de l’environnement d’exécution distribué (ETCD) Open Software Foundation (OSF).</span><span class="sxs-lookup"><span data-stu-id="fc7de-106">Microsoft's implementation of RPC is compatible with the Open Software Foundation (OSF) Distributed Computing Environment (DCE) RPC.</span></span>

<span data-ttu-id="fc7de-107">Vous pouvez configurer RPC pour utiliser un ou plusieurs transports, un ou plusieurs services de noms et un ou plusieurs serveurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="fc7de-107">You can configure RPC to use one or more transports, one or more name services, and one or more security servers.</span></span> <span data-ttu-id="fc7de-108">Les interfaces à ces fournisseurs sont gérées par RPC.</span><span class="sxs-lookup"><span data-stu-id="fc7de-108">The interfaces to those providers are handled by RPC.</span></span> <span data-ttu-id="fc7de-109">Étant donné que Microsoft RPC est conçu pour fonctionner avec plusieurs fournisseurs, vous pouvez choisir les fournisseurs qui conviennent le mieux à votre réseau.</span><span class="sxs-lookup"><span data-stu-id="fc7de-109">Because Microsoft RPC is designed to work with multiple providers, you can choose the providers that work best for your network.</span></span> <span data-ttu-id="fc7de-110">Le transport est responsable de la transmission des données sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="fc7de-110">The transport is responsible for transmitting the data across the network.</span></span> <span data-ttu-id="fc7de-111">Le service de noms prend un nom d’objet, tel qu’un moniker, et trouve son emplacement sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="fc7de-111">The name service takes an object name, such as a moniker, and finds its location on the network.</span></span> <span data-ttu-id="fc7de-112">Le serveur de sécurité offre aux applications la possibilité de refuser l’accès à des utilisateurs et/ou des groupes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fc7de-112">The security server offers applications the option of denying access to specific users and/or groups.</span></span> <span data-ttu-id="fc7de-113">Pour plus d’informations sur la sécurité de l’application, consultez [règles de conception d’interface](interface-design-rules.md) .</span><span class="sxs-lookup"><span data-stu-id="fc7de-113">See [Interface Design Rules](interface-design-rules.md) for more detailed information about application security.</span></span>

<span data-ttu-id="fc7de-114">En plus des bibliothèques Runtime RPC, Microsoft RPC comprend le langage IDL (Interface Definition Language) et son compilateur.</span><span class="sxs-lookup"><span data-stu-id="fc7de-114">In addition to the RPC run-time libraries, Microsoft RPC includes the Interface Definition Language (IDL) and its compiler.</span></span> <span data-ttu-id="fc7de-115">Bien que le fichier IDL soit une partie standard de RPC, Microsoft l’a amélioré pour étendre ses fonctionnalités afin de prendre en charge les interfaces COM personnalisées.</span><span class="sxs-lookup"><span data-stu-id="fc7de-115">Although the IDL file is a standard part of RPC, Microsoft has enhanced it to extend its functionality to support custom COM interfaces.</span></span> <span data-ttu-id="fc7de-116">Le compilateur Microsoft Interface Definition Language (MIDL) utilise le fichier IDL qui décrit votre interface personnalisée pour générer plusieurs fichiers décrits dans [génération et inscription d’une dll proxy](building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="fc7de-116">The Microsoft Interface Definition Language (MIDL) compiler uses the IDL file that describes your custom interface to generate several files discussed in [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc7de-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc7de-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc7de-118">Channel</span><span class="sxs-lookup"><span data-stu-id="fc7de-118">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="fc7de-119">Communication entre les objets</span><span class="sxs-lookup"><span data-stu-id="fc7de-119">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="fc7de-120">Détails du marshaling</span><span class="sxs-lookup"><span data-stu-id="fc7de-120">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="fc7de-121">Proxy</span><span class="sxs-lookup"><span data-stu-id="fc7de-121">Proxy</span></span>](proxy.md)
</dt> <dt>

[<span data-ttu-id="fc7de-122">Talon</span><span class="sxs-lookup"><span data-stu-id="fc7de-122">Stub</span></span>](stub.md)
</dt> </dl>

 

 




