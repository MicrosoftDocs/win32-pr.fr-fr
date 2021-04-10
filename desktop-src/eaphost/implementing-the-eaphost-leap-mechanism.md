---
title: Implémentation du mécanisme d’LEAP EAPHost
description: Décrit le mécanisme EAPHost qui permet à des tiers d’écrire des modules LEAP (Extensible Authentication Protocol) légers pour Windows.
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc50cda8d32cc26dd81af5733345deebb579c792
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102508"
---
# <a name="implementing-the-eaphost-leap-mechanism"></a>Implémentation du mécanisme d’LEAP EAPHost

Cette rubrique décrit le mécanisme EAPHost qui permet à des tiers d’écrire des modules LEAP (Extensible Authentication Protocol) légers pour Windows. LEAP est une méthode d’authentification héritée, créée par Cisco, conformément à la [norme RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016). Pour plus d’informations sur LEAP, consultez [Cisco LEAP Q&A](https://go.microsoft.com/fwlink/p/?linkid=84018).

## <a name="eaphost-authentication-process"></a>Processus d’authentification EAPHost

Le processus d’authentification EAPHost standard se produit comme suit :

-   L’authentificateur envoie une demande d’authentification de l’homologue. Par exemple, l’application appelle [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) avec la configuration EAPHost et les données utilisateur.
-   L’homologue envoie un paquet de réponse en réponse à une demande valide. Par exemple, un appel réussi retourne un handle de session de **\_ \_ handle de session EAP** .
-   L’authentificateur envoie un paquet de demande supplémentaire et l’homologue répond avec une réponse. Par exemple, l’application appelle [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) pour obtenir les paquets EAP reçus par EAPHost tout au long de la session. Chaque paquet est traité par un appel à [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket).
-   [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) retourne toujours un code d’action. Le demandeur doit ensuite appeler la fonction correspondant au code d’action.
-   La séquence des demandes et des réponses se poursuit aussi longtemps que nécessaire. Par exemple, l’application peut appeler [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) pour demander des attributs EAP disponibles, et l’homologue répond avec [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) pour les retourner.
-   Après une demande initiale, une nouvelle demande ne peut pas être envoyée tant qu’une réponse valide n’a pas été reçue.
-   La conversation se poursuit jusqu’à ce que l’authentificateur ne puisse pas authentifier l’homologue. dans ce cas, l’implémentation de l’authentificateur doit transmettre un échec EAP. Par exemple, les réponses inacceptables à une ou plusieurs demandes obligent l’authentificateur à transmettre un échec EAP code 4.
-   Sinon, la conversation d’authentification peut se poursuivre jusqu’à ce que l’authentificateur détermine que l’authentification réussie s’est produite, auquel cas l’authentificateur doit transmettre une réussite EAP (code 3).
-   Que le résultat indique la réussite ou l’échec, l’application appelle [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) pour mettre fin à la session. En cas de défaillance, une nouvelle authentification peut être tentée en ouvrant une autre session avec EAPHost et en fournissant la même identité ou une nouvelle identité.

### <a name="leap-authentication-process"></a>Processus d’authentification LEAP

Le processus d’authentification LEAP diffère du processus d’authentification EAPhost standard, comme suit :

-   L’authentification EAP est lancée par le serveur (authentificateur). Par opposition, le client (homologue) initie le LEAP.
    -   Par conséquent, lors de l’écriture d’un module LEAP, vous devez toujours vous assurer que le paquet de demande de vérification de la méthode d’homologue et la réponse EAP du serveur EAP doivent toujours avoir le même ID de paquet que celui du paquet de réussite EAP du serveur.

    <!-- -->

    -   En revanche, les paquets de demande et de réponse EAPHost et les paquets de réussite ont généralement des ID différents.
        > [!Note]  
        > Chaque demande EAP a un champ type pour indiquer ce qui est demandé. Comme pour le paquet de demande, chaque paquet de réponse EAP contient un champ de type, qui correspond au champ de type de la demande. Citons par exemple les paquets de demande d’identité et de demande de stimulation.

         

-   En cas de défaillance avec EAPHost, une nouvelle authentification peut être tentée en ouvrant une autre session avec EAPHost et en fournissant la même identité ou une nouvelle identité.

### <a name="leap-authenticator-method-implementation"></a>Implémentation de la méthode d’authentificateur LEAP

Lors du développement d’une méthode d’authentificateur LEAP, vérifiez les points suivants :

-   Les méthodes d’authentificateur LEAP doivent retourner le code d’action d’envoi de la réponse de l' [**\_ authentificateur de méthode \_ \_ \_ EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) après la première phase de l’authentification (authentification d’homologue). Quand [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) est appelé, il doit retourner un [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket) valide avec un code EAP de [**EapCodeSuccess**](/windows/win32/api/eapmethodtypes/ne-eapmethodtypes-eapcode).
-   Les méthodes d’authentificateur LEAP doivent retourner le code d’action du résultat de la réponse de l' [**\_ authentificateur de méthode \_ \_ \_ EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) si la première phase de l’authentification d’homologue échoue.
-   Les méthodes d’authentificateur LEAP doivent retourner le paquet de réponse d’authentification final avec le code d’action du [](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) résultat de la réponse de l' [**authentificateur de \_ méthode \_ \_ \_ EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) lorsque EapMethodAuthenticatorSendPacket est appelé. Ensuite, dans les appels suivants à [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) , le **\_ \_ descripteur de session EAP** doit être retourné pour identifier la session authentifiée.
-   

### <a name="leap-peer-method-implementation"></a>Implémentation de la méthode d’homologue LEAP

Lors du développement d’une méthode pair LEAP, vérifiez les points suivants :

-   Les méthodes pair LEAP doivent retourner le code d’action [**EapPeerMethodResponseActionSend**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) après la réussite de la première phase de l’authentification (authentification d’homologue).
-   Les méthodes pair LEAP doivent retourner le code d’action [**EapPeerMethodResponseActionResult**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) après la réussite de la deuxième phase de l’authentification.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquence d’appel EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Utilisation d’EAPHost](using-eap-host.md)
</dt> </dl>

 

 




