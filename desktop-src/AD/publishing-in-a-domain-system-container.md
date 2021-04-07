---
title: Publication dans un conteneur de système de domaine
description: Le conteneur système d’une partition de domaine contient des informations opérationnelles par domaine.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publication dans un conteneur de système de domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839274"
---
# <a name="publishing-in-a-domain-system-container"></a><span data-ttu-id="97bcc-104">Publication dans un conteneur de système de domaine</span><span class="sxs-lookup"><span data-stu-id="97bcc-104">Publishing in a Domain System Container</span></span>

<span data-ttu-id="97bcc-105">Le conteneur système d’une partition de domaine contient des informations opérationnelles par domaine.</span><span class="sxs-lookup"><span data-stu-id="97bcc-105">The System container of a domain partition holds per-domain operational information.</span></span> <span data-ttu-id="97bcc-106">Cela comprend la stratégie de sécurité locale par défaut, le suivi des liaisons de fichiers, les réunions réseau et les conteneurs pour les points de connexion de résolution et d’inscription Windows Sockets (RnR) et de service de noms RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="97bcc-106">This includes the default local security policy, file link tracking, network meetings, and containers for Windows Sockets registration and resolution (RnR) and RPC name service (RpcNs) connection points.</span></span> <span data-ttu-id="97bcc-107">Le conteneur système est masqué par défaut et fournit un emplacement pratique pour le stockage des objets qui présentent un intérêt pour les administrateurs, mais pas pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="97bcc-107">The system container is hidden, by default, and provides a convenient place for storing objects that are of interest to administrators, but not to end users.</span></span>

<span data-ttu-id="97bcc-108">Les services qui ne sont pas liés à un seul hôte peuvent créer leur SCP sous le conteneur système d’une partition de domaine.</span><span class="sxs-lookup"><span data-stu-id="97bcc-108">Services that are not tied to a single host may want to create their SCPs under the System container of a domain partition.</span></span> <span data-ttu-id="97bcc-109">Cette alternative peut être utile pour les services dont les réplicas sont installés sur plusieurs hôtes, chaque réplica fournissant des services identiques aux clients dans l’ensemble du domaine.</span><span class="sxs-lookup"><span data-stu-id="97bcc-109">This alternative can be useful for services with replicas installed on multiple hosts, each replica providing identical services to clients throughout the domain.</span></span> <span data-ttu-id="97bcc-110">Elle vous permet de regrouper tous les objets pour le service répliqué sous un seul conteneur.</span><span class="sxs-lookup"><span data-stu-id="97bcc-110">It enables you to group all the objects for the replicated service under a single container.</span></span>

<span data-ttu-id="97bcc-111">Les services qui créent des objets spécifiques au service dans le conteneur système doivent effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="97bcc-111">Services that create service-specific objects in the System container must do the following:</span></span>

1.  <span data-ttu-id="97bcc-112">Créez un sous-conteneur de **conteneur** de classe d’objets en tant qu’enfant immédiat du conteneur système.</span><span class="sxs-lookup"><span data-stu-id="97bcc-112">Create a sub-container of object class **container** as an immediate child of the System container.</span></span> <span data-ttu-id="97bcc-113">Donnez à ce sous-conteneur un nom qui l’identifie clairement comme appartenant au service.</span><span class="sxs-lookup"><span data-stu-id="97bcc-113">Give this sub-container a name that clearly identifies it as pertaining to the service.</span></span>
2.  <span data-ttu-id="97bcc-114">Créez les objets liés au service dans ce sous-conteneur.</span><span class="sxs-lookup"><span data-stu-id="97bcc-114">Create the service-related objects in this sub-container.</span></span> <span data-ttu-id="97bcc-115">Par exemple, NetMeeting utilise le conteneur de réunions pour publier les objets de réunion réseau.</span><span class="sxs-lookup"><span data-stu-id="97bcc-115">For example, NetMeeting uses the Meetings container to publish network meeting objects.</span></span>

<span data-ttu-id="97bcc-116">Un fournisseur avec plusieurs produits peut utiliser une stratégie similaire pour regrouper des objets liés au service pour tous ses produits.</span><span class="sxs-lookup"><span data-stu-id="97bcc-116">A vendor with multiple products can use a similar strategy to group service-related objects for all of its products.</span></span> <span data-ttu-id="97bcc-117">Dans ce cas, vous pouvez créer un objet **conteneur** avec un nom qui identifie clairement le fournisseur ; Ensuite, créez des objets **conteneurs** pour chaque service en tant qu’enfants du conteneur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="97bcc-117">In this case, you could create a **container** object with a name that clearly identifies the vendor; then create **container** objects for each service as children of the vendor container.</span></span> <span data-ttu-id="97bcc-118">Créez le conteneur spécifique au fournisseur en tant qu’enfant du conteneur système.</span><span class="sxs-lookup"><span data-stu-id="97bcc-118">Create the vendor-specific container as a child of the System container.</span></span>

 

 




