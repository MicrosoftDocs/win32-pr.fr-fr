---
title: Implémentation de la prise en charge NAP pour les méthodes EAP
description: Découvrez comment implémenter la prise en charge de la protection d’accès réseau pour un demandeur EAPHost. Consultez les rubriques relatives à la protection d’accès réseau (NAP) de EAPHost et consultez les ressources disponibles supplémentaires.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00860057baeedbfdbae1939ab402db6f28fd74bd
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812390"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implémentation de la prise en charge NAP pour les méthodes EAP

Cette rubrique explique comment implémenter la protection d’accès réseau pour un demandeur EAPHost. dans Windows Vista et Windows Server 2008, un Client de contrainte de mise en conformité nap est disponible pour les connexions authentifiées [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .

## <a name="implementing-network-access-protection-nap"></a>Implémentation de la protection d’accès réseau (NAP)

Pour prendre en charge la protection d’accès réseau (NAP), un demandeur EAPHost implémente une fonction de rappel correspondant au prototype de rappel [**NotificationHandler**](/previous-versions/windows/desktop/api) et doit fournir un pointeur vers cette fonction de rappel lors de l’appel de [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).

La fonction de rappel accepte deux paramètres.

-   GUID qui identifie de façon unique l’interface associée à l’authentification.
-   Pointeur VOID vers une structure de données opaque fournie par le demandeur.

EAPHost appellera la fonction de rappel fournie par le demandeur avec le GUID d’interface unique et le pointeur VOID lorsque l’état de mise en quarantaine de l’ordinateur change. Quand EAPHost appelle la fonction de rappel fournie par le demandeur, le demandeur répond en détachant la connexion réseau logique identifiée par le pointeur d’interface GUID/VOID et recommence l’authentification à l’aide de **EapHostPeerBeginSession**.

EAPHost peut appeler la fonction de rappel fournie par le demandeur à tout moment : avant, pendant une authentification active ou une fois l’authentification terminée (après l’appel de [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) mais pas avant l’appel de [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ). Le demandeur doit toujours répondre en détachant la connexion réseau logique et en réauthentifiant.

Si le demandeur s’arrête ou si vous choisissez de ne plus recevoir de notification des modifications d’état d’isolement, le demandeur doit appeler [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) et spécifier le GUID d’interface approprié. Si le demandeur souhaite déterminer l’isolation de la connexion réseau logique, le demandeur peut obtenir ces informations à partir de **EapHostPeerMethodResult. isolationState** lorsque le [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) est obtenu à partir de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).

## <a name="eaphost-related-nap-information"></a>Informations NAP relatives à EAPHost

Pour obtenir des informations sur l’API EAPHost, reportez-vous aux rubriques suivantes.

-   [**\_type d’attribut EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**\_erreur EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Forum aux questions sur le demandeur EAPHost](eaphost-supplicant-frequently-asked-questions.yml)
-   [**Propriétés de la méthode EAP**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Constantes d’informations et d’erreurs liées à EAP**](eap-related-error-and-information-constants.md)
-   [**État d’isolement \_**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Ressources supplémentaires


-   Pour obtenir la liste des ressources NAP, consultez [protection d’accès réseau](https://go.microsoft.com/fwlink/p/?linkid=84107).
-   Pour obtenir des informations sur la déclaration d’intégrité, voir [messages de déclaration d’intégrité (SoH) de la protection d’accès réseau (NAP](https://go.microsoft.com/fwlink/p/?linkid=83918)).
-   pour la page web du groupe de mise en réseau Enterprise et le blog, consultez [Protection d’accès réseau (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).
-   Pour obtenir des informations sur l’API NAP, consultez [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page).


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’interface utilisateur de la méthode EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Activation de stratégie de groupe](enabling-group-policy.md)
</dt> <dt>

[Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Transfert de données entre le demandeur et les méthodes EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Demandeurs EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 