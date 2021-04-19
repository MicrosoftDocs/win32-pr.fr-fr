---
title: Chiffrement garanti
description: Le scénario de stratégie IPsec de chiffrement garanti requiert le chiffrement IPsec pour tout le trafic correspondant. Cette stratégie doit être spécifiée conjointement avec l’une des options de la stratégie mode de transport.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbffa3d78a9e178850f3afaa4d6b7fa9831be875
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314642"
---
# <a name="guaranteed-encryption"></a><span data-ttu-id="25b96-104">Chiffrement garanti</span><span class="sxs-lookup"><span data-stu-id="25b96-104">Guaranteed Encryption</span></span>

<span data-ttu-id="25b96-105">Le scénario de stratégie IPsec de chiffrement garanti requiert le chiffrement IPsec pour tout le trafic correspondant.</span><span class="sxs-lookup"><span data-stu-id="25b96-105">The Guaranteed Encryption IPsec policy scenario requires IPsec encryption for all matching traffic.</span></span> <span data-ttu-id="25b96-106">Cette stratégie doit être spécifiée conjointement avec l’une des options de la stratégie mode de transport.</span><span class="sxs-lookup"><span data-stu-id="25b96-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="25b96-107">Le chiffrement garanti est généralement utilisé pour chiffrer le trafic sensible pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="25b96-107">Guaranteed Encryption is typically used to encrypt sensitive traffic on a per application basis.</span></span>

<span data-ttu-id="25b96-108">Un exemple de scénario de chiffrement garanti est le suivant : « sécuriser tout le trafic de données monodiffusion, sauf ICMP, à l’aide du mode de transport IPsec, activer la découverte de négociation et exiger un chiffrement garanti pour tout le trafic de monodiffusion correspondant au port local TCP 5555 ».</span><span class="sxs-lookup"><span data-stu-id="25b96-108">An example of a possible Guaranteed Encryption scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and require guaranteed encryption for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="25b96-109">Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.</span><span class="sxs-lookup"><span data-stu-id="25b96-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="25b96-110">**Stratégie de négociation de l’installation de la \_ couche FWPM \_ IKEEXT \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="25b96-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="25b96-111">Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="25b96-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="25b96-112">Pour IKE, contexte d’un fournisseur de stratégie de type FWPM \_ IPSec \_ IKE \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="25b96-112">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="25b96-113">Pour AuthIP, contexte du fournisseur de stratégie de type FWPM \_ IPSec \_ AuthIP \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="25b96-113">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="25b96-114">Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="25b96-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="25b96-115">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="25b96-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="25b96-116">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="25b96-117">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-117">Filter property</span></span>        | <span data-ttu-id="25b96-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="25b96-119">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="25b96-119">Filtering conditions</span></span>   | <span data-ttu-id="25b96-120">Vide.</span><span class="sxs-lookup"><span data-stu-id="25b96-120">Empty.</span></span> <span data-ttu-id="25b96-121">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="25b96-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="25b96-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="25b96-122">**providerContextKey**</span></span> | <span data-ttu-id="25b96-123">GUID du contexte du fournisseur MM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="25b96-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="25b96-124">**Au niveau de FWPM \_ Layer \_ IPSec \_ V {4 \| 6} Setup QM et em Negotiation Policy**</span><span class="sxs-lookup"><span data-stu-id="25b96-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="25b96-125">Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux, et définissez l’indicateur de sécurité de l' [**\_ indicateur de stratégie IPSec \_ \_ ND \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="25b96-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="25b96-126">Pour IKE, contexte du fournisseur de stratégie de type **FWPM le \_ \_ \_ \_ \_ contexte de transport QM IPsec IKE**.</span><span class="sxs-lookup"><span data-stu-id="25b96-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="25b96-127">Pour AuthIP, contexte du fournisseur de stratégie de **type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="25b96-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="25b96-128">Ce contexte peut éventuellement contenir la stratégie de négociation en mode étendu AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="25b96-128">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="25b96-129">Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="25b96-129">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="25b96-130">AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="25b96-130">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="25b96-131">Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-131">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="25b96-132">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-132">Filter property</span></span>        | <span data-ttu-id="25b96-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-133">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="25b96-134">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="25b96-134">Filtering conditions</span></span>   | <span data-ttu-id="25b96-135">Vide.</span><span class="sxs-lookup"><span data-stu-id="25b96-135">Empty.</span></span> <span data-ttu-id="25b96-136">Tout le trafic correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="25b96-136">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="25b96-137">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="25b96-137">**providerContextKey**</span></span> | <span data-ttu-id="25b96-138">GUID du contexte du fournisseur QM ajouté à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="25b96-138">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="25b96-139">**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**</span><span class="sxs-lookup"><span data-stu-id="25b96-139">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="25b96-140">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-140">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="25b96-141">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-141">Filter property</span></span>                                               | <span data-ttu-id="25b96-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-142">Value</span></span>                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="25b96-143">\_Condition de \_ filtrage \_ de \_ type d’adresse locale IP de condition FWPM \_</span><span class="sxs-lookup"><span data-stu-id="25b96-143">FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE filtering condition</span></span> | [<span data-ttu-id="25b96-144">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-144">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="25b96-145">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-145">**action.type**</span></span>                                               | <span data-ttu-id="25b96-146">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-146">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="25b96-147">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="25b96-147">**action.calloutKey**</span></span>                                         | <span data-ttu-id="25b96-148">**FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="25b96-148">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="25b96-149">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="25b96-149">**rawContext**</span></span>                                                | [<span data-ttu-id="25b96-150">**\_sécurité de \_ \_ connexion entrante IPSec de \_ \_ contexte FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-150">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="25b96-151">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-151">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="25b96-152">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-152">Filter property</span></span>                                                   | <span data-ttu-id="25b96-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-153">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="25b96-154">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-154">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="25b96-155">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-155">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="25b96-156">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-156">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="25b96-157">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="25b96-157">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="25b96-158">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-158">**action.type**</span></span>                                                   | <span data-ttu-id="25b96-159">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-159">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="25b96-160">**weight**</span><span class="sxs-lookup"><span data-stu-id="25b96-160">**weight**</span></span>                                                        | [<span data-ttu-id="25b96-161">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-161">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="25b96-162">**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**</span><span class="sxs-lookup"><span data-stu-id="25b96-162">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="25b96-163">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-163">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="25b96-164">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-164">Filter property</span></span>                                                   | <span data-ttu-id="25b96-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-165">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="25b96-166">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-166">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="25b96-167">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-167">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="25b96-168">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-168">**action.type**</span></span>                                                   | <span data-ttu-id="25b96-169">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-169">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="25b96-170">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="25b96-170">**action.calloutKey**</span></span>                                             | <span data-ttu-id="25b96-171">**FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="25b96-171">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="25b96-172">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="25b96-172">**rawContext**</span></span>                                                    | [<span data-ttu-id="25b96-173">**\_détection de \_ \_ négociation sortante \_ IPSec \_ du contexte FWPM**</span><span class="sxs-lookup"><span data-stu-id="25b96-173">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="25b96-174">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-174">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="25b96-175">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-175">Filter property</span></span>                                                   | <span data-ttu-id="25b96-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-176">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="25b96-177">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-177">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="25b96-178">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-178">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="25b96-179">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-179">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="25b96-180">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="25b96-180">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="25b96-181">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-181">**action.type**</span></span>                                                   | <span data-ttu-id="25b96-182">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-182">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="25b96-183">**weight**</span><span class="sxs-lookup"><span data-stu-id="25b96-183">**weight**</span></span>                                                        | <span data-ttu-id="25b96-184">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-184">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="25b96-185">**Au niveau de FWPM \_ \_ , l’authentification ALE de la couche ALE \_ \_ recv \_ accepte \_ \| les règles de filtrage par connexion entrantes V {4 6}**</span><span class="sxs-lookup"><span data-stu-id="25b96-185">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="25b96-186">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-186">Add a filter with the following properties.</span></span> <span data-ttu-id="25b96-187">Ce filtre n’autorise que les tentatives de connexion entrante s’ils sont sécurisés par IPsec.</span><span class="sxs-lookup"><span data-stu-id="25b96-187">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="25b96-188">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-188">Filter property</span></span>                                                   | <span data-ttu-id="25b96-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-189">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="25b96-190">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-190">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="25b96-191">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-191">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="25b96-192">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-192">**action.type**</span></span>                                                   | <span data-ttu-id="25b96-193">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-193">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="25b96-194">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="25b96-194">**action.calloutKey**</span></span>                                             | <span data-ttu-id="25b96-195">**\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="25b96-195">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="25b96-196">Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-196">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="25b96-197">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-197">Filter property</span></span>                                                   | <span data-ttu-id="25b96-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-198">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="25b96-199">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-199">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="25b96-200">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-200">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="25b96-201">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-201">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="25b96-202">**IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="25b96-202">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="25b96-203">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-203">**action.type**</span></span>                                                   | <span data-ttu-id="25b96-204">**\_autorisation d’action fwp \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-204">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="25b96-205">**weight**</span><span class="sxs-lookup"><span data-stu-id="25b96-205">**weight**</span></span>                                                        | <span data-ttu-id="25b96-206">**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-206">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="25b96-207">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-207">Add a filter with the following properties.</span></span> <span data-ttu-id="25b96-208">Ce filtre autorise uniquement les connexions entrantes vers le port TCP 5555 s’ils sont chiffrés.</span><span class="sxs-lookup"><span data-stu-id="25b96-208">This filter will only permit inbound connections to TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="25b96-209">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-209">Filter property</span></span>                                                   | <span data-ttu-id="25b96-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-210">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="25b96-211">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-211">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="25b96-212">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-212">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="25b96-213">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-213">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="25b96-214">**IPPROTO \_ TCP** cette constante est définie dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="25b96-214">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="25b96-215">**FWPM \_ Condition de filtrage de \_ \_ \_ port local IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-215">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="25b96-216">5555</span><span class="sxs-lookup"><span data-stu-id="25b96-216">5555</span></span>                                                                                                  |
    | <span data-ttu-id="25b96-217">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-217">**action.type**</span></span>                                                   | <span data-ttu-id="25b96-218">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-218">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="25b96-219">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="25b96-219">**action.calloutKey**</span></span>                                             | <span data-ttu-id="25b96-220">**\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="25b96-220">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>                                          |
    | <span data-ttu-id="25b96-221">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="25b96-221">**rawContext**</span></span>                                                    | [<span data-ttu-id="25b96-222">**la \_ connexion du jeu ale du contexte FWPM \_ \_ nécessite le \_ \_ \_ \_ chiffrement IPSec**</span><span class="sxs-lookup"><span data-stu-id="25b96-222">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

        

<span data-ttu-id="25b96-223">**Au niveau de FWPM \_ couche \_ ALE \_ auth \_ Connect connexion \_ V {4 \| 6} configurer les règles de filtrage par connexion sortantes**</span><span class="sxs-lookup"><span data-stu-id="25b96-223">**At FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6} setup outbound per-connection filtering rules**</span></span>

-   <span data-ttu-id="25b96-224">Ajoutez un filtre avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25b96-224">Add a filter with the following properties.</span></span> <span data-ttu-id="25b96-225">Ce filtre autorise uniquement les connexions sortantes à partir du port TCP 5555 s’ils sont chiffrés.</span><span class="sxs-lookup"><span data-stu-id="25b96-225">This filter will only permit outbound connections from TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="25b96-226">Filter (propriété)</span><span class="sxs-lookup"><span data-stu-id="25b96-226">Filter property</span></span>                                                   | <span data-ttu-id="25b96-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b96-227">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="25b96-228">**FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="25b96-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="25b96-229">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="25b96-230">**FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="25b96-231">**IPPROTO \_ TCP** cette constante est définie dans Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="25b96-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="25b96-232">**FWPM \_ Condition de filtrage de \_ \_ \_ port local IP de condition**</span><span class="sxs-lookup"><span data-stu-id="25b96-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="25b96-233">5555</span><span class="sxs-lookup"><span data-stu-id="25b96-233">5555</span></span>                                                                                                  |
    | <span data-ttu-id="25b96-234">**action. type**</span><span class="sxs-lookup"><span data-stu-id="25b96-234">**action.type**</span></span>                                                   | <span data-ttu-id="25b96-235">**fin de l’appel à l' \_ action fwp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-235">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="25b96-236">**action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="25b96-236">**action.calloutKey**</span></span>                                             | <span data-ttu-id="25b96-237">**FWPM \_ de \_ \_ connexion ALE ALE IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="25b96-237">**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V{4\|6}**</span></span>                                                       |
    | <span data-ttu-id="25b96-238">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="25b96-238">**rawContext**</span></span>                                                    | [<span data-ttu-id="25b96-239">**la \_ connexion du jeu ale du contexte FWPM \_ \_ nécessite le \_ \_ \_ \_ chiffrement IPSec**</span><span class="sxs-lookup"><span data-stu-id="25b96-239">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="25b96-240">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="25b96-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25b96-241">Exemple de code : utilisation du mode de transport</span><span class="sxs-lookup"><span data-stu-id="25b96-241">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="25b96-242">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="25b96-242">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="25b96-243">**Identificateurs de légende intégrés**</span><span class="sxs-lookup"><span data-stu-id="25b96-243">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="25b96-244">Conditions de filtrage</span><span class="sxs-lookup"><span data-stu-id="25b96-244">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="25b96-245">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="25b96-245">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="25b96-246">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="25b96-246">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="25b96-247">**\_type de \_ contexte du fournisseur FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="25b96-247">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

