---
title: Authenticator Séquence d’appel de l’API de méthode
description: En savoir plus sur la séquence d’appels d’API de méthode d’authentificateur. Consultez une liste qui illustre la séquence des appels effectués par une EAPHost sur une méthode d’authentificateur EAP.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3864d7b08c3c5c154ef3be86d0ac14716cd8b46adb1485fc5c55e598f870a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852289"
---
# <a name="authenticator-method-api-call-sequence"></a>Authenticator Séquence d’appel de l’API de méthode

Cette rubrique fournit la séquence d’appel spécifique pour l’API de méthode d’authentificateur. Lors d’une session d’authentification EAP classique, EAPHost effectue un certain nombre d’appels sur une méthode EAP qui implémente les API de méthode d’authentificateur EAPHost.

La liste suivante illustre la séquence d’appels effectuée par EAPHost sur une méthode d’authentificateur EAP.

-   L’authentificateur EAP charge d’abord la DLL de méthode EAP utilisée pour l’authentification spécifique sur un serveur NPS (Network Policy Server) ou un autre serveur d’authentification.
-   Appelle [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) sur la méthode avec une structure [**de \_ type EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) remplie pour obtenir une liste de pointeurs vers des fonctions implémentées sur la dll. Les appels de fonction suivants par les méthodes d’authentificateur (serveur) sont supposés être implémentés sur la DLL.
-   Appelle [**EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) pour indiquer à la bibliothèque de méthodes EAP de préparer au moins une session d’authentification à l’aide de cette méthode de l’authentificateur.
-   Appelle [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) pour établir une session d’authentification unique.
-   Répète les étapes suivantes jusqu’à ce que [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) indique qu’un résultat d’authentification est disponible.
    -   Appelle [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) avec un pointeur vers un paquet de demande à passer au demandeur.
    -   Appelle [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) pour récupérer le paquet de réponse envoyé par le demandeur. Cette fonction retourne un code d’action de réponse de l' **\_ authentificateur de méthode \_ \_ \_ EAP** qui indique la prochaine action que l’authentificateur doit effectuer dans la session d’authentification EAP.
    -   Si le code d’action est réponse à l' [ \_ authentificateur de méthode \_ \_ \_ EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), il indique que la méthode EAP a des attributs disponibles pour que l’authentificateur récupère et passe à la méthode homologue. Authenticator appelle [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) pour obtenir les différents attributs d’authentification eap à partir de la méthode d’authentificateur eap. Une fois que l’authentificateur a traité les attributs, il appelle [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) , qui fournit les attributs d’authentification EAP mis à jour à définir sur la méthode de l’authentificateur EAP. Cette fonction retourne un code d’action de réponse de l' **\_ authentificateur de méthode \_ \_ \_ EAP** qui détermine l’action suivante.
-   Si le code d’action est le résultat de la réponse de l' [ \_ authentificateur de méthode \_ \_ \_ EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), il indique que l’authentificateur a déterminé les résultats de la session d’authentification et que ces résultats sont disponibles pour EAPHost. Authenticator appelle [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) et obtient les résultats de la session d’authentification.
-   Ceci est suivi d’un appel à [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) pour mettre fin à la session d’authentification.
-   Enfin, un appel est fait à [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) pour décharger la dll de la méthode de l’authentificateur.
-   Décharge la bibliothèque de méthodes EAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ACTION de réponse de l' \_ authentificateur de méthode EAP \_ \_ \_**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Séquence d’appel de l’API Supplier](supplicant-api-call-sequence.md)
</dt> <dt>

[Séquence d’appel de l’API de méthode homologue](peer-method-api-call-sequence.md)
</dt> <dt>

[Séquences d’appels EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




