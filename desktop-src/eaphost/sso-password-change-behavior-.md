---
title: Comportement de modification du mot de passe SSO
description: Fournit une approche pas à pas pour résoudre le comportement de modification du mot de passe SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106536884"
---
# <a name="sso-password-change-behavior"></a><span data-ttu-id="bea3f-103">Comportement de modification du mot de passe SSO</span><span class="sxs-lookup"><span data-stu-id="bea3f-103">SSO Password Change Behavior</span></span>

<span data-ttu-id="bea3f-104">Cette rubrique fournit une approche étape par étape pour résoudre le comportement de modification du mot de passe SSO.</span><span class="sxs-lookup"><span data-stu-id="bea3f-104">This topic provides a step-by-step approach for resolving SSO password change behavior.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="bea3f-105">Approche étape par étape</span><span class="sxs-lookup"><span data-stu-id="bea3f-105">Step-By-Step Approach</span></span>

<span data-ttu-id="bea3f-106">La liste suivante représente une approche étape par étape pour la résolution du comportement de modification du mot de passe SSO.</span><span class="sxs-lookup"><span data-stu-id="bea3f-106">The following list represents a step-by-step approach for resolving SSO password change behavior.</span></span>

-   <span data-ttu-id="bea3f-107">Une fois que la méthode EAP est notifiée d’une modification de mot de passe, la méthode notifie EAPHost ; EAPHost notifie à son tour le demandeur en retournant le code d’action, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="bea3f-107">Once the EAP method is notified about a password change, the method notifies EAPHost; EAPHost in turn notifies the supplicant by returning the action code, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="bea3f-108">Après avoir reçu le code d’action [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) d’EAPHost, le demandeur obtient le contexte de l’interface utilisateur à partir de la méthode EAP en appelant la fonction [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) ; EAPHost obtient ensuite le contexte de l’interface utilisateur à partir de la méthode EAP en appelant la fonction de méthode correspondante</span><span class="sxs-lookup"><span data-stu-id="bea3f-108">After receiving the [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) action code from EAPHost, the supplicant obtains the UI context from the EAP method by calling the [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) function; EAPHost then obtains the UI context from the EAP method by calling the corresponding method function</span></span>
-   <span data-ttu-id="bea3f-109">Le demandeur passe le contexte de l’interface utilisateur au processus d’interface utilisateur (à l’aide d’une forme de communication inter-processus).</span><span class="sxs-lookup"><span data-stu-id="bea3f-109">The supplicant passes the UI context to the UI process (using some form of inter-process communication).</span></span>
-   <span data-ttu-id="bea3f-110">Le processus d’interface utilisateur appelle [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) sur EAPHost.</span><span class="sxs-lookup"><span data-stu-id="bea3f-110">The UI process calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) on EAPHost.</span></span>
-   <span data-ttu-id="bea3f-111">EAPHost collecte le contexte de l’interface utilisateur en appelant [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) sur la méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="bea3f-111">EAPHost collects the UI context by calling [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) on the EAP method.</span></span>
-   <span data-ttu-id="bea3f-112">La méthode EAP fournit toutes les informations de contexte d’interface utilisateur nécessaires dans la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , où *DwDataType* a la valeur *EapCredExpiryReq* et *pbUiData* pointe vers une structure de type [**EAP \_ cred \_ req**](eap-cred-req.md).</span><span class="sxs-lookup"><span data-stu-id="bea3f-112">The EAP method provides any necessary UI context information in the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, where *dwDataType* is set to *EapCredExpiryReq* and *pbUiData* points to a structure of type [**EAP\_CRED\_REQ**](eap-cred-req.md).</span></span>
-   <span data-ttu-id="bea3f-113">Lors du remplissage de la structure de données de l' [**\_ \_ \_ interface utilisateur interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , cette méthode EAP ne renseigne que le paramètre *curCreds* et ne définit pas l’indicateur de [**\_ \_ \_ \_ \_ lecture \_ seule des champs d’entrée de l’interface utilisateur EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) dans la structure de **\_ \_ \_ \_ données du champ d’entrée de la configuration EAP** .</span><span class="sxs-lookup"><span data-stu-id="bea3f-113">While populating the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, this EAP method will only fill in the *curCreds* parameter, and not set the [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag in the **EAP\_CONFIG\_INPUT\_FIELD\_DATA** structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="bea3f-114">L’indicateur de [**\_ \_ \_ \_ \_ lecture \_ seule des champs d’entrée de l’interface utilisateur EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) concerne les champs de membre qui doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="bea3f-114">The [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag is for member field(s) which need to be changed.</span></span>

     

-   <span data-ttu-id="bea3f-115">Après avoir collecté le contexte de l’interface utilisateur informtion, le processus de l’interface utilisateur affiche une interface utilisateur pour collecter les informations de mot de passe de modification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bea3f-115">Having collected the UI context informtion, the UI process renders a UI to collect change password information from the user.</span></span> <span data-ttu-id="bea3f-116">Ces informations sont renseignées dans le paramètre *NewCreds* de la structure de [**demande d’expiration d' \_ \_ expiration \_ du protocole EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .</span><span class="sxs-lookup"><span data-stu-id="bea3f-116">This information is populated in the *NewCreds* parameter of the [**EAP\_CRED\_EXPIRY\_REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) structure.</span></span>
-   <span data-ttu-id="bea3f-117">Le processus d’interface utilisateur transmet la structure de [**\_ \_ réponse EAP cred**](eap-cred-resp.md) à EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span><span class="sxs-lookup"><span data-stu-id="bea3f-117">The UI process passes the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure back to EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span></span>
-   <span data-ttu-id="bea3f-118">Le processus d’interface utilisateur transmet cet objet BLOB d’utilisateur au demandeur, et le demandeur continue les fonctions d’exécution EAPHost comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="bea3f-118">The UI process passes this user BLOB to the supplicant, and the supplicant continues with EAPHost run-time functions as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bea3f-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bea3f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bea3f-120">Scénarios d’authentification unique EAPHost</span><span class="sxs-lookup"><span data-stu-id="bea3f-120">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="bea3f-121">SSO et PLAP</span><span class="sxs-lookup"><span data-stu-id="bea3f-121">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




