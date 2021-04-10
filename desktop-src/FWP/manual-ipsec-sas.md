---
title: SA manuelle
description: Le scénario de stratégie IPsec d’association de sécurité manuelle permet aux appelants de contourner les modules de génération de clé IPsec intégrés (IKE et AuthIP) en spécifiant directement les associations de sécurité IPsec pour sécuriser tout le trafic réseau.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940895"
---
# <a name="manual-sa"></a><span data-ttu-id="c68b6-103">SA manuelle</span><span class="sxs-lookup"><span data-stu-id="c68b6-103">Manual SA</span></span>

<span data-ttu-id="c68b6-104">Le scénario de stratégie IPsec d’association de sécurité manuelle permet aux appelants de contourner les modules de génération de clé IPsec intégrés (IKE et AuthIP) en spécifiant directement les associations de sécurité IPsec pour sécuriser tout le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="c68b6-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="c68b6-105">Un exemple de scénario d’association de sécurité manuelle possible est « ajouter une paire SA IPsec pour sécuriser le trafic de données de monodiffusion entre les adresses IP 1.1.1.1 & 2.2.2.2, sauf ICMP, à l’aide du mode de transport IPsec ».</span><span class="sxs-lookup"><span data-stu-id="c68b6-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="c68b6-106">Les étapes suivantes doivent être exécutées sur les deux ordinateurs avec des adresses IP définies correctement.</span><span class="sxs-lookup"><span data-stu-id="c68b6-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="c68b6-107">Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.</span><span class="sxs-lookup"><span data-stu-id="c68b6-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="c68b6-108">**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**</span><span class="sxs-lookup"><span data-stu-id="c68b6-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="c68b6-109">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c68b6-109">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="c68b6-110">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="c68b6-110">Filter property</span></span>                                                   | <span data-ttu-id="c68b6-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="c68b6-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="c68b6-112">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="c68b6-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="c68b6-113">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c68b6-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="c68b6-114">**\_ \_ \_ adresse locale IP de condition FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="c68b6-115">Adresse locale appropriée (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="c68b6-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="c68b6-116">**\_ \_ \_ adresse distante IP de la condition FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="c68b6-117">Adresse distante appropriée (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="c68b6-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="c68b6-118">**action. type**</span><span class="sxs-lookup"><span data-stu-id="c68b6-118">**action.type**</span></span>                                                   | <span data-ttu-id="c68b6-119">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="c68b6-120">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="c68b6-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="c68b6-121">**FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="c68b6-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="c68b6-122">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c68b6-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="c68b6-123">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="c68b6-123">Filter property</span></span>                                                   | <span data-ttu-id="c68b6-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c68b6-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c68b6-125">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="c68b6-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c68b6-126">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c68b6-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="c68b6-127">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="c68b6-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="c68b6-128">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="c68b6-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="c68b6-129">**action. type**</span><span class="sxs-lookup"><span data-stu-id="c68b6-129">**action.type**</span></span>                                                   | <span data-ttu-id="c68b6-130">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="c68b6-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="c68b6-131">**weight**</span></span>                                                        | [<span data-ttu-id="c68b6-132">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="c68b6-133">**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**</span><span class="sxs-lookup"><span data-stu-id="c68b6-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="c68b6-134">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c68b6-134">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="c68b6-135">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="c68b6-135">Filter property</span></span>                                                   | <span data-ttu-id="c68b6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c68b6-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="c68b6-137">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="c68b6-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c68b6-138">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c68b6-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="c68b6-139">**FWPM \_ Condition de filtrage d' \_ \_ \_ adresse locale de condition IP**</span><span class="sxs-lookup"><span data-stu-id="c68b6-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="c68b6-140">Adresse locale appropriée (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="c68b6-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="c68b6-141">**FWPM \_ Condition de filtrage d' \_ \_ \_ adresse distante IP de condition**</span><span class="sxs-lookup"><span data-stu-id="c68b6-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="c68b6-142">Adresse distante appropriée (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="c68b6-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="c68b6-143">**action. type**</span><span class="sxs-lookup"><span data-stu-id="c68b6-143">**action.type**</span></span>                                                   | <span data-ttu-id="c68b6-144">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="c68b6-145">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="c68b6-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="c68b6-146">**FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="c68b6-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="c68b6-147">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c68b6-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="c68b6-148">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="c68b6-148">Filter property</span></span>                                                   | <span data-ttu-id="c68b6-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="c68b6-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c68b6-150">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="c68b6-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c68b6-151">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c68b6-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="c68b6-152">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="c68b6-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="c68b6-153">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="c68b6-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="c68b6-154">**action. type**</span><span class="sxs-lookup"><span data-stu-id="c68b6-154">**action.type**</span></span>                                                   | <span data-ttu-id="c68b6-155">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="c68b6-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="c68b6-156">**weight**</span></span>                                                        | <span data-ttu-id="c68b6-157">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c68b6-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="c68b6-158">**Configurer des associations de sécurité entrantes et sortantes**</span><span class="sxs-lookup"><span data-stu-id="c68b6-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="c68b6-159">Appelez [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)avec le paramètre *outboundTraffic* contenant les adresses IP sous la forme 1.1.1.1 & 2.2.2.2 et **ipsecFilterId** comme LUID du filtre de la légende IPSec de la couche de transport sortant ajoutée ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c68b6-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="c68b6-160">Appelez [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), avec le paramètre *ID* contenant l’ID de contexte renvoyé par [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), et le paramètre *getSpi* contenant les adresses IP sous la forme 1.1.1.1 & 2.2.2.2 et **ipsecFilterId** comme LUID du filtre de la légende IPSec de la couche transport entrante ajoutée ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c68b6-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="c68b6-161">La valeur SPI renvoyée est destinée à être utilisée comme le SPI entrant de l’administrateur système par l’ordinateur local et comme le SPI sortant de l’administrateur système par la machine distante correspondante.</span><span class="sxs-lookup"><span data-stu-id="c68b6-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="c68b6-162">Les deux ordinateurs doivent utiliser des moyens hors bande pour échanger les valeurs SPI.</span><span class="sxs-lookup"><span data-stu-id="c68b6-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="c68b6-163">Appelez [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), avec le paramètre *ID* contenant l’ID de contexte renvoyé par [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), et le paramètre *inboundBundle* décrivant les propriétés du bundle de l’Association de sécurité entrante (par exemple, le SPI entrant sa, le type de transformation, les types d’algorithmes, les clés, etc.).</span><span class="sxs-lookup"><span data-stu-id="c68b6-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="c68b6-164">Appelez [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), avec le paramètre *ID* contenant l’ID de contexte renvoyé par [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), et le paramètre *outboundBundle* décrivant les propriétés du bundle de la sa sortante (par exemple, le SPI sortant sa, le type de transformation, les types d’algorithmes, les clés, etc.).</span><span class="sxs-lookup"><span data-stu-id="c68b6-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="c68b6-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c68b6-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68b6-166">Exemple de code : génération manuelle de la clé SA</span><span class="sxs-lookup"><span data-stu-id="c68b6-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="c68b6-167">**Identificateurs de légende intégrés**</span><span class="sxs-lookup"><span data-stu-id="c68b6-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="c68b6-168">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="c68b6-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="c68b6-169">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="c68b6-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

