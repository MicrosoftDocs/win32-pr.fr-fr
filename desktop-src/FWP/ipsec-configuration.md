---
title: Configuration IPsec
description: La plateforme de filtrage Windows (WFP) est la plateforme sous-jacente pour le pare-feu Windows avec fonctions avancées de sécurité.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940933"
---
# <a name="ipsec-configuration"></a><span data-ttu-id="b3785-103">Configuration IPsec</span><span class="sxs-lookup"><span data-stu-id="b3785-103">IPsec Configuration</span></span>

<span data-ttu-id="b3785-104">La plateforme de filtrage Windows (WFP) est la plateforme sous-jacente pour le pare-feu Windows avec fonctions avancées de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b3785-104">Windows Filtering Platform (WFP) is the underlying platform for Windows Firewall with Advanced Security.</span></span> <span data-ttu-id="b3785-105">WFP est utilisé pour configurer les règles de filtrage réseau, qui incluent des règles qui régissent la sécurisation du trafic réseau avec IPsec.</span><span class="sxs-lookup"><span data-stu-id="b3785-105">WFP is used to configure network filtering rules, which include rules that govern securing network traffic with IPsec.</span></span> <span data-ttu-id="b3785-106">Les développeurs d’applications peuvent configurer IPsec directement à l’aide de l’API WFP, afin de tirer parti d’un modèle de filtrage du trafic réseau plus granulaire que le modèle exposé via le composant logiciel enfichable MMC (Microsoft Management Console) pour le pare-feu Windows avec fonctions avancées de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b3785-106">Application developers may configure IPsec directly using the WFP API, in order to take advantage of a more granular network traffic filtering model than the model exposed through the Microsoft Management Console (MMC) snap-in for Windows Firewall with Advanced Security.</span></span>

## <a name="what-is-ipsec"></a><span data-ttu-id="b3785-107">Qu’est-ce qu’IPsec ?</span><span class="sxs-lookup"><span data-stu-id="b3785-107">What is IPsec</span></span>

<span data-ttu-id="b3785-108">La sécurité du protocole Internet (IPsec) est un ensemble de protocoles de sécurité utilisés pour transférer des paquets IP de façon confidentielle sur Internet.</span><span class="sxs-lookup"><span data-stu-id="b3785-108">Internet Protocol Security (IPsec) is a set of security protocols used to transfer IP packets confidentially across the Internet.</span></span> <span data-ttu-id="b3785-109">IPsec est obligatoire pour toutes les implémentations IPv6 et facultatif pour IPv4.</span><span class="sxs-lookup"><span data-stu-id="b3785-109">IPsec is mandatory for all IPv6 implementations and optional for IPv4.</span></span>

<span data-ttu-id="b3785-110">Le trafic IP sécurisé comporte deux en-têtes IPsec facultatifs, qui identifient les types de protection par chiffrement appliqués au paquet IP et incluent des informations pour le décodage du paquet protégé.</span><span class="sxs-lookup"><span data-stu-id="b3785-110">Secured IP traffic has two optional IPsec headers, which identify the types of cryptographic protection applied to the IP packet and include information for decoding the protected packet.</span></span>

<span data-ttu-id="b3785-111">L’en-tête ESP (Encapsulating Security Payload) est utilisé pour la confidentialité et la protection contre les modifications malveillantes en effectuant l’authentification et le chiffrement facultatif.</span><span class="sxs-lookup"><span data-stu-id="b3785-111">The Encapsulating Security Payload (ESP) header is used for privacy and protection against malicious modification by performing authentication and optional encryption.</span></span> <span data-ttu-id="b3785-112">Il peut être utilisé pour le trafic qui traverse les routeurs de traduction d’adresses réseau (NAT).</span><span class="sxs-lookup"><span data-stu-id="b3785-112">It can be used for traffic that traverses Network Address Translation (NAT) routers.</span></span>

<span data-ttu-id="b3785-113">L’en-tête d’authentification (AH) est utilisé uniquement pour la protection contre les modifications malveillantes en effectuant l’authentification.</span><span class="sxs-lookup"><span data-stu-id="b3785-113">The Authentication Header (AH) is used only for protection against malicious modification by performing authentication.</span></span> <span data-ttu-id="b3785-114">Elle ne peut pas être utilisée pour le trafic qui traverse les routeurs NAT.</span><span class="sxs-lookup"><span data-stu-id="b3785-114">It cannot be used for traffic that traverses NAT routers.</span></span>

<span data-ttu-id="b3785-115">Pour plus d’informations sur IPsec, consultez également :</span><span class="sxs-lookup"><span data-stu-id="b3785-115">For more information on IPsec, see also:</span></span>

<dl>

<span data-ttu-id="b3785-116">[Informations techniques de référence sur IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b3785-116">[IPsec Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span></span>  
</dl>

## <a name="what-is-ike"></a><span data-ttu-id="b3785-117">Qu’est-ce que IKE ?</span><span class="sxs-lookup"><span data-stu-id="b3785-117">What is IKE</span></span>

<span data-ttu-id="b3785-118">Protocole IKE (Internet Key Exchange) (IKE) est un protocole d’échange de clés qui fait partie de l’ensemble de protocoles IPsec.</span><span class="sxs-lookup"><span data-stu-id="b3785-118">Internet Key Exchange (IKE) is a key exchange protocol that is part of the IPsec protocol set.</span></span> <span data-ttu-id="b3785-119">IKE est utilisé lors de la configuration d’une connexion sécurisée et effectue l’échange sécurisé de clés secrètes et d’autres paramètres liés à la protection sans l’intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3785-119">IKE is used while setting up a secure connection and accomplishes the safe exchange of secret keys and other protection-related parameters without the intervention of the user.</span></span>

<span data-ttu-id="b3785-120">Pour plus d’informations sur IKE, voir aussi :</span><span class="sxs-lookup"><span data-stu-id="b3785-120">For more information on IKE, see also:</span></span>

<dl>

<span data-ttu-id="b3785-121">[protocole IKE (Internet Key Exchange)](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b3785-121">[Internet Key Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span></span>  
</dl>

## <a name="what-is-authip"></a><span data-ttu-id="b3785-122">Présentation d’AuthIP</span><span class="sxs-lookup"><span data-stu-id="b3785-122">What is AuthIP</span></span>

<span data-ttu-id="b3785-123">Protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP) est un nouveau protocole d’échange de clés qui étend IKE comme suit.</span><span class="sxs-lookup"><span data-stu-id="b3785-123">Authenticated Internet Protocol (AuthIP) is a new key exchange protocol that expands IKE as follows.</span></span>

<dl> <span data-ttu-id="b3785-124">Alors que IKE prend uniquement en charge les informations d’authentification de l’ordinateur, AuthIP prend également en charge :</span><span class="sxs-lookup"><span data-stu-id="b3785-124">While IKE only supports computer authentication credentials, AuthIP also supports:</span></span>

-   <span data-ttu-id="b3785-125">Informations d’identification de l’utilisateur : NTLM, Kerberos, certificats.</span><span class="sxs-lookup"><span data-stu-id="b3785-125">User credentials: NTLM, Kerberos, certificates.</span></span>
-   <span data-ttu-id="b3785-126">Certificats d’intégrité de la protection d’accès réseau (NAP).</span><span class="sxs-lookup"><span data-stu-id="b3785-126">Network Access Protection (NAP) health certificates.</span></span>
-   <span data-ttu-id="b3785-127">Informations d’identification anonymes, utilisées pour l’authentification facultative.</span><span class="sxs-lookup"><span data-stu-id="b3785-127">Anonymous credential, used for optional authentication.</span></span>
-   <span data-ttu-id="b3785-128">Combinaison d’informations d’identification ; par exemple, une combinaison d’informations d’identification Kerberos de l’ordinateur et de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3785-128">Combination of credentials; for example, a combination of machine and user Kerberos credentials.</span></span>

  
<span data-ttu-id="b3785-129">AuthIP a un mécanisme de nouvelle tentative d’authentification qui vérifie toutes les méthodes d’authentification configurées avant l’échec de la connexion.</span><span class="sxs-lookup"><span data-stu-id="b3785-129">AuthIP has an authentication-retry mechanism that verifies all configured authentication methods before failing the connection.</span></span>  
<span data-ttu-id="b3785-130">AuthIP peut être utilisé avec des sockets sécurisés pour implémenter le trafic sécurisé IPsec basé sur les applications.</span><span class="sxs-lookup"><span data-stu-id="b3785-130">AuthIP can be used with secure sockets to implement application-based IPsec secured traffic.</span></span> <span data-ttu-id="b3785-131">Il offre :</span><span class="sxs-lookup"><span data-stu-id="b3785-131">It provides:</span></span>

-   <span data-ttu-id="b3785-132">Le chiffrement et l’authentification par socket.</span><span class="sxs-lookup"><span data-stu-id="b3785-132">Per-socket authentication and encryption.</span></span> <span data-ttu-id="b3785-133">Pour plus d’informations, consultez [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) .</span><span class="sxs-lookup"><span data-stu-id="b3785-133">See [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) for more information.</span></span>
-   <span data-ttu-id="b3785-134">Emprunt d’identité du client.</span><span class="sxs-lookup"><span data-stu-id="b3785-134">Client impersonation.</span></span> <span data-ttu-id="b3785-135">(IPsec emprunte l’identité du contexte de sécurité sous lequel le socket est créé.)</span><span class="sxs-lookup"><span data-stu-id="b3785-135">(IPsec impersonates the security context under which the socket is created.)</span></span>
-   <span data-ttu-id="b3785-136">Validation du nom d’homologue entrante et sortante.</span><span class="sxs-lookup"><span data-stu-id="b3785-136">Inbound and outbound peer name validation.</span></span> <span data-ttu-id="b3785-137">Pour plus d’informations, consultez [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) .</span><span class="sxs-lookup"><span data-stu-id="b3785-137">See [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) for more information.</span></span>

  
</dl>

<span data-ttu-id="b3785-138">Pour plus d’informations sur AuthIP, consultez également :</span><span class="sxs-lookup"><span data-stu-id="b3785-138">For more information on AuthIP, see also:</span></span>

<dl>

[<span data-ttu-id="b3785-139">AuthIP dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3785-139">AuthIP in Windows Vista</span></span>](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a><span data-ttu-id="b3785-140">Qu’est-ce qu’une stratégie IPsec ?</span><span class="sxs-lookup"><span data-stu-id="b3785-140">What is an IPsec Policy</span></span>

<span data-ttu-id="b3785-141">Une stratégie IPsec est un ensemble de règles qui déterminent le type de trafic IP qui doit être sécurisé à l’aide d’IPsec et comment sécuriser ce trafic.</span><span class="sxs-lookup"><span data-stu-id="b3785-141">An IPsec policy is a set of rules that determine which type of IP traffic needs to be secured using IPsec and how to secure that traffic.</span></span> <span data-ttu-id="b3785-142">Une seule stratégie IPsec est active sur un ordinateur à la fois.</span><span class="sxs-lookup"><span data-stu-id="b3785-142">Only one IPsec policy is active on a computer at one time.</span></span>

<span data-ttu-id="b3785-143">Pour en savoir plus sur l’implémentation des stratégies IPsec, ouvrez le composant logiciel enfichable MMC stratégie de sécurité locale (secpol. msc), appuyez sur F1 pour afficher l’aide, puis sélectionnez création et utilisation des stratégies IPsec dans la table des matières.</span><span class="sxs-lookup"><span data-stu-id="b3785-143">To learn more about implementing IPsec policies, open the Local Security Policy MMC snap-in (secpol.msc), press F1 to display the Help, and then select Creating and Using IPsec Policies from the table of contents.</span></span>

<span data-ttu-id="b3785-144">Pour plus d’informations sur les stratégies IPsec, voir aussi :</span><span class="sxs-lookup"><span data-stu-id="b3785-144">For more information on IPsec policies, see also:</span></span>

<dl>

<span data-ttu-id="b3785-145">[Vue d’ensemble des concepts de la stratégie IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b3785-145">[Overview of IPsec Policy Concepts](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>  
<span data-ttu-id="b3785-146">[Description d’une stratégie IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b3785-146">[Description of an IPsec Policy](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span></span>  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a><span data-ttu-id="b3785-147">Comment utiliser WFP pour configurer des stratégies IPsec</span><span class="sxs-lookup"><span data-stu-id="b3785-147">How to Use WFP to Configure IPsec Policies</span></span>

<span data-ttu-id="b3785-148">L’implémentation Microsoft d’IPsec utilise la plateforme de filtrage Windows pour configurer des stratégies IPsec.</span><span class="sxs-lookup"><span data-stu-id="b3785-148">The Microsoft implementation of IPsec uses Windows Filtering Platform to setup IPsec policies.</span></span> <span data-ttu-id="b3785-149">Les stratégies IPsec sont implémentées en ajoutant des filtres dans différentes couches WFP comme suit.</span><span class="sxs-lookup"><span data-stu-id="b3785-149">IPsec policies are implemented by adding filters at various WFP layers as follows.</span></span>

-   <span data-ttu-id="b3785-150">Au niveau de la \_ couche FWPM \_ \_ couches IKEEXT V {4 \| 6}, ajoutez des filtres qui spécifient les stratégies de négociation utilisées par les modules de génération de clé (IKE/AuthIP) pendant les échanges en mode principal (mm).</span><span class="sxs-lookup"><span data-stu-id="b3785-150">At the FWPM\_LAYER\_IKEEXT\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules (IKE/AuthIP) during Main Mode (MM) exchanges.</span></span> <span data-ttu-id="b3785-151">Les méthodes d’authentification et les algorithmes de chiffrement sont spécifiés au niveau de ces couches.</span><span class="sxs-lookup"><span data-stu-id="b3785-151">Authentication methods and cryptographic algorithms are specified at these layers.</span></span>
-   <span data-ttu-id="b3785-152">Au niveau des \_ couches FWPM Layer \_ IPSec \_ V {4 \| 6}, ajoutez des filtres qui spécifient les stratégies de négociation utilisées par les modules de génération de clés en mode rapide (QM) et les échanges en mode étendu (EM).</span><span class="sxs-lookup"><span data-stu-id="b3785-152">At the FWPM\_LAYER\_IPSEC\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules during Quick Mode (QM) and Extended Mode (EM) exchanges.</span></span> <span data-ttu-id="b3785-153">Les en-têtes IPsec (AH/ESP) et les algorithmes de chiffrement sont spécifiés au niveau de ces couches.</span><span class="sxs-lookup"><span data-stu-id="b3785-153">IPsec headers (AH/ESP) and cryptographic algorithms are specified at these layers.</span></span>

    <span data-ttu-id="b3785-154">Une stratégie de négociation est spécifiée comme un contexte de fournisseur de stratégie associé au filtre.</span><span class="sxs-lookup"><span data-stu-id="b3785-154">A negotiation policy is specified as a policy provider context associated with the filter.</span></span> <span data-ttu-id="b3785-155">Le module de génération de clés énumère les contextes du fournisseur de stratégie en fonction des caractéristiques du trafic et obtient la stratégie à utiliser pour la négociation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b3785-155">The keying module enumerates the policy provider contexts based on the traffic characteristics and obtains the policy to use for the security negotiation.</span></span>

    > [!Note]  
    > <span data-ttu-id="b3785-156">L’API WFP peut être utilisée pour spécifier les associations de sécurité (SAP) directement et par conséquent pour ignorer la stratégie de négociation du module de génération de clés.</span><span class="sxs-lookup"><span data-stu-id="b3785-156">The WFP API can be used to specify the Security Associations (SAs) directly and therefore to ignore the keying module negotiation policy.</span></span>

     

-   <span data-ttu-id="b3785-157">Au niveau des \_ \_ \_ couches FWPM transport entrant \_ v {4 \| 6} et \_ transport sortant de couche FWPM \_ \_ \_ v {4 \| 6}, ajoutez des filtres qui appellent des légendes et déterminent le flux de trafic à sécuriser.</span><span class="sxs-lookup"><span data-stu-id="b3785-157">At the FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers add filters that invoke callouts and determine which traffic flow should be secured.</span></span>
-   <span data-ttu-id="b3785-158">Au niveau des \_ couches FWPM d’authentification ALE de la couche \_ ALE \_ \_ \_ , accepter les \_ couches {4 \| 6} ajoutez des filtres qui implémentent le filtrage d’identité et la stratégie par application.</span><span class="sxs-lookup"><span data-stu-id="b3785-158">At the FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers add filters that implement identity filtering and per-application policy.</span></span>

<span data-ttu-id="b3785-159">Le diagramme suivant illustre l’interaction des différents composants de WFP, en ce qui concerne le fonctionnement d’IPsec.</span><span class="sxs-lookup"><span data-stu-id="b3785-159">The following diagram illustrates the interaction of the various WFP components, with respect to IPsec operation.</span></span>![configuration IPSec à l’aide de la plateforme de filtrage Windows](images/ipsec-configuration.jpg)

<span data-ttu-id="b3785-161">Une fois IPsec configuré, il s’intègre à WFP et étend les fonctionnalités de filtrage de WFP en fournissant des informations à utiliser comme conditions de filtrage au niveau des couches d’autorisation d’application de la couche application (ALE).</span><span class="sxs-lookup"><span data-stu-id="b3785-161">Once IPsec is configured, it integrates with WFP and extends the WFP filtering capabilities by providing information to be used as filtering conditions at the Application Layer Enforcement (ALE) authorization layers.</span></span> <span data-ttu-id="b3785-162">Par exemple, IPsec fournit l’identité de l’utilisateur distant et de l’ordinateur distant, que WFP expose au niveau de la connexion ALE et accepte les couches d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="b3785-162">For example, IPsec provides the remote user and remote machine identity, which WFP exposes at the ALE connect and accept authorization layers.</span></span> <span data-ttu-id="b3785-163">Ces informations peuvent être utilisées pour une autorisation d’identité à distance fine par une implémentation de pare-feu basée sur WFP.</span><span class="sxs-lookup"><span data-stu-id="b3785-163">This information can be used for fine-grained remote identity authorization by a WFP-based firewall implementation.</span></span>

<span data-ttu-id="b3785-164">Voici un exemple de stratégie d’isolation qui peut être implémentée à l’aide d’IPsec :</span><span class="sxs-lookup"><span data-stu-id="b3785-164">Below is a sample isolation policy that may be implemented using IPsec:</span></span>

-   <span data-ttu-id="b3785-165">\_Couches FWPM \_ IKEEXT \_ V {4 \| 6} couche-authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b3785-165">FWPM\_LAYER\_IKEEXT\_V{4\|6} layers – Kerberos authentication.</span></span>
-   <span data-ttu-id="b3785-166">\_Couches FWPM \_ IPSec \_ V {4 \| 6} couches – Ah/SHA-1.</span><span class="sxs-lookup"><span data-stu-id="b3785-166">FWPM\_LAYER\_IPSEC\_V{4\|6} layers – AH/SHA-1.</span></span>
-   <span data-ttu-id="b3785-167">\_Couche FWPM \_ transport entrant \_ \_ v {4 \| 6} et couche FWPM \_ \_ transport sortant \_ \_ v {4 \| 6} couches-détection de négociation pour tout le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="b3785-167">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers - negotiation discovery for all network traffic.</span></span>
-   <span data-ttu-id="b3785-168">FWPM \_ \_ de l’authentification ALE de la couche ALE \_ \_ \_ \_ -accepter les couches V {4 \| 6}-IPSec requis pour tout le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="b3785-168">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers - IPsec required for all network traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3785-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3785-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3785-170">**Couches WFP**</span><span class="sxs-lookup"><span data-stu-id="b3785-170">**WFP Layers**</span></span>
</dt> <dt>

[<span data-ttu-id="b3785-171">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="b3785-171">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="b3785-172">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="b3785-172">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

<span data-ttu-id="b3785-173">**Scénarios de stratégie IPsec implémentés à l’aide de l’API WFP :**</span><span class="sxs-lookup"><span data-stu-id="b3785-173">**IPsec Policy Scenarios Implemented using WFP API:**</span></span>
</dt> <dt>

[<span data-ttu-id="b3785-174">mode de transport</span><span class="sxs-lookup"><span data-stu-id="b3785-174">Transport Mode</span></span>](regular-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="b3785-175">Mode de transport de la découverte de négociation</span><span class="sxs-lookup"><span data-stu-id="b3785-175">Negotiation Discovery Transport Mode</span></span>](negotiation-discovery-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="b3785-176">Mode de transport de la découverte de négociation en mode limite</span><span class="sxs-lookup"><span data-stu-id="b3785-176">Negotiation Discovery Transport Mode in Boundary Mode</span></span>](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[<span data-ttu-id="b3785-177">Mode de tunnel</span><span class="sxs-lookup"><span data-stu-id="b3785-177">Tunnel Mode</span></span>](tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="b3785-178">Chiffrement garanti</span><span class="sxs-lookup"><span data-stu-id="b3785-178">Guaranteed Encryption</span></span>](guaranteed-encryption.md)
</dt> <dt>

[<span data-ttu-id="b3785-179">Autorisation d’identité distante</span><span class="sxs-lookup"><span data-stu-id="b3785-179">Remote Identity Authorization</span></span>](remote-identity-authorization.md)
</dt> <dt>

[<span data-ttu-id="b3785-180">SAs IPsec manuelle</span><span class="sxs-lookup"><span data-stu-id="b3785-180">Manual IPsec SAs</span></span>](manual-ipsec-sas.md)
</dt> <dt>

[<span data-ttu-id="b3785-181">Exemptions IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="b3785-181">IKE/AuthIP Exemptions</span></span>](ike-exemptions.md)
</dt> <dt>

<span data-ttu-id="b3785-182">**Solutions IPsec :**</span><span class="sxs-lookup"><span data-stu-id="b3785-182">**IPsec Solutions:**</span></span>
</dt> <dt>

<span data-ttu-id="b3785-183">[Isolation de serveur et de domaine](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b3785-183">[Server and Domain Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>
</dt> </dl>

 

 