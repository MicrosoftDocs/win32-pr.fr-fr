---
title: Séquence d’appel de l’API de méthode de tunnel
description: En savoir plus sur la séquence d’appel d’API pour les méthodes de tunnel. Consultez une vue d’ensemble et affichez des ressources supplémentaires disponibles.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316505"
---
# <a name="tunnel-method-api-call-sequence"></a><span data-ttu-id="71f62-104">Séquence d’appel de l’API de méthode de tunnel</span><span class="sxs-lookup"><span data-stu-id="71f62-104">Tunnel Method API Call Sequence</span></span>

<span data-ttu-id="71f62-105">Cette rubrique couvre la séquence d’appels d’API pour les méthodes de tunnel</span><span class="sxs-lookup"><span data-stu-id="71f62-105">This topic covers the API call sequence for Tunnel Methods</span></span>

## <a name="tunnel-method-call-sequence-overview"></a><span data-ttu-id="71f62-106">Vue d’ensemble de la séquence d’appels de méthode de tunnel</span><span class="sxs-lookup"><span data-stu-id="71f62-106">Tunnel Method Call Sequence Overview</span></span>

<span data-ttu-id="71f62-107">Lorsque le demandeur reçoit une demande pour l’identité de l’utilisateur et les données utilisateur, le workflow d’appel d’API suivant se produit généralement.</span><span class="sxs-lookup"><span data-stu-id="71f62-107">When Supplicant gets request for user identity and user data the following API call flow typically occurs.</span></span>

-   <span data-ttu-id="71f62-108">Le demandeur appelle EapHostPeerProcessReceivedPacket sur EapHost pour traiter le paquet reçu de l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="71f62-108">The Supplicant calls EapHostPeerProcessReceivedPacket on EapHost, to process the packet received from the authenticator.</span></span>
-   <span data-ttu-id="71f62-109">Lors du traitement de ce paquet, EAPHost le détermine comme paquet IdentityRequest et appelle [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sur la méthode de tunnel pour obtenir l’identité de l’utilisateur à utiliser pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="71f62-109">Upon processing this packet, EAPHost determines it as IdentityRequest packet and calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on tunnel method to obtain the user identity to use for authentication.</span></span>
-   <span data-ttu-id="71f62-110">Si la méthode de tunnel doit obtenir l’identité de l’utilisateur à partir de la méthode interne, elle appelle [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) sur l’EAPHost interne, qui à son tour appelle [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sur la méthode interne.</span><span class="sxs-lookup"><span data-stu-id="71f62-110">If tunnel method needs to obtain user identity from the inner method, it calls [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) on inner EAPHost, which in turn calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on the inner method.</span></span>

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a><span data-ttu-id="71f62-111">Interaction de l’utilisateur avec le workflow de l’API méthodes de tunnel</span><span class="sxs-lookup"><span data-stu-id="71f62-111">User Interaction with the Tunnel Methods API Call Flow</span></span>

<span data-ttu-id="71f62-112">Dans certains cas, lorsque l’identité n’est pas disponible, ou lorsque l’utilisateur doit fournir des informations supplémentaires, la méthode EAP génère une boîte de dialogue d’interface utilisateur sur le demandeur.</span><span class="sxs-lookup"><span data-stu-id="71f62-112">In certain cases, when the identity is not available, or when the user must provide additional information, Eap Method raises an user interface dialog box on the supplicant.</span></span>

<span data-ttu-id="71f62-113">Dans ce cas, la séquence d’appel suivante se produit généralement pour recevoir des informations directement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71f62-113">In such cases following call sequence typically takes place to get information directly from the user.</span></span>

-   <span data-ttu-id="71f62-114">La méthode tunnel EAP retourne le code d’action pour appeler l’interface utilisateur sur EapHost.</span><span class="sxs-lookup"><span data-stu-id="71f62-114">Tunnel Eap Method returns action code to invoke UI to EapHost.</span></span> <span data-ttu-id="71f62-115">Le demandeur appelle [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)pour obtenir les informations de contexte de l’interface utilisateur actuelle pour la boîte de dialogue de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71f62-115">Supplicant calls [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)to obtain the current user interface context information for the user interface dialog box.</span></span>
-   <span data-ttu-id="71f62-116">Le demandeur appelle ensuite [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="71f62-116">Supplicant then calls [**EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span> <span data-ttu-id="71f62-117">Cette fonction utilise les informations de contexte de l’interface utilisateur pour déclencher une interface utilisateur interactive qui est utilisée pour récupérer les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71f62-117">This function uses the UI context information to raise an interactive user interface which is used to get credential information from the user.</span></span> <span data-ttu-id="71f62-118">Le processus d’interface utilisateur charge Eappcfg.dll et obtient les pointeurs vers EapPeerInvokeInteractiveUI et EapPeerFreeMemory.</span><span class="sxs-lookup"><span data-stu-id="71f62-118">The UI process loads Eappcfg.dll and obtains the pointers to EapPeerInvokeInteractiveUI and EapPeerFreeMemory.</span></span>
    > [!Note]  
    > <span data-ttu-id="71f62-119">Le processus d’interface utilisateur collecte généralement l’interface utilisateur ou gère l’interface utilisateur interactive et est séparé du processus du demandeur.</span><span class="sxs-lookup"><span data-stu-id="71f62-119">UI process typically collects UI or handles interactive UI and is separate from the supplicant process.</span></span> <span data-ttu-id="71f62-120">La séparation des deux processus n’est pas une exigence d’EAPHost, mais cela présente l’avantage de permettre au processus de l’interface utilisateur d’interagir avec le bureau.</span><span class="sxs-lookup"><span data-stu-id="71f62-120">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

-   <span data-ttu-id="71f62-121">EapHost appelle [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sur la méthode de tunnel pour obtenir les informations d’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71f62-121">EapHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on tunnel method to obtain user identity information.</span></span>
-   <span data-ttu-id="71f62-122">Afin d’obtenir l’identité de l’utilisateur à partir de la méthode interne, la méthode de tunnel appelle [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) sur l’EAPHost interne.</span><span class="sxs-lookup"><span data-stu-id="71f62-122">In order to obtain user identity from inner method, tunnel method calls [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) on inner EAPHost.</span></span>
-   <span data-ttu-id="71f62-123">L’interface EAPHost interne appelle [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sur la méthode interne pour appeler l’interface utilisateur de l’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71f62-123">Inner EAPHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on inner method to invoke user identity UI.</span></span>
-   <span data-ttu-id="71f62-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) fournit des informations de contexte d’interface utilisateur nouvelles ou mises à jour à la méthode d’homologue EAP chargée sur EAPHost après le déclenchement de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71f62-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) provides a new or updated UI context information to the EAP peer method loaded on EAPHost after the UI has been raised.</span></span>

<span data-ttu-id="71f62-125">Le diagramme suivant explique la séquence d’appels d’API pour les méthodes de tunnel</span><span class="sxs-lookup"><span data-stu-id="71f62-125">Following diagram explains the API Call Sequence for Tunnel Methods</span></span>

![séquence d’appel de l’API méthodes de tunnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a><span data-ttu-id="71f62-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71f62-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f62-128">Séquence d’appel EAPHost</span><span class="sxs-lookup"><span data-stu-id="71f62-128">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="71f62-129">Séquence d’appel de l’API Supplier</span><span class="sxs-lookup"><span data-stu-id="71f62-129">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="71f62-130">Informations de référence sur l’API Supplier EAPHost</span><span class="sxs-lookup"><span data-stu-id="71f62-130">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




