---
title: mode de transport
description: Le scénario de stratégie IPsec en mode de transport requiert la protection du mode de transport IPsec pour tout le trafic correspondant.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8335854c80850e44b860530bbebab05aa3f14273
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314932"
---
# <a name="transport-mode"></a><span data-ttu-id="5ce0e-103">mode de transport</span><span class="sxs-lookup"><span data-stu-id="5ce0e-103">Transport Mode</span></span>

<span data-ttu-id="5ce0e-104">Le scénario de stratégie IPsec en mode de transport requiert la protection du mode de transport IPsec pour tout le trafic correspondant.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-104">The Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="5ce0e-105">Tout trafic en texte clair correspondant est supprimé jusqu’à ce que la négociation IKE ou AuthIP s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-105">Any matching clear text traffic is dropped until the IKE or AuthIP negotiation has completed successfully.</span></span> <span data-ttu-id="5ce0e-106">Si la négociation échoue, la connectivité avec l’adresse IP correspondante reste ininterrompue.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-106">If the negotiation fails, connectivity with the corresponding IP address will remain broken.</span></span>

<span data-ttu-id="5ce0e-107">Un exemple de scénario de mode de transport possible est « sécuriser tout le trafic de données monodiffusion, sauf ICMP, à l’aide du mode de transport IPsec ».</span><span class="sxs-lookup"><span data-stu-id="5ce0e-107">An example of a possible Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode."</span></span>

<span data-ttu-id="5ce0e-108">Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="5ce0e-109">**Stratégie de négociation de l’installation de la \_ couche FWPM \_ IKEEXT \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="5ce0e-110">Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="5ce0e-111">Pour IKE, contexte d’un fournisseur de stratégie de type **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-111">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="5ce0e-112">Pour AuthIP, contexte du fournisseur de stratégie de type **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-112">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="5ce0e-113">Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="5ce0e-114">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="5ce0e-115">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="5ce0e-116">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-116">Filter property</span></span>        | <span data-ttu-id="5ce0e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ce0e-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="5ce0e-118">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="5ce0e-118">Filtering conditions</span></span>   | <span data-ttu-id="5ce0e-119">Vide.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-119">Empty.</span></span> <span data-ttu-id="5ce0e-120">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="5ce0e-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-121">**providerContextKey**</span></span> | <span data-ttu-id="5ce0e-122">GUID du contexte du fournisseur MM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="5ce0e-123">**Au niveau de FWPM \_ Layer \_ IPSec \_ V {4 \| 6} Setup QM et em Negotiation Policy**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="5ce0e-124">Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-124">Add one or both of the following QM transport mode policy provider contexts.</span></span>  
    -   <span data-ttu-id="5ce0e-125">Pour IKE, contexte du fournisseur de stratégie de type **FWPM le \_ \_ \_ \_ \_ contexte de transport QM IPsec IKE**.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="5ce0e-126">Pour AuthIP, contexte du fournisseur de stratégie de **type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="5ce0e-127">Ce contexte peut éventuellement contenir la stratégie de négociation en mode étendu AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="5ce0e-128">Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="5ce0e-129">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="5ce0e-130">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="5ce0e-131">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-131">Filter property</span></span>        | <span data-ttu-id="5ce0e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ce0e-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="5ce0e-133">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="5ce0e-133">Filtering conditions</span></span>   | <span data-ttu-id="5ce0e-134">Vide.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-134">Empty.</span></span> <span data-ttu-id="5ce0e-135">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="5ce0e-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-136">**providerContextKey**</span></span> | <span data-ttu-id="5ce0e-137">GUID du contexte du fournisseur QM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="5ce0e-138">**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="5ce0e-139">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="5ce0e-140">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-140">Filter property</span></span>                                                   | <span data-ttu-id="5ce0e-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ce0e-141">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="5ce0e-142">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="5ce0e-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5ce0e-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="5ce0e-144">**action. type**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-144">**action.type**</span></span>                                                   | <span data-ttu-id="5ce0e-145">fin de l’appel à l' \_ action fwp \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ce0e-145">FWP\_ACTION\_CALLOUT\_TERMINATING</span></span>                             |
    | <span data-ttu-id="5ce0e-146">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5ce0e-147">FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5ce0e-147">FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>             |

        
2.  <span data-ttu-id="5ce0e-148">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-148">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="5ce0e-149">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-149">Filter property</span></span>                                                  | <span data-ttu-id="5ce0e-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ce0e-150">Value</span></span>                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | <span data-ttu-id="5ce0e-151">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-151">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5ce0e-152">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5ce0e-152">NlatUnicast</span></span>                                                               |
    | <span data-ttu-id="5ce0e-153">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-153">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>            | <span data-ttu-id="5ce0e-154">IPPROTO \_ ICMP {V6} ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-154">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/>    |
    | <span data-ttu-id="5ce0e-155">**action. type**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-155">**action.type**</span></span>                                                  | <span data-ttu-id="5ce0e-156">\_autorisation d’action fwp \_</span><span class="sxs-lookup"><span data-stu-id="5ce0e-156">FWP\_ACTION\_PERMIT</span></span>                                                       |
    | <span data-ttu-id="5ce0e-157">**weight**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-157">**weight**</span></span>                                                       | [<span data-ttu-id="5ce0e-158">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-158">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md) |

        

<span data-ttu-id="5ce0e-159">**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-159">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="5ce0e-160">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-160">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="5ce0e-161">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-161">Filter property</span></span>                                                   | <span data-ttu-id="5ce0e-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ce0e-162">Value</span></span>                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | <span data-ttu-id="5ce0e-163">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-163">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5ce0e-164">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5ce0e-164">NlatUnicast</span></span>                                        |
    | <span data-ttu-id="5ce0e-165">**action. type**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-165">**action.type**</span></span>                                                   | <span data-ttu-id="5ce0e-166">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-166">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>              |
    | <span data-ttu-id="5ce0e-167">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-167">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5ce0e-168">FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5ce0e-168">FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span> |

        
2.  <span data-ttu-id="5ce0e-169">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-169">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="5ce0e-170">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-170">Filter property</span></span>                                                   | <span data-ttu-id="5ce0e-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ce0e-171">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="5ce0e-172">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-172">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5ce0e-173">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5ce0e-173">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="5ce0e-174">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-174">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5ce0e-175">IPPROTO \_ ICMP {V6} ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-175">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="5ce0e-176">**action. type**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-176">**action.type**</span></span>                                                   | <span data-ttu-id="5ce0e-177">\_autorisation d’action fwp \_</span><span class="sxs-lookup"><span data-stu-id="5ce0e-177">FWP\_ACTION\_PERMIT</span></span>                                                    |
    | <span data-ttu-id="5ce0e-178">**weight**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-178">**weight**</span></span>                                                        | <span data-ttu-id="5ce0e-179">\_ \_ \_ exemptions IKE de la plage de poids FWPM \_</span><span class="sxs-lookup"><span data-stu-id="5ce0e-179">FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="5ce0e-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ce0e-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce0e-181">Exemple de code : utilisation du mode de transport</span><span class="sxs-lookup"><span data-stu-id="5ce0e-181">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="5ce0e-182">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-182">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="5ce0e-183">**Types de contexte du fournisseur**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-183">**Provider Context Types**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[<span data-ttu-id="5ce0e-184">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="5ce0e-184">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="5ce0e-185">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-185">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="5ce0e-186">**Identificateurs de légende intégrés**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-186">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> </dl>

 

