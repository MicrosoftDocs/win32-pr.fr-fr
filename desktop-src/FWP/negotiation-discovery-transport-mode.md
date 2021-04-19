---
title: Mode de transport de la découverte de négociation
description: Le scénario de stratégie IPsec de mode de transport de la découverte de négociation nécessite la protection du mode de transport IPsec pour tout le trafic entrant correspondant et demande une protection IPsec pour le trafic sortant correspondant.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216fec869eca28dc0661a37d44cce3a1fd05b80a
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314812"
---
# <a name="negotiation-discovery-transport-mode"></a><span data-ttu-id="b4452-103">Mode de transport de la découverte de négociation</span><span class="sxs-lookup"><span data-stu-id="b4452-103">Negotiation Discovery Transport Mode</span></span>

<span data-ttu-id="b4452-104">Le scénario de stratégie IPsec de mode de transport de la découverte de négociation nécessite la protection du mode de transport IPsec pour tout le trafic entrant correspondant et demande une protection IPsec pour le trafic sortant correspondant.</span><span class="sxs-lookup"><span data-stu-id="b4452-104">The Negotiation Discovery Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching inbound traffic, and requests IPsec protection for matching outbound traffic.</span></span> <span data-ttu-id="b4452-105">Par conséquent, les connexions sortantes sont autorisées à revenir en texte clair alors que les connexions entrantes ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="b4452-105">Therefore, outbound connections are allowed to fallback to clear-text while inbound connections are not.</span></span>

<span data-ttu-id="b4452-106">Avec cette stratégie, lorsque l’ordinateur hôte tente une nouvelle connexion sortante et qu’il n’existe aucune association de sécurité IPsec correspondant au trafic, l’hôte envoie simultanément les paquets en texte clair et démarre une négociation IKE ou AuthIP.</span><span class="sxs-lookup"><span data-stu-id="b4452-106">With this policy, when the host machine attempts a new outbound connection and there is no existing IPsec SA matching the traffic, the host simultaneously sends the packets in clear-text and starts an IKE or AuthIP negotiation.</span></span> <span data-ttu-id="b4452-107">Si la négociation s’effectue correctement, la connexion est mise à niveau vers protégé par IPsec.</span><span class="sxs-lookup"><span data-stu-id="b4452-107">If the negotiation succeeds, the connection is upgraded to IPsec-protected.</span></span> <span data-ttu-id="b4452-108">Dans le cas contraire, la connexion reste en texte clair.</span><span class="sxs-lookup"><span data-stu-id="b4452-108">Otherwise, the connection stays in clear-text.</span></span> <span data-ttu-id="b4452-109">Une fois qu’il est protégé par IPsec, une connexion ne peut jamais être rétrogradée en texte clair.</span><span class="sxs-lookup"><span data-stu-id="b4452-109">Once IPsec-protected, a connection can never be downgraded to clear-text.</span></span>

<span data-ttu-id="b4452-110">Le mode de transport de la découverte de négociation est généralement utilisé dans les environnements qui incluent des ordinateurs prenant en charge IPsec et non-IPsec.</span><span class="sxs-lookup"><span data-stu-id="b4452-110">Negotiation Discovery Transport Mode is typically used in environments that include both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="b4452-111">Un exemple de scénario de mode de transport de découverte de négociation possible est « sécuriser tout le trafic de données de monodiffusion, sauf ICMP, en utilisant le mode de transport IPsec et l’activation de la découverte de négociation ».</span><span class="sxs-lookup"><span data-stu-id="b4452-111">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, and enable negotiation discovery."</span></span>

<span data-ttu-id="b4452-112">Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.</span><span class="sxs-lookup"><span data-stu-id="b4452-112">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="b4452-113">**Au niveau de la couche FWPM, \_ \_ IKEEXT \_ V {4 \| 6} configurer la stratégie de négociation mm**</span><span class="sxs-lookup"><span data-stu-id="b4452-113">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} set up MM negotiation policy**</span></span>  

1.  <span data-ttu-id="b4452-114">Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b4452-114">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="b4452-115">Pour IKE, contexte d’un fournisseur de stratégie de type **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="b4452-115">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="b4452-116">Pour AuthIP, contexte du fournisseur de stratégie de type **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="b4452-116">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="b4452-117">Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="b4452-117">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="b4452-118">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4452-118">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="b4452-119">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-119">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="b4452-120">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-120">Filter property</span></span>        | <span data-ttu-id="b4452-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-121">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="b4452-122">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="b4452-122">Filtering conditions</span></span>   | <span data-ttu-id="b4452-123">Vide.</span><span class="sxs-lookup"><span data-stu-id="b4452-123">Empty.</span></span> <span data-ttu-id="b4452-124">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="b4452-124">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="b4452-125">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="b4452-125">**providerContextKey**</span></span> | <span data-ttu-id="b4452-126">GUID du contexte du fournisseur MM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="b4452-126">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="b4452-127">**Au niveau de la \_ couche FWPM \_ \_ , IPSec V {4 \| 6} configurez la stratégie de négociation QM et em**</span><span class="sxs-lookup"><span data-stu-id="b4452-127">**At FWPM\_LAYER\_IPSEC\_V{4\|6} set up QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="b4452-128">Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux, et définissez l’indicateur de sécurité de l' [**\_ indicateur de stratégie IPSec \_ \_ ND \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="b4452-128">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="b4452-129">Pour IKE, contexte du fournisseur de stratégie de type FWPM le \_ \_ contexte de \_ transport QM IPsec IKE \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b4452-129">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT.</span></span>
    -   <span data-ttu-id="b4452-130">Pour AuthIP, contexte du fournisseur de stratégie de type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context.</span><span class="sxs-lookup"><span data-stu-id="b4452-130">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT.</span></span> <span data-ttu-id="b4452-131">Ce contexte peut éventuellement contenir la stratégie de négociation en mode étendu AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="b4452-131">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="b4452-132">Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="b4452-132">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="b4452-133">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4452-133">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="b4452-134">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-134">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="b4452-135">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-135">Filter property</span></span>        | <span data-ttu-id="b4452-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-136">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="b4452-137">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="b4452-137">Filtering conditions</span></span>   | <span data-ttu-id="b4452-138">Vide.</span><span class="sxs-lookup"><span data-stu-id="b4452-138">Empty.</span></span> <span data-ttu-id="b4452-139">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="b4452-139">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="b4452-140">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="b4452-140">**providerContextKey**</span></span> | <span data-ttu-id="b4452-141">GUID du contexte du fournisseur QM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="b4452-141">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="b4452-142">**Au niveau du \_ transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet entrant**</span><span class="sxs-lookup"><span data-stu-id="b4452-142">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} set up inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="b4452-143">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-143">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="b4452-144">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-144">Filter property</span></span>                                                   | <span data-ttu-id="b4452-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-145">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b4452-146">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-146">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="b4452-147">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="b4452-147">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="b4452-148">**action. type**</span><span class="sxs-lookup"><span data-stu-id="b4452-148">**action.type**</span></span>                                                   | <span data-ttu-id="b4452-149">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-149">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="b4452-150">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="b4452-150">**action.calloutKey**</span></span>                                             | <span data-ttu-id="b4452-151">**FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b4452-151">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="b4452-152">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="b4452-152">**rawContext**</span></span>                                                    | [<span data-ttu-id="b4452-153">**\_sécurité de \_ \_ connexion entrante IPSec de \_ \_ contexte FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-153">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="b4452-154">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-154">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="b4452-155">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-155">Filter property</span></span>                                                   | <span data-ttu-id="b4452-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-156">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b4452-157">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-157">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b4452-158">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="b4452-158">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="b4452-159">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-159">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b4452-160">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="b4452-160">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="b4452-161">**action. type**</span><span class="sxs-lookup"><span data-stu-id="b4452-161">**action.type**</span></span>                                                   | <span data-ttu-id="b4452-162">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-162">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="b4452-163">**weight**</span><span class="sxs-lookup"><span data-stu-id="b4452-163">**weight**</span></span>                                                        | [<span data-ttu-id="b4452-164">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-164">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="b4452-165">**Au niveau du \_ transport sortant de la couche FWPM \_ \_ \_ V {4 \| 6} configurer les règles de filtrage par paquets sortants**</span><span class="sxs-lookup"><span data-stu-id="b4452-165">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} set up outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="b4452-166">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-166">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="b4452-167">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-167">Filter property</span></span>                                                   | <span data-ttu-id="b4452-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-168">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b4452-169">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-169">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b4452-170">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="b4452-170">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="b4452-171">**action. type**</span><span class="sxs-lookup"><span data-stu-id="b4452-171">**action.type**</span></span>                                                   | <span data-ttu-id="b4452-172">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-172">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="b4452-173">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="b4452-173">**action.calloutKey**</span></span>                                             | <span data-ttu-id="b4452-174">**FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b4452-174">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="b4452-175">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="b4452-175">**rawContext**</span></span>                                                    | [<span data-ttu-id="b4452-176">**\_détection de \_ \_ négociation sortante \_ IPSec \_ du contexte FWPM**</span><span class="sxs-lookup"><span data-stu-id="b4452-176">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="b4452-177">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-177">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="b4452-178">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-178">Filter property</span></span>                                                   | <span data-ttu-id="b4452-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-179">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b4452-180">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-180">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b4452-181">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="b4452-181">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="b4452-182">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-182">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b4452-183">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="b4452-183">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="b4452-184">**action. type**</span><span class="sxs-lookup"><span data-stu-id="b4452-184">**action.type**</span></span>                                                   | <span data-ttu-id="b4452-185">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-185">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="b4452-186">**weight**</span><span class="sxs-lookup"><span data-stu-id="b4452-186">**weight**</span></span>                                                        | <span data-ttu-id="b4452-187">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-187">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="b4452-188">**Au niveau de FWPM \_ couche \_ ALE \_ auth \_ recv \_ Accept \_ V {4 \| 6} configurer les règles de filtrage par connexion entrantes**</span><span class="sxs-lookup"><span data-stu-id="b4452-188">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} set up inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="b4452-189">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-189">Add a filter with the following properties.</span></span> <span data-ttu-id="b4452-190">Ce filtre n’autorise que les tentatives de connexion entrante s’ils sont sécurisés par IPsec.</span><span class="sxs-lookup"><span data-stu-id="b4452-190">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="b4452-191">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-191">Filter property</span></span>                                                   | <span data-ttu-id="b4452-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-192">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="b4452-193">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-193">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b4452-194">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="b4452-194">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="b4452-195">**action. type**</span><span class="sxs-lookup"><span data-stu-id="b4452-195">**action.type**</span></span>                                                   | <span data-ttu-id="b4452-196">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-196">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="b4452-197">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="b4452-197">**action.calloutKey**</span></span>                                             | <span data-ttu-id="b4452-198">**\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="b4452-198">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="b4452-199">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4452-199">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="b4452-200">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="b4452-200">Filter property</span></span>                                                   | <span data-ttu-id="b4452-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4452-201">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b4452-202">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-202">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="b4452-203">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="b4452-203">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="b4452-204">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="b4452-204">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="b4452-205">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="b4452-205">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="b4452-206">**action. type**</span><span class="sxs-lookup"><span data-stu-id="b4452-206">**action.type**</span></span>                                                   | <span data-ttu-id="b4452-207">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-207">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="b4452-208">**weight**</span><span class="sxs-lookup"><span data-stu-id="b4452-208">**weight**</span></span>                                                        | <span data-ttu-id="b4452-209">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-209">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="b4452-210">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4452-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4452-211">Exemple de code : utilisation du mode de transport</span><span class="sxs-lookup"><span data-stu-id="b4452-211">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="b4452-212">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="b4452-212">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="b4452-213">**Identificateurs de légende intégrés**</span><span class="sxs-lookup"><span data-stu-id="b4452-213">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="b4452-214">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="b4452-214">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="b4452-215">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="b4452-215">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="b4452-216">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="b4452-216">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="b4452-217">**\_type de \_ contexte du fournisseur FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="b4452-217">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

