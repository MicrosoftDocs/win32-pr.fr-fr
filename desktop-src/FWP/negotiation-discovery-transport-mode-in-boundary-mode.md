---
title: Mode de transport de la découverte de négociation en mode limite
description: Le mode de transport de la découverte de négociation dans le scénario de stratégie IPsec en mode limite demande la protection du mode de transport IPsec pour tout le trafic correspondant.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9869be61923bff1c392c5abe2bd98099a0c3c89f
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314592"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a><span data-ttu-id="316b9-103">Mode de transport de la découverte de négociation en mode limite</span><span class="sxs-lookup"><span data-stu-id="316b9-103">Negotiation Discovery Transport Mode in Boundary Mode</span></span>

<span data-ttu-id="316b9-104">Le mode de transport de la découverte de négociation dans le scénario de stratégie IPsec en mode limite demande la protection du mode de transport IPsec pour tout le trafic correspondant.</span><span class="sxs-lookup"><span data-stu-id="316b9-104">The Negotiation Discovery Transport Mode in Boundary Mode IPsec policy scenario requests IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="316b9-105">Si la négociation IKE/AuthIP échoue, les connexions entrantes et sortantes sont autorisées à revenir en texte clair.</span><span class="sxs-lookup"><span data-stu-id="316b9-105">If the IKE/AuthIP negotiation fails, both inbound and outbound connections are allowed to fallback to clear-text .</span></span>

<span data-ttu-id="316b9-106">Cette stratégie IPsec est généralement utilisée sur les ordinateurs qui sont accessibles à la fois par les ordinateurs prenant en charge IPsec et non-IPsec.</span><span class="sxs-lookup"><span data-stu-id="316b9-106">This IPsec policy is typically used on machines that are accessed by both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="316b9-107">Un exemple de scénario potentiel de mode de transport de la découverte de négociation consiste à sécuriser tout le trafic de données de monodiffusion, sauf ICMP, à l’aide du mode de transport IPsec et à activer la détection de négociation en mode limite.</span><span class="sxs-lookup"><span data-stu-id="316b9-107">An example of a potential Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode and enable negotiation discovery in boundary mode."</span></span>

<span data-ttu-id="316b9-108">Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.</span><span class="sxs-lookup"><span data-stu-id="316b9-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="316b9-109">**Stratégie de négociation de l’installation de la \_ couche FWPM \_ IKEEXT \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="316b9-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="316b9-110">Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="316b9-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="316b9-111">Pour IKE, contexte d’un fournisseur de stratégie de type FWPM \_ IPSec \_ IKE \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="316b9-111">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="316b9-112">Pour AuthIP, contexte du fournisseur de stratégie de type FWPM \_ IPSec \_ AuthIP \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="316b9-112">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="316b9-113">Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="316b9-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="316b9-114">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="316b9-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="316b9-115">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="316b9-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="316b9-116">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="316b9-116">Filter property</span></span>        | <span data-ttu-id="316b9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="316b9-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="316b9-118">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="316b9-118">Filtering conditions</span></span>   | <span data-ttu-id="316b9-119">Vide.</span><span class="sxs-lookup"><span data-stu-id="316b9-119">Empty.</span></span> <span data-ttu-id="316b9-120">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="316b9-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="316b9-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="316b9-121">**providerContextKey**</span></span> | <span data-ttu-id="316b9-122">GUID du contexte du fournisseur MM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="316b9-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="316b9-123">**Au niveau de FWPM \_ Layer \_ IPSec \_ V {4 \| 6} Setup QM et em Negotiation Policy**</span><span class="sxs-lookup"><span data-stu-id="316b9-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="316b9-124">Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux, et définissez l’indicateur de [**\_ \_ \_ \_ limite ND de l’indicateur de stratégie IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="316b9-124">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_BOUNDARY**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="316b9-125">Pour IKE, contexte du fournisseur de stratégie de type **FWPM le \_ \_ \_ \_ \_ contexte de transport QM IPsec IKE**.</span><span class="sxs-lookup"><span data-stu-id="316b9-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="316b9-126">Pour AuthIP, contexte du fournisseur de stratégie de **type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="316b9-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="316b9-127">Ce contexte peut éventuellement contenir la stratégie de négociation en mode étendu AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="316b9-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="316b9-128">Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="316b9-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="316b9-129">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="316b9-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="316b9-130">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="316b9-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="316b9-131">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="316b9-131">Filter property</span></span>        | <span data-ttu-id="316b9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="316b9-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="316b9-133">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="316b9-133">Filtering conditions</span></span>   | <span data-ttu-id="316b9-134">Vide.</span><span class="sxs-lookup"><span data-stu-id="316b9-134">Empty.</span></span> <span data-ttu-id="316b9-135">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="316b9-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="316b9-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="316b9-136">**providerContextKey**</span></span> | <span data-ttu-id="316b9-137">GUID du contexte du fournisseur QM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="316b9-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="316b9-138">**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**</span><span class="sxs-lookup"><span data-stu-id="316b9-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="316b9-139">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="316b9-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="316b9-140">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="316b9-140">Filter property</span></span>                                                   | <span data-ttu-id="316b9-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="316b9-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="316b9-142">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="316b9-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="316b9-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="316b9-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="316b9-144">**action. type**</span><span class="sxs-lookup"><span data-stu-id="316b9-144">**action.type**</span></span>                                                   | <span data-ttu-id="316b9-145">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="316b9-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="316b9-146">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="316b9-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="316b9-147">**FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="316b9-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="316b9-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="316b9-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="316b9-149">**\_sécurité de \_ \_ connexion entrante IPSec de \_ \_ contexte FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="316b9-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="316b9-150">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="316b9-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="316b9-151">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="316b9-151">Filter property</span></span>                                                   | <span data-ttu-id="316b9-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="316b9-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="316b9-153">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="316b9-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="316b9-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="316b9-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="316b9-155">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="316b9-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="316b9-156">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="316b9-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="316b9-157">**action. type**</span><span class="sxs-lookup"><span data-stu-id="316b9-157">**action.type**</span></span>                                                   | <span data-ttu-id="316b9-158">\_autorisation d’action fwp \_</span><span class="sxs-lookup"><span data-stu-id="316b9-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="316b9-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="316b9-159">**weight**</span></span>                                                        | [<span data-ttu-id="316b9-160">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="316b9-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="316b9-161">**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**</span><span class="sxs-lookup"><span data-stu-id="316b9-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="316b9-162">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="316b9-162">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="316b9-163">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="316b9-163">Filter property</span></span>                                                   | <span data-ttu-id="316b9-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="316b9-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="316b9-165">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="316b9-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="316b9-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="316b9-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="316b9-167">**action. type**</span><span class="sxs-lookup"><span data-stu-id="316b9-167">**action.type**</span></span>                                                   | <span data-ttu-id="316b9-168">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="316b9-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="316b9-169">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="316b9-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="316b9-170">**FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="316b9-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="316b9-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="316b9-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="316b9-172">**\_détection de \_ \_ négociation sortante \_ IPSec \_ du contexte FWPM**</span><span class="sxs-lookup"><span data-stu-id="316b9-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="316b9-173">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="316b9-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="316b9-174">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="316b9-174">Filter property</span></span>                                                   | <span data-ttu-id="316b9-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="316b9-175">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="316b9-176">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="316b9-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="316b9-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="316b9-177">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="316b9-178">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="316b9-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="316b9-179">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="316b9-179">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="316b9-180">**action. type**</span><span class="sxs-lookup"><span data-stu-id="316b9-180">**action.type**</span></span>                                                   | <span data-ttu-id="316b9-181">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="316b9-181">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="316b9-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="316b9-182">**weight**</span></span>                                                        | <span data-ttu-id="316b9-183">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="316b9-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

> [!Note]  
> <span data-ttu-id="316b9-184">Par opposition au mode de transport de la découverte de négociation, pour le mode de transport de la découverte de négociation en mode de limite, il n’est pas nécessaire d’ajouter un filtre aux couches **FWPM d' \_ authentification ALE de la couche \_ ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}** car cette stratégie autorise les connexions entrantes non protégées en texte clair.</span><span class="sxs-lookup"><span data-stu-id="316b9-184">As opposed to Negotiation Discovery Transport Mode, for Negotiation Discovery Transport Mode in Boundary Mode policy there is no need to add a filter at the **FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}** layers because this policy allows inbound unprotected clear-text connections.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="316b9-185">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="316b9-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="316b9-186">Exemple de code : utilisation du mode de transport</span><span class="sxs-lookup"><span data-stu-id="316b9-186">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="316b9-187">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="316b9-187">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="316b9-188">**Identificateurs de légende intégrés**</span><span class="sxs-lookup"><span data-stu-id="316b9-188">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="316b9-189">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="316b9-189">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="316b9-190">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="316b9-190">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="316b9-191">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="316b9-191">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="316b9-192">**\_type de \_ contexte du fournisseur FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="316b9-192">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

