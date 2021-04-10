---
title: Comportement de mise en cache du code confidentiel EAP-TLS SSO
description: Fournit une approche étape par étape pour résoudre les problèmes de reprise de session et de réauthentification d’un utilisateur itinérant dans un environnement EAP-TLS SSO.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7c4e3058598f98327570fbcd0347cfb84e5825
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101121"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="61740-103">Comportement de mise en cache du code confidentiel EAP-TLS SSO</span><span class="sxs-lookup"><span data-stu-id="61740-103">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="61740-104">Cette rubrique fournit une approche étape par étape pour résoudre les problèmes de reprise de session et de réauthentification d’un utilisateur itinérant dans un environnement EAP-TLS SSO.</span><span class="sxs-lookup"><span data-stu-id="61740-104">This topic provides a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="61740-105">Approche étape par étape</span><span class="sxs-lookup"><span data-stu-id="61740-105">Step-By-Step Approach</span></span>

<span data-ttu-id="61740-106">La liste suivante représente une approche étape par étape pour résoudre les problèmes de reprise de session et de réauthentification d’un utilisateur itinérant dans un environnement EAP-TLS SSO.</span><span class="sxs-lookup"><span data-stu-id="61740-106">The following list represents a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

-   <span data-ttu-id="61740-107">Après la première authentification réussie dans un environnement SSO avec EAP-TLS, le demandeur conserve par défaut toutes les informations relatives aux informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61740-107">After the first successful authentication in an SSO environment with EAP-TLS, the supplicant retains all user credential related information by default.</span></span>
    > [!Note]  
    > <span data-ttu-id="61740-108">Bien que soumis à l’implémentation de demandeur particulière, il est recommandé au demandeur de conserver la structure de [**\_ tableau de \_ \_ champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) complète que le demandeur a utilisé en dernier dans l’appel [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) à EAPHost.</span><span class="sxs-lookup"><span data-stu-id="61740-108">Although subject to the particular supplicant implementation, it's advisable for the supplicant to retain the entire [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure that the supplicant last used in the [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) call to EAPHost.</span></span>

     

-   <span data-ttu-id="61740-109">À mesure que l’utilisateur se déplace pour la première fois et que la réauthentification commence, le demandeur appelle à nouveau [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) avec la même structure de [**tableau de \_ \_ \_ champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) ; le demandeur doit également passer le même objet blob d’utilisateur conservé après la première authentification réussie.</span><span class="sxs-lookup"><span data-stu-id="61740-109">As the user first roams and the re-authentication begins, the supplicant calls [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) again with the same [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure; the supplicant must also pass in the same user BLOB retained after the first successful authentication.</span></span>
-   <span data-ttu-id="61740-110">EAPHost transmet ensuite les informations de l’objet BLOB utilisateur à la méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="61740-110">EAPHost then passes the information in the user BLOB to the EAP method.</span></span>
-   <span data-ttu-id="61740-111">La méthode EAP met à jour à son tour l’objet BLOB de l’utilisateur avec les champs d’informations d’identification, le code confidentiel par exemple fourni dans *pEapConfigInputFieldArray*, et conserve les valeurs restantes, le certificat de serveur, par exemple, tel qu’il était dans l’objet blob d’origine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61740-111">The EAP method in turn updates the user BLOB with credential fields - the PIN for example - provided in *pEapConfigInputFieldArray*, and keeps the remaining values - the server certificate for example - as it was in the original user BLOB.</span></span>
-   <span data-ttu-id="61740-112">Une fois ces étapes terminées, le demandeur peut reprendre l’authentification de manière normale en appelant la fonction runtime [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) avec cet objet blob d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61740-112">After completing these steps, the supplicant can resume authentication in a normal way by calling the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) run-time function with this user BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61740-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61740-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61740-114">Scénarios d’authentification unique EAPHost</span><span class="sxs-lookup"><span data-stu-id="61740-114">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="61740-115">SSO et PLAP</span><span class="sxs-lookup"><span data-stu-id="61740-115">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




