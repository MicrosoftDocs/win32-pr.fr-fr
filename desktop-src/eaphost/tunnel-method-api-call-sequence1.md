---
title: Tunnel Séquence d’appel de l’API de méthode
description: en savoir plus sur la séquence d’appel d’API pour Tunnel méthodes. Consultez une vue d’ensemble et affichez des ressources supplémentaires disponibles.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca32a889229b6cdbdb3f008ebea8b838f9b6d64fba36bc2a30c4ddd9d62ac83d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272790"
---
# <a name="tunnel-method-api-call-sequence"></a>Tunnel Séquence d’appel de l’API de méthode

cette rubrique couvre la séquence d’appels d’API pour les méthodes Tunnel

## <a name="tunnel-method-call-sequence-overview"></a>Tunnel Vue d’ensemble de la séquence d’appel de méthode

Lorsque le demandeur reçoit une demande pour l’identité de l’utilisateur et les données utilisateur, le workflow d’appel d’API suivant se produit généralement.

-   Le demandeur appelle EapHostPeerProcessReceivedPacket sur EapHost pour traiter le paquet reçu de l’authentificateur.
-   Lors du traitement de ce paquet, EAPHost le détermine comme paquet IdentityRequest et appelle [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sur la méthode de tunnel pour obtenir l’identité de l’utilisateur à utiliser pour l’authentification.
-   Si la méthode de tunnel doit obtenir l’identité de l’utilisateur à partir de la méthode interne, elle appelle [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) sur l’EAPHost interne, qui à son tour appelle [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sur la méthode interne.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Interaction de l’utilisateur avec l’appel d’API méthodes Tunnel Flow

Dans certains cas, lorsque l’identité n’est pas disponible, ou lorsque l’utilisateur doit fournir des informations supplémentaires, la méthode EAP génère une boîte de dialogue d’interface utilisateur sur le demandeur.

Dans ce cas, la séquence d’appel suivante se produit généralement pour recevoir des informations directement de l’utilisateur.

-   Tunnel La méthode EAP retourne le code d’action pour appeler l’interface utilisateur sur EapHost. Le demandeur appelle [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)pour obtenir les informations de contexte de l’interface utilisateur actuelle pour la boîte de dialogue de l’interface utilisateur.
-   Le demandeur appelle ensuite [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Cette fonction utilise les informations de contexte de l’interface utilisateur pour déclencher une interface utilisateur interactive qui est utilisée pour récupérer les informations d’identification de l’utilisateur. Le processus d’interface utilisateur charge Eappcfg.dll et obtient les pointeurs vers EapPeerInvokeInteractiveUI et EapPeerFreeMemory.
    > [!Note]  
    > Le processus d’interface utilisateur collecte généralement l’interface utilisateur ou gère l’interface utilisateur interactive et est séparé du processus du demandeur. La séparation des deux processus n’est pas une exigence d’EAPHost, mais cela présente l’avantage de permettre au processus de l’interface utilisateur d’interagir avec le bureau.

     

-   EapHost appelle [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sur la méthode de tunnel pour obtenir les informations d’identité de l’utilisateur.
-   Afin d’obtenir l’identité de l’utilisateur à partir de la méthode interne, la méthode de tunnel appelle [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) sur l’EAPHost interne.
-   L’interface EAPHost interne appelle [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sur la méthode interne pour appeler l’interface utilisateur de l’identité de l’utilisateur.
-   [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) fournit des informations de contexte d’interface utilisateur nouvelles ou mises à jour à la méthode d’homologue EAP chargée sur EAPHost après le déclenchement de l’interface utilisateur.

le diagramme suivant explique la séquence d’appels d’API pour les méthodes de Tunnel

![séquence d’appel de l’API méthodes de tunnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquence d’appel EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Séquence d’appel de l’API Supplier](supplicant-api-call-sequence.md)
</dt> <dt>

[Informations de référence sur l’API Supplier EAPHost](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




