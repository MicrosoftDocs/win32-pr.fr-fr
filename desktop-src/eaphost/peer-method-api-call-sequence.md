---
title: Séquence d’appel de l’API de méthode homologue
description: En savoir plus sur la séquence d’appels d’API de méthode homologue. Consultez une liste qui illustre la séquence des appels effectués par une EAPHost sur une méthode d’homologue EAP.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647a6a558d282ff4ae3691c23600b696b79764ee68a1007ccabb445c5a1fe65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042787"
---
# <a name="peer-method-api-call-sequence"></a>Séquence d’appel de l’API de méthode homologue

Cette rubrique fournit la séquence d’appel spécifique pour l’API de méthode homologue. Lors d’une session d’authentification EAP classique, EAPHost effectue un certain nombre d’appels sur les méthodes EAP pour implémenter l’API de méthode homologue EAPHost.

La liste suivante illustre la séquence d’appels effectuée par EAPHost sur une méthode d’homologue EAP.

-   Charge la DLL de méthode homologue EAP utilisée pour l’authentification.
-   Appelle [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) sur la méthode pour obtenir une liste de pointeurs vers des fonctions implémentées sur la dll. Les appels de fonction suivants par l’homologue EAPHost (client) sont supposés être implémentés sur la DLL.
-   Appelle [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) pour indiquer à la bibliothèque de méthodes EAP de préparer au moins une session d’authentification à l’aide de cette méthode homologue.
-   Appelle [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) pour établir une session d’authentification unique.
-   Appelle [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) pour obtenir l’identité à utiliser pour l’authentification. Si l’identité n’est pas disponible, ou si l’utilisateur doit fournir des informations supplémentaires, EAPHost appelle [ **EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Cette fonction obtient les informations de contexte pour la boîte de dialogue de l’interface utilisateur qui sera déclenchée sur le demandeur. Une fois que l’utilisateur a envoyé les informations d’identité, l’identité de l’utilisateur est définie avec un appel à [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)et est obtenue par un appel à **EapPeerGetIdentity**.
-   Répète les étapes suivantes jusqu’à ce que [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) indique qu’un résultat d’authentification est disponible.
    -   Appelle [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) avec le pointeur d’un paquet de demande à passer au demandeur.
    -   Appelle **EapPeerGetResponsePacket** pour récupérer le paquet de réponse à envoyer à l’authentificateur.
    -   Si vous le souhaitez, si les attributs EAP doivent être récupérés ou envoyés au cours de la session d’authentification, EAPHost appelle [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) et [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) respectivement.
-   Lorsque l’authentificateur envoie un code d’action qui indique que l’authentification est terminée, EAPHost appelle [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) et obtient les résultats de l’authentification.
-   Appelle [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) pour mettre fin à la session d’authentification.
-   Appelle [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) pour décharger la dll de méthode homologue.
-   Décharge la bibliothèque de méthodes EAP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquence d’appel de l’API Supplier](supplicant-api-call-sequence.md)
</dt> <dt>

[Authenticator Séquence d’appel de l’API de méthode](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Séquences d’appels EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




