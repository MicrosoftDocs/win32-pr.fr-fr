---
title: Autorisation d’identité distante
description: Le scénario de la stratégie IPsec d’autorisation d’identité distante requiert que les connexions entrantes proviennent d’un ensemble spécifique de principaux de sécurité distants qui sont spécifiés dans une liste de contrôle d’accès (ACL) du descripteur de sécurité Windows.
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57287a0dd9af4686b1a2dab162677912213559a7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314832"
---
# <a name="remote-identity-authorization"></a><span data-ttu-id="a6121-103">Autorisation d’identité distante</span><span class="sxs-lookup"><span data-stu-id="a6121-103">Remote Identity Authorization</span></span>

<span data-ttu-id="a6121-104">Le scénario de la stratégie IPsec d’autorisation d’identité distante requiert que les connexions entrantes proviennent d’un ensemble spécifique de principaux de sécurité distants qui sont spécifiés dans une liste de contrôle d’accès (ACL) du descripteur de sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="a6121-104">The Remote Identity Authorization IPsec policy scenario requires that inbound connections come from a specific set of remote security principals which are specified in a Windows security descriptor (SD) access control list (ACL).</span></span> <span data-ttu-id="a6121-105">Si l’identité distante (telle que déterminée par IPsec) ne correspond pas à l’ensemble d’identités autorisées, la connexion est supprimée.</span><span class="sxs-lookup"><span data-stu-id="a6121-105">If the remote identity (as determined by IPsec) does not match the set of allowed identities, the connection will be dropped.</span></span> <span data-ttu-id="a6121-106">Cette stratégie doit être spécifiée conjointement avec l’une des options de la stratégie mode de transport.</span><span class="sxs-lookup"><span data-stu-id="a6121-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="a6121-107">Si AuthIP est activé, il est possible de spécifier deux descripteurs de sécurité, l’un correspondant au mode principal AuthIP et l’autre correspondant au mode étendu AuthIP.</span><span class="sxs-lookup"><span data-stu-id="a6121-107">If AuthIP is enabled, two security descriptors can be specified, one corresponding to AuthIP main mode, and the other corresponding to AuthIP extended mode.</span></span>

<span data-ttu-id="a6121-108">Un exemple de scénario de mode de transport de découverte de négociation est le suivant : «sécuriser tout le trafic de données de monodiffusion, sauf ICMP, à l’aide du mode de transport IPsec, activer la découverte de négociation et limiter l’accès entrant aux identités distantes autorisées en tant que descripteur de sécurité SD1 (correspondant au 5555 mode principal d’IKE</span><span class="sxs-lookup"><span data-stu-id="a6121-108">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and restrict inbound access to remote identities allowed as per security descriptor SD1 (corresponding to IKE/AuthIP main mode) and security descriptor SD2 (corresponding to AuthIP extended mode), for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="a6121-109">Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.</span><span class="sxs-lookup"><span data-stu-id="a6121-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="a6121-110">**Stratégie de négociation de l’installation de la \_ couche FWPM \_ IKEEXT \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a6121-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="a6121-111">Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="a6121-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="a6121-112">Pour IKE, contexte d’un fournisseur de stratégie de type **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="a6121-112">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="a6121-113">Pour AuthIP, contexte du fournisseur de stratégie de type **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="a6121-113">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="a6121-114">Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="a6121-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="a6121-115">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a6121-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="a6121-116">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="a6121-117">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-117">Filter property</span></span>        | <span data-ttu-id="a6121-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="a6121-119">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="a6121-119">Filtering conditions</span></span>   | <span data-ttu-id="a6121-120">Vide.</span><span class="sxs-lookup"><span data-stu-id="a6121-120">Empty.</span></span> <span data-ttu-id="a6121-121">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="a6121-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="a6121-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="a6121-122">**providerContextKey**</span></span> | <span data-ttu-id="a6121-123">GUID du contexte du fournisseur MM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="a6121-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="a6121-124">**Au niveau de FWPM \_ Layer \_ IPSec \_ V {4 \| 6} Setup QM et em Negotiation Policy**</span><span class="sxs-lookup"><span data-stu-id="a6121-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="a6121-125">Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux, et définissez l’indicateur de sécurité de l' [**\_ indicateur de stratégie IPSec \_ \_ ND \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="a6121-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="a6121-126">Pour IKE, contexte du fournisseur de stratégie de type **FWPM le \_ \_ \_ \_ \_ contexte de transport QM IPsec IKE**.</span><span class="sxs-lookup"><span data-stu-id="a6121-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="a6121-127">Pour AuthIP, contexte du fournisseur de stratégie de **type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context** qui contient la stratégie de négociation en mode étendu AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="a6121-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT** that contains the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="a6121-128">Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="a6121-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="a6121-129">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a6121-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="a6121-130">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="a6121-131">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-131">Filter property</span></span>        | <span data-ttu-id="a6121-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="a6121-133">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="a6121-133">Filtering conditions</span></span>   | <span data-ttu-id="a6121-134">Vide.</span><span class="sxs-lookup"><span data-stu-id="a6121-134">Empty.</span></span> <span data-ttu-id="a6121-135">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="a6121-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="a6121-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="a6121-136">**providerContextKey**</span></span> | <span data-ttu-id="a6121-137">GUID du contexte du fournisseur QM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="a6121-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="a6121-138">**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**</span><span class="sxs-lookup"><span data-stu-id="a6121-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="a6121-139">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="a6121-140">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-140">Filter property</span></span>                                                   | <span data-ttu-id="a6121-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a6121-142">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="a6121-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="a6121-144">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-144">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-145">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="a6121-146">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="a6121-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a6121-147">**FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a6121-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="a6121-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="a6121-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="a6121-149">**\_sécurité de \_ \_ connexion entrante IPSec de \_ \_ contexte FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="a6121-150">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="a6121-151">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-151">Filter property</span></span>                                                   | <span data-ttu-id="a6121-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="a6121-153">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a6121-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="a6121-155">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a6121-156">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="a6121-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a6121-157">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-157">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-158">\_autorisation d’action fwp \_</span><span class="sxs-lookup"><span data-stu-id="a6121-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="a6121-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="a6121-159">**weight**</span></span>                                                        | [<span data-ttu-id="a6121-160">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="a6121-161">**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**</span><span class="sxs-lookup"><span data-stu-id="a6121-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="a6121-162">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-162">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="a6121-163">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-163">Filter property</span></span>                                                   | <span data-ttu-id="a6121-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a6121-165">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a6121-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="a6121-167">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-167">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-168">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="a6121-169">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="a6121-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a6121-170">**FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a6121-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="a6121-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="a6121-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="a6121-172">**\_détection de \_ \_ négociation sortante \_ IPSec \_ du contexte FWPM**</span><span class="sxs-lookup"><span data-stu-id="a6121-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="a6121-173">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="a6121-174">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-174">Filter property</span></span>                                                   | <span data-ttu-id="a6121-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-175">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="a6121-176">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a6121-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-177">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="a6121-178">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a6121-179">IPPROTO \_ ICMP {V6} ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="a6121-179">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a6121-180">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-180">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-181">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-181">**FWP\_ACTION\_PERMIT**</span></span>                                                |
    | <span data-ttu-id="a6121-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="a6121-182">**weight**</span></span>                                                        | <span data-ttu-id="a6121-183">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                               |

        

<span data-ttu-id="a6121-184">**Au niveau de FWPM \_ \_ , l’authentification ALE de la couche ALE \_ \_ recv \_ accepte \_ \| les règles de filtrage par connexion entrantes V {4 6}**</span><span class="sxs-lookup"><span data-stu-id="a6121-184">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="a6121-185">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-185">Add a filter with the following properties.</span></span> <span data-ttu-id="a6121-186">Ce filtre n’autorise que les tentatives de connexion entrante s’ils sont sécurisés par IPsec.</span><span class="sxs-lookup"><span data-stu-id="a6121-186">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="a6121-187">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-187">Filter property</span></span>                                                   | <span data-ttu-id="a6121-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-188">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="a6121-189">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-189">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a6121-190">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-190">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="a6121-191">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-191">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-192">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-192">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="a6121-193">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="a6121-193">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a6121-194">**\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a6121-194">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="a6121-195">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-195">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="a6121-196">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-196">Filter property</span></span>                                                   | <span data-ttu-id="a6121-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-197">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="a6121-198">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-198">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a6121-199">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-199">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="a6121-200">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-200">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a6121-201">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="a6121-201">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a6121-202">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-202">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-203">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-203">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="a6121-204">**weight**</span><span class="sxs-lookup"><span data-stu-id="a6121-204">**weight**</span></span>                                                        | <span data-ttu-id="a6121-205">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-205">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="a6121-206">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-206">Add a filter with the following properties.</span></span> <span data-ttu-id="a6121-207">Ce filtre autorise les connexions entrantes vers le port TCP 5555 si les identités distantes correspondantes sont autorisées par SD1 et SD2.</span><span class="sxs-lookup"><span data-stu-id="a6121-207">This filter will permit inbound connections to TCP port 5555 if the corresponding remote identities are allowed by both SD1 and SD2.</span></span> 

    | <span data-ttu-id="a6121-208">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-208">Filter property</span></span>                                                   | <span data-ttu-id="a6121-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-209">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="a6121-210">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-210">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a6121-211">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-211">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="a6121-212">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-212">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a6121-213">**IPPROTO \_ TCP** cette constante est définie dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="a6121-213">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a6121-214">**FWPM \_ Condition de filtrage de \_ \_ \_ port local IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-214">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="a6121-215">5555</span><span class="sxs-lookup"><span data-stu-id="a6121-215">5555</span></span>                                                               |
    | <span data-ttu-id="a6121-216">**\_ID de \_ \_ machine distante ALE \_ de condition \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="a6121-216">**FWPM\_CONDITION\_ALE\_REMOTE\_MACHINE\_ID**</span></span>                     | <span data-ttu-id="a6121-217">SD1</span><span class="sxs-lookup"><span data-stu-id="a6121-217">SD1</span></span>                                                                |
    | <span data-ttu-id="a6121-218">**\_ID d' \_ \_ utilisateur distant \_ ALE \_ de condition FWPM**</span><span class="sxs-lookup"><span data-stu-id="a6121-218">**FWPM\_CONDITION\_ALE\_REMOTE\_USER\_ID**</span></span>                        | <span data-ttu-id="a6121-219">SD2</span><span class="sxs-lookup"><span data-stu-id="a6121-219">SD2</span></span>                                                                |
    | <span data-ttu-id="a6121-220">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-220">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-221">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-221">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                              |
    | <span data-ttu-id="a6121-222">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="a6121-222">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a6121-223">**\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="a6121-223">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>       |

        
4.  <span data-ttu-id="a6121-224">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6121-224">Add a filter with the following properties.</span></span> <span data-ttu-id="a6121-225">Ce filtre bloque toutes les autres connexions entrantes vers le port TCP 5555 qui ne correspondait pas au filtre précédent.</span><span class="sxs-lookup"><span data-stu-id="a6121-225">This filter will block any other inbound connections to TCP port 5555 that did not match the previous filter.</span></span> 

    | <span data-ttu-id="a6121-226">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="a6121-226">Filter property</span></span>                                                   | <span data-ttu-id="a6121-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6121-227">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="a6121-228">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a6121-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a6121-229">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="a6121-230">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a6121-231">**IPPROTO \_ TCP** cette constante est définie dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="a6121-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a6121-232">**FWPM \_ Condition de filtrage de \_ \_ \_ port local IP de condition**</span><span class="sxs-lookup"><span data-stu-id="a6121-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="a6121-233">5555</span><span class="sxs-lookup"><span data-stu-id="a6121-233">5555</span></span>                                                               |
    | <span data-ttu-id="a6121-234">**action. type**</span><span class="sxs-lookup"><span data-stu-id="a6121-234">**action.type**</span></span>                                                   | <span data-ttu-id="a6121-235">**\_bloc d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-235">**FWP\_ACTION\_BLOCK**</span></span>                                             |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="a6121-236">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6121-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6121-237">Exemple de code : utilisation du mode de transport</span><span class="sxs-lookup"><span data-stu-id="a6121-237">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="a6121-238">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="a6121-238">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="a6121-239">**Identificateurs de légende intégrés**</span><span class="sxs-lookup"><span data-stu-id="a6121-239">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="a6121-240">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="a6121-240">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="a6121-241">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="a6121-241">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="a6121-242">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="a6121-242">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="a6121-243">**\_type de \_ contexte du fournisseur FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="a6121-243">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

