---
title: Mode de tunnel
description: Le scénario de stratégie IPsec en mode tunnel est utilisé pour appliquer la protection du mode de tunnel IPsec pour tout le trafic correspondant entre deux points de terminaison de tunnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310693"
---
# <a name="tunnel-mode"></a><span data-ttu-id="5b842-103">Mode de tunnel</span><span class="sxs-lookup"><span data-stu-id="5b842-103">Tunnel Mode</span></span>

<span data-ttu-id="5b842-104">Le scénario de stratégie IPsec en mode tunnel est utilisé pour appliquer la protection du mode de tunnel IPsec pour tout le trafic correspondant entre deux points de terminaison de tunnel.</span><span class="sxs-lookup"><span data-stu-id="5b842-104">The Tunnel Mode IPsec policy scenario is used to apply IPsec tunnel mode protection for all matching traffic between two tunnel endpoints.</span></span>

<span data-ttu-id="5b842-105">Ce scénario de stratégie est généralement utilisé pour protéger le trafic entre plusieurs sous-réseaux de succursales, lorsqu’il est transféré entre les passerelles correspondantes sur Internet.</span><span class="sxs-lookup"><span data-stu-id="5b842-105">This policy scenario is typically used to protect traffic between multiple branch-office subnets, when it gets forwarded between the corresponding gateways on the Internet.</span></span> <span data-ttu-id="5b842-106">Il peut également être utilisé pour sécuriser la communication de bout en bout entre deux ordinateurs hôtes, également appelés tunnels point à point.</span><span class="sxs-lookup"><span data-stu-id="5b842-106">It can also be used to secure end-to-end communication between two host machines, also referred to as point-to-point tunnels.</span></span>

<span data-ttu-id="5b842-107">Pour implémenter une stratégie de mode de tunnel à l’aide de la plateforme de filtrage Windows (WFP), appelez la fonction [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) qui instancie les filtres de mode de tunnel appropriés aux couches appropriées pour le compte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5b842-107">To implement Tunnel Mode policy using the Windows Filtering Platform (WFP), call the [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) function that instantiates the appropriate tunnel mode filters at the appropriate layers on behalf of the caller.</span></span> <span data-ttu-id="5b842-108">L’appelant doit spécifier le mode principal, les contextes de fournisseur en mode rapide et les conditions de filtre qui décrivent le trafic qui doit être sécurisé à l’intérieur du tunnel.</span><span class="sxs-lookup"><span data-stu-id="5b842-108">The caller needs to specify the Main Mode, Quick Mode provider contexts, and the filter conditions describing the traffic that should be secured inside the tunnel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b842-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b842-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b842-110">Exemple de code : utilisation du mode de tunnel</span><span class="sxs-lookup"><span data-stu-id="5b842-110">Sample code: Using Tunnel Mode</span></span>](using-tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="5b842-111">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="5b842-111">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




