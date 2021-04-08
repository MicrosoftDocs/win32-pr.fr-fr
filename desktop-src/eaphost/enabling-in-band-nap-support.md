---
title: Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP
description: Peut être activé pour les méthodes EAP EAPHost qui prennent en charge la transmission d’objets type-length-value (TLVs).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734613"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP

La prise en charge de la [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP) intrabande pour une méthode EAP peut être activée pour les méthodes EAP EAPHost qui prennent en charge la transmission d’objets TLVs (type-length-value). Lorsque la prise en charge de la protection d’accès réseau intrabande est activée, les paquets NAP sont transportés dans les paquets de méthode EAP.

En revanche, lorsque la prise en charge de la protection d’accès réseau hors bande est activée, l’échange [de déclaration d’intégrité](https://go.microsoft.com/fwlink/p/?linkid=83917) NAP se produit par le biais d’autres paquets de méthode internes aux protocoles EAP.

Tous les TLVs sont spécifiques au fournisseur.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implémentation de la prise en charge NAP sur les méthodes homologues EAP

L’implémentation de la méthode d’homologue EAP reçoit un TLV contenant la requête [de déclaration d’intégrité](https://go.microsoft.com/fwlink/p/?linkid=83917) TLV d’un serveur EAP.

L’implémentation de la méthode d’homologue EAP transmet ensuite la TLV contenant la requête SoH TLV à EAPHost comme suit.

-   L’implémentation de la méthode d’homologue EAP retourne le code d’action [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) à EAPHost au retour de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost appelle [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) à partir de l’implémentation de la méthode d’homologue EAP. Les attributs sont passés dans le processus.
-   L’implémentation de la méthode d’homologue EAP retourne la méthode TLV contenant la méthode TLV de demande SoH dans [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Les attributs sont reçus dans le processus.

L’implémentation de la méthode d’homologue EAP reçoit un TLV contenant un TLV SoH d’EAPHost comme suit.

-   EAPHost appelle [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) à partir de l’implémentation de la méthode d’homologue EAP. **EapPeerSetResponseAttributes** contient un TLV qui héberge un TLV SOH.
-   L’implémentation de la méthode d’homologue EAP envoie le TLV SoH au serveur EAP.
-   L’implémentation de la méthode d’homologue EAP reçoit un TLV contenant un TLV de réponse SoH à partir du serveur EAP.

L’implémentation de la méthode d’homologue EAP transmet la TLV contenant le TLV de réponse SoH à EAPHost comme suit.

-   L’implémentation de la méthode d’homologue EAP retourne le code d’action **EapPeerMethodResponseActionRespond** à EAPHost au retour de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost appelle [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) à partir des implémentations de la méthode d’homologue EAP. La structure des [**\_ attributs EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) est passée dans le processus.
-   L’implémentation de la méthode d’homologue EAP retourne la méthode TLV contenant le TLV de réponse SoH dans [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> Le membre **eapType** de la structure d' [**\_ attribut EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) aura toujours la valeur **eatEAPTLV** et le membre **pValue** pointera vers le premier octet de la TLV qui contient le TLV réponse SOH.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implémentation de la prise en charge NAP sur les méthodes de serveur EAP

L’implémentation de la méthode de serveur EAP construit un TLV contenant une requête SoH TLV. L’implémentation de la méthode de serveur EAP envoie ce TLV contenant la requête SoH TLV à l’homologue EAP. L’implémentation de la méthode de serveur EAP reçoit le TLV de l’homologue EAP.

L’implémentation de la méthode de serveur EAP transmet la TLV contenant un TLV SoH à EAPHost comme suit.

-   L’implémentation de la méthode de serveur EAP retourne le code d’action réponse de l' **\_ authentificateur de méthode EAP \_ \_ \_ répondre** à EAPHost au retour de [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).
-   EAPHost appelle [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) à partir de l’implémentation de la méthode de serveur EAP.
-   L’implémentation de la méthode de serveur EAP retourne la méthode TLV contenant la TLV SoH dans [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

L’implémentation de la méthode de serveur EAP reçoit un TLV contenant un TLV de réponse SoH d’EAPHost comme suit.

-   EAPHost appelle [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) à partir de l’implémentation de la méthode de serveur EAP.
-   La TLV contenant le TLV de réponse SoH est retournée dans [ **EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   L’implémentation de la méthode de serveur EAP envoie le TLV contenant le TLV de réponse SoH.

> [!Note]  
> Le membre **eapType** de la structure d' [**\_ attribut EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) aura toujours la valeur **eatEAPTLV** et le membre **pValue** pointera vers le premier octet de la TLV qui contient le TLV réponse SOH.

 

### <a name="messages"></a>Messages

EAP SoH TLV est utilisé pour encapsuler le protocole SoH en vue d’une transmission via une méthode EAP. Toutes les TLVs de déclaration d’intégrité EAP ont la même structure, qui diffère uniquement par l’ID de message et la partie de données du message.

Pour plus d’informations, consultez [messages de déclaration d’intégrité de la protection d’accès réseau (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’interface utilisateur de la méthode EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Activation de stratégie de groupe](enabling-group-policy.md)
</dt> <dt>

[Implémentation de la prise en charge NAP pour les méthodes EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transfert de données entre le demandeur et les méthodes EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Demandeurs EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 