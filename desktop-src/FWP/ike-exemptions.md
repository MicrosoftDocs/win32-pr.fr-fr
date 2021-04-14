---
title: Exemptions IKE/AuthIP
description: Protocole IKE (Internet Key Exchange) (IKE) et protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP), afin de fonctionner, doivent exempter le trafic réseau du filtrage IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381567"
---
# <a name="ikeauthip-exemptions"></a><span data-ttu-id="1e39e-103">Exemptions IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="1e39e-103">IKE/AuthIP Exemptions</span></span>

<span data-ttu-id="1e39e-104">Les modules de génération de clés IPsec (Internet Protocol Security), protocole IKE (Internet Key Exchange) (IKE) et protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP), afin de fonctionner, doivent exempter le trafic réseau du filtrage IPsec.</span><span class="sxs-lookup"><span data-stu-id="1e39e-104">The Internet Protocol security (IPsec) keying modules, Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP), in order to function, need to exempt their network traffic from the IPsec filtering.</span></span>

<span data-ttu-id="1e39e-105">Dans la plateforme de filtrage Windows (WFP), le moteur de filtrage de base (BFE) ajoute automatiquement des filtres d’exemption IKE et AuthIP lorsque le filtre de stratégie en mode principal IKE ou AuthIP (MM) est ajouté et les supprime lorsque le dernier filtre de stratégie IKE ou AuthIP MM est supprimé.</span><span class="sxs-lookup"><span data-stu-id="1e39e-105">In Windows Filtering Platform (WFP) the Base Filtering Engine (BFE) automatically adds IKE and AuthIP exemption filters when the first IKE or AuthIP main mode (MM) policy filter is added and deletes them when the last IKE or AuthIP MM policy filter is deleted.</span></span> <span data-ttu-id="1e39e-106">De cette façon, les fournisseurs de stratégie n’ont pas à gérer individuellement les exemptions de filtrage IKE et AuthIP.</span><span class="sxs-lookup"><span data-stu-id="1e39e-106">This way, the policy providers do not have to manage IKE and AuthIP filtering exemptions individually.</span></span>

<span data-ttu-id="1e39e-107">Un filtre de stratégie IKE MM est un filtre dans la couche de moteur [**FWPM \_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) qui fait référence à un contexte de fournisseur de type [**FWPM \_ IPSec \_ IKE \_ mm \_ Context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="1e39e-107">An IKE MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_IKE\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="1e39e-108">Un filtre de stratégie AuthIP MM est un filtre dans la couche de moteur [**FWPM \_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) qui fait référence à un contexte de fournisseur de type [**FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="1e39e-108">An AuthIP MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="1e39e-109">Un filtre d’exemption IKE ou AuthIP est un filtre dans la couche FWPM couche du moteur [**\_ \_ \_ transport entrant \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) ou transport sortant de la couche **FWPM \_ \_ \_ \_ v {4 \| 6}** pondéré automatiquement dans la plage de poids [**FWPM les \_ \_ \_ \_ exemptions IKE**](filter-weight-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="1e39e-109">An IKE or AuthIP exemption filter is a filter in the engine layer [**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}**](management-filtering-layer-identifiers-.md) or **FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}** auto-weighted in the [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md) weight range.</span></span>

<span data-ttu-id="1e39e-110">Les exemptions IKE et AuthIP implémentées par BFE sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e39e-110">The IKE and AuthIP exemptions implemented by BFE are as follows.</span></span>

| <span data-ttu-id="1e39e-111">Version de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="1e39e-111">IP version</span></span>      | <span data-ttu-id="1e39e-112">Port</span><span class="sxs-lookup"><span data-stu-id="1e39e-112">Port</span></span>                        | <span data-ttu-id="1e39e-113">Exemption</span><span class="sxs-lookup"><span data-stu-id="1e39e-113">Exemption</span></span>                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e39e-114">IPv4</span><span class="sxs-lookup"><span data-stu-id="1e39e-114">IPv4</span></span><br/> | <span data-ttu-id="1e39e-115">UDP : 500 UDP : 4500</span><span class="sxs-lookup"><span data-stu-id="1e39e-115">UDP:500 UDP:4500</span></span><br/> | <span data-ttu-id="1e39e-116">Autorisez le trafic IKE et AuthIP au niveau de la couche de transport entrante et au niveau de la couche de transport sortante.</span><span class="sxs-lookup"><span data-stu-id="1e39e-116">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="1e39e-117">Autorisez le trafic IKE et AuthIP aux couches de réception/acceptation et de connexion ALE, mais limitez-les au système local.</span><span class="sxs-lookup"><span data-stu-id="1e39e-117">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |
| <span data-ttu-id="1e39e-118">IPv6</span><span class="sxs-lookup"><span data-stu-id="1e39e-118">IPv6</span></span><br/> | <span data-ttu-id="1e39e-119">UDP : 500</span><span class="sxs-lookup"><span data-stu-id="1e39e-119">UDP:500</span></span><br/>          | <span data-ttu-id="1e39e-120">Autorisez le trafic IKE et AuthIP au niveau de la couche de transport entrante et au niveau de la couche de transport sortante.</span><span class="sxs-lookup"><span data-stu-id="1e39e-120">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="1e39e-121">Autorisez le trafic IKE et AuthIP aux couches de réception/acceptation et de connexion ALE, mais limitez-les au système local.</span><span class="sxs-lookup"><span data-stu-id="1e39e-121">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |



 

<span data-ttu-id="1e39e-122">Les filtres d’exemption IKE et AuthIP sont ouverts à toutes les adresses.</span><span class="sxs-lookup"><span data-stu-id="1e39e-122">The IKE and AuthIP exemption filters are open to all addresses.</span></span> <span data-ttu-id="1e39e-123">Pour implémenter un pare-feu avec un contrôle plus granulaire, les fournisseurs de stratégie doivent ajouter des filtres dans une plage de poids supérieure à celle des [**\_ \_ \_ \_ exemptions IKE**](filter-weight-identifiers.md)de la plage de poids de FWPM.</span><span class="sxs-lookup"><span data-stu-id="1e39e-123">To implement a firewall with more granular control, policy providers should add filters in a weight range higher than [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e39e-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e39e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e39e-125">Configuration IPsec</span><span class="sxs-lookup"><span data-stu-id="1e39e-125">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="1e39e-126">Affectation de poids de filtre</span><span class="sxs-lookup"><span data-stu-id="1e39e-126">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

 





