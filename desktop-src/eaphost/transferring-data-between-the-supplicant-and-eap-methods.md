---
title: Transfert de données entre le demandeur et les méthodes EAP
description: En savoir plus sur le transfert de données entre le demandeur et les méthodes EAP. Le transfert de données entre méthodes s’effectue à l’aide d’attributs EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382883"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Transfert de données entre le demandeur et les méthodes EAP

L’utilisation d’attributs EAP permet d’échanger des données entre les demandeurs et les méthodes EAP.

## <a name="attribute-consumption"></a>Consommation d’attribut

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consomme les attributs EAP transmis directement à la méthode EAP configurée. De même, les méthodes EAP sont gratuites pour retourner un code d’action qui indique au demandeur que les attributs sont disponibles et qu’il doit collecter les attributs à l’aide de [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).

Pour plus d'informations, consultez les rubriques ci-dessous.

-   [Codes d’action du demandeur d’homologue EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Codes de raison du demandeur d’homologue EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [Codes d’action de la méthode d’authentificateur EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Les demandeurs sont censés ignorer les attributs qu’ils ne reconnaissent pas ou ne peuvent pas agir. À l’aide de [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) , ces attributs ignorés sont renvoyés à EAPHost et à la méthode EAP.

## <a name="vendor-specific-attributes"></a>Attributs spécifiques au fournisseur

À l’aide de l’attribut EAP spécifique au fournisseur, les méthodes et les demandeurs EAP peuvent intervenir dans l’échange de données à des fins spécifiques. Les attributs spécifiques au fournisseur sont ignorés par les demandeurs et les méthodes qui ne prennent pas en charge l’attribut propre au fournisseur.

Pour plus d'informations, consultez les rubriques ci-dessous.

-   [Attributs EAP](about-eap-attributes.md).
-   [**Protocole EAP \_ \_type d’attribut**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’interface utilisateur de la méthode EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Activation de stratégie de groupe](enabling-group-policy.md)
</dt> <dt>

[Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implémentation de la prise en charge NAP pour les méthodes EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Demandeurs EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




