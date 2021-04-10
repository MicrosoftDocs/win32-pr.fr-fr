---
title: Séquence d’appel de l’API Supplier
description: En savoir plus sur la séquence d’appel de l’API Supplier. Consultez une vue d’ensemble de la séquence d’appel et affichez des ressources supplémentaires disponibles.
ms.assetid: 83276783-aee5-43ac-982d-1144df982a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c93afea6dbf4c3220bbeaec4f6278eb3d0b756
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941381"
---
# <a name="supplicant-api-call-sequence"></a>Séquence d’appel de l’API Supplier

Cette rubrique fournit la séquence d’appel spécifique pour l’API du demandeur.

## <a name="supplicant-api-call-sequence-overview"></a>Vue d’ensemble de la séquence d’appels d’API Supplier

Lorsque le demandeur reçoit un paquet EAP d’un fournisseur, tel qu’un point d’accès, le workflow d’appel d’API demandeur suivant se produit généralement.

-   L’application appelle [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) avec les données de configuration EAPHost et les données utilisateur. Un appel réussi retourne un handle de session de **\_ \_ handle de session EAP** .
-   Chaque paquet reçu par le demandeur est traité par un appel à [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket). Le demandeur appelle ensuite la fonction correspondant au code d’action retourné par la fonction.
-   Si le code d’action est **EapHostPeerResponseSend**, le demandeur appelle [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) pour obtenir la réponse à envoyer à l’authentificateur.
-   Si, au cours de la session, le code d’action renvoyé au demandeur est **EapHostPeerResponseRespond**, il indique que les attributs EAP sont disponibles. Le demandeur appelle ensuite [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) pour les obtenir. Ces attributs contiennent des données supplémentaires utilisées pendant le processus d’authentification. Une fois que le demandeur a terminé le traitement des attributs, il appelle [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) qui met à jour les données. Cette fonction retourne un code d’action qui détermine l’action suivante du demandeur.
-   Si le code d’action est **EapHostPeerResponseInvokeUI** , le demandeur déclenche une boîte de dialogue d’interface utilisateur pour obtenir des données interactives de l’utilisateur, telles que des informations d’identification ou des informations d’identité. Consultez interaction de l’utilisateur avec le processus d’appel d’API demandeur ci-dessous.
-   Si le code d’action est **EapHostPeerResponseResult**, cela signifie que les résultats de la session d’authentification sont disponibles pour le demandeur. Le demandeur appelle ensuite [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) pour obtenir les résultats. Que les résultats indiquent la réussite ou l’échec, le demandeur appelle [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession). En cas de défaillance, une nouvelle authentification peut être tentée en ouvrant une autre session avec EAPHost et en fournissant une nouvelle identité, ou en tentant à nouveau l’authentification avec l’identité d’origine.

## <a name="user-interaction-with-the-supplicant-api-call-flow"></a>Interaction de l’utilisateur avec le workflow d’appel d’API du demandeur

Dans certains cas, le demandeur doit obtenir des informations auprès de l’utilisateur pour poursuivre le processus d’authentification.

La liste suivante illustre la séquence d’appels sur le demandeur et le processus d’interface utilisateur EAPHost nécessaire pour activer l’entrée interactive.

1.  Le demandeur obtient le contexte de l’interface utilisateur actuel en appelant [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext).
2.  Le demandeur envoie ensuite les données de contexte de l’interface utilisateur au processus de l’interface utilisateur du demandeur.
    > [!Note]  
    > Le processus d’interface utilisateur, qui collecte généralement l’interface utilisateur ou gère l’interface utilisateur interactive, est distinct du processus du demandeur. La séparation des deux processus n’est pas une exigence d’EAPHost, mais cela présente l’avantage de permettre au processus de l’interface utilisateur d’interagir avec le bureau.

     

3.  Si le demandeur souhaite afficher l’interface utilisateur en soi, il appelle la fonction [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) pour obtenir les champs d’entrée des composants de l’interface utilisateur interactifs à déclencher. Dans le cas contraire, il suit le modèle traditionnel d’appel de l’interface utilisateur interactive de la méthode en appelant [ **EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)
    > [!Note]  
    > Si [**l' \_ opération EAP E \_ EAPHOST \_ méthode \_ \_ non \_ prise en charge**](eap-related-error-and-information-constants.md) est retournée, le demandeur doit suivre le modèle traditionnel d’appel de l’interface utilisateur interactive de la méthode en appelant [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui). En cas d’erreur, [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) retourne un code de retour autre que **null**.

     

4.  Si le demandeur appelle [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) ou [**EaphostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) , le processus d’interface utilisateur passe les données de contexte existantes et charge Eappcfg.dll. L’interface utilisateur appropriée est déclenchée pour collecter les nouvelles données. Les nouvelles données de contexte d’interface utilisateur, qui peuvent désormais contenir une entrée d’utilisateur, sont copiées et les anciennes données de contexte sont libérées avec un appel à [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory).
5.  Le processus d’interface utilisateur retourne les nouvelles données de contexte au demandeur, qui appelle [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) pour le définir.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquence d’appel de l’API de méthode homologue](peer-method-api-call-sequence.md)
</dt> <dt>

[Séquence d’appel de l’API de méthode d’authentificateur](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Séquence d’appel EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Demandeurs EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




