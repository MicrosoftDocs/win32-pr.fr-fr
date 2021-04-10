---
title: Implémentation de la prise en charge NAP pour les méthodes EAP
description: Découvrez comment implémenter la prise en charge de la protection d’accès réseau pour un demandeur EAPHost. Consultez les rubriques relatives à la protection d’accès réseau (NAP) de EAPHost et consultez les ressources disponibles supplémentaires.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104032129"
---
# <a name="implementing-nap-support-for-eap-methods"></a><span data-ttu-id="35c99-104">Implémentation de la prise en charge NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="35c99-104">Implementing NAP Support for EAP Methods</span></span>

<span data-ttu-id="35c99-105">Cette rubrique explique comment implémenter la protection d’accès réseau pour un demandeur EAPHost.</span><span class="sxs-lookup"><span data-stu-id="35c99-105">This topic explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="35c99-106">Dans Windows Vista et Windows Server 2008, un client de contrainte de mise en conformité NAP (NAP EC) est disponible pour les connexions authentifiées [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="35c99-106">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span>

## <a name="implementing-network-access-protection-nap"></a><span data-ttu-id="35c99-107">Implémentation de la protection d’accès réseau (NAP)</span><span class="sxs-lookup"><span data-stu-id="35c99-107">Implementing Network Access Protection (NAP)</span></span>

<span data-ttu-id="35c99-108">Pour prendre en charge la protection d’accès réseau (NAP), un demandeur EAPHost implémente une fonction de rappel correspondant au prototype de rappel [**NotificationHandler**](/previous-versions/windows/desktop/api) et doit fournir un pointeur vers cette fonction de rappel lors de l’appel de [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="35c99-108">To support NAP, an EAPHost supplicant implements a callback function matching the [**NotificationHandler**](/previous-versions/windows/desktop/api) callback prototype and must provide a pointer to this callback function when calling [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>

<span data-ttu-id="35c99-109">La fonction de rappel accepte deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="35c99-109">The callback function takes two parameters.</span></span>

-   <span data-ttu-id="35c99-110">GUID qui identifie de façon unique l’interface associée à l’authentification.</span><span class="sxs-lookup"><span data-stu-id="35c99-110">A GUID that uniquely identifies the interface associated with the authentication.</span></span>
-   <span data-ttu-id="35c99-111">Pointeur VOID vers une structure de données opaque fournie par le demandeur.</span><span class="sxs-lookup"><span data-stu-id="35c99-111">A VOID pointer to an opaque data structure that is supplied by the supplicant.</span></span>

<span data-ttu-id="35c99-112">EAPHost appellera la fonction de rappel fournie par le demandeur avec le GUID d’interface unique et le pointeur VOID lorsque l’état de mise en quarantaine de l’ordinateur change.</span><span class="sxs-lookup"><span data-stu-id="35c99-112">EAPHost will call the supplicant-provided callback function with the unique interface GUID and the VOID pointer when the quarantine state of the machine changes.</span></span> <span data-ttu-id="35c99-113">Quand EAPHost appelle la fonction de rappel fournie par le demandeur, le demandeur répond en détachant la connexion réseau logique identifiée par le pointeur d’interface GUID/VOID et recommence l’authentification à l’aide de **EapHostPeerBeginSession**.</span><span class="sxs-lookup"><span data-stu-id="35c99-113">When EAPHost calls the supplicant-provided callback function, the supplicant responds by tearing down the logical network connection identified by the interface GUID/VOID pointer and begins authentication again using **EapHostPeerBeginSession**.</span></span>

<span data-ttu-id="35c99-114">EAPHost peut appeler la fonction de rappel fournie par le demandeur à tout moment : avant, pendant une authentification active ou une fois l’authentification terminée (après l’appel de [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) mais pas avant l’appel de [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ).</span><span class="sxs-lookup"><span data-stu-id="35c99-114">EAPHost may call the supplicant-supplied callback function at any time: before, during an active authentication, or after the authentication has been completed (after [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) has been called but not before [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) has been called).</span></span> <span data-ttu-id="35c99-115">Le demandeur doit toujours répondre en détachant la connexion réseau logique et en réauthentifiant.</span><span class="sxs-lookup"><span data-stu-id="35c99-115">The supplicant should always respond by tearing down the logical network connection and re-authenticating.</span></span>

<span data-ttu-id="35c99-116">Si le demandeur s’arrête ou si vous choisissez de ne plus recevoir de notification des modifications d’état d’isolement, le demandeur doit appeler [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) et spécifier le GUID d’interface approprié.</span><span class="sxs-lookup"><span data-stu-id="35c99-116">If the supplicant is shutting down or choosing to no longer receive notification of isolation state changes, the supplicant should call [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) and specify the appropriate interface GUID.</span></span> <span data-ttu-id="35c99-117">Si le demandeur souhaite déterminer l’isolation de la connexion réseau logique, le demandeur peut obtenir ces informations à partir de **EapHostPeerMethodResult. isolationState** lorsque le [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) est obtenu à partir de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span><span class="sxs-lookup"><span data-stu-id="35c99-117">If the supplicant wishes to determine the isolation of the logical network connection, the supplicant can obtain that information from **EapHostPeerMethodResult.isolationState** when the [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) is obtained from [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span></span>

## <a name="eaphost-related-nap-information"></a><span data-ttu-id="35c99-118">Informations NAP relatives à EAPHost</span><span class="sxs-lookup"><span data-stu-id="35c99-118">EAPHost Related NAP Information</span></span>

<span data-ttu-id="35c99-119">Pour obtenir des informations sur l’API EAPHost, reportez-vous aux rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="35c99-119">For EAPHost API related NAP information refer to the following topics.</span></span>

-   [<span data-ttu-id="35c99-120">**\_type d’attribut EAP \_**</span><span class="sxs-lookup"><span data-stu-id="35c99-120">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [<span data-ttu-id="35c99-121">**\_erreur EAP**</span><span class="sxs-lookup"><span data-stu-id="35c99-121">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [<span data-ttu-id="35c99-122">Forum aux questions sur le demandeur EAPHost</span><span class="sxs-lookup"><span data-stu-id="35c99-122">EAPHost Supplicant Frequently Asked Questions</span></span>](eaphost-supplicant-frequently-asked-questions.md)
-   [<span data-ttu-id="35c99-123">**Propriétés de la méthode EAP**</span><span class="sxs-lookup"><span data-stu-id="35c99-123">**EAP Method Properties**</span></span>](eap-method-properties.md)
-   [<span data-ttu-id="35c99-124">**EapHostPeerBeginSession**</span><span class="sxs-lookup"><span data-stu-id="35c99-124">**EapHostPeerBeginSession**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [<span data-ttu-id="35c99-125">**Constantes d’informations et d’erreurs liées à EAP**</span><span class="sxs-lookup"><span data-stu-id="35c99-125">**EAP Related Error and Information Constants**</span></span>](eap-related-error-and-information-constants.md)
-   [<span data-ttu-id="35c99-126">**État d’isolement \_**</span><span class="sxs-lookup"><span data-stu-id="35c99-126">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [<span data-ttu-id="35c99-127">**NotificationHandler**</span><span class="sxs-lookup"><span data-stu-id="35c99-127">**NotificationHandler**</span></span>](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a><span data-ttu-id="35c99-128">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="35c99-128">Additional Resources</span></span>


-   <span data-ttu-id="35c99-129">Pour obtenir la liste des ressources NAP, consultez [protection d’accès réseau](https://go.microsoft.com/fwlink/p/?linkid=84107).</span><span class="sxs-lookup"><span data-stu-id="35c99-129">For a list of NAP resources, see [Network Access Protection](https://go.microsoft.com/fwlink/p/?linkid=84107).</span></span>
-   <span data-ttu-id="35c99-130">Pour obtenir des informations sur la déclaration d’intégrité, voir [messages de déclaration d’intégrité (SoH) de la protection d’accès réseau (NAP](https://go.microsoft.com/fwlink/p/?linkid=83918)).</span><span class="sxs-lookup"><span data-stu-id="35c99-130">For Statement of Health information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>
-   <span data-ttu-id="35c99-131">Pour la page Web du groupe de mise en réseau d’entreprise et le blog, consultez [protection d’accès réseau (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span><span class="sxs-lookup"><span data-stu-id="35c99-131">For the Enterprise Networking Group webpage and blog, see [Network Access Protection (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span></span>
-   <span data-ttu-id="35c99-132">Pour obtenir des informations sur l’API NAP, consultez [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page).</span><span class="sxs-lookup"><span data-stu-id="35c99-132">For NAP API information, see [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page).</span></span>


## <a name="related-topics"></a><span data-ttu-id="35c99-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35c99-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35c99-134">Configuration de l’interface utilisateur de la méthode EAP</span><span class="sxs-lookup"><span data-stu-id="35c99-134">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="35c99-135">Activation de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="35c99-135">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="35c99-136">Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="35c99-136">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="35c99-137">Transfert de données entre le demandeur et les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="35c99-137">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="35c99-138">Demandeurs EAPHost</span><span class="sxs-lookup"><span data-stu-id="35c99-138">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 