---
description: L’interface TAPI envoie le \_ message d’État téléphonique à une application chaque fois que l’état d’un périphérique téléphonique change.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Message PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90003eaa67cb3384b123c62827fcf52bae524b1e20f9f14c2391c46dc89a367c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796759"
---
# <a name="phone_state-message"></a>Message d’état de téléphone \_

L’interface TAPI envoie le message d' **\_ État téléphonique** à une application chaque fois que l’état d’un périphérique téléphonique change.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPhone* 
</dt> <dd>

Handle vers l’appareil mobile.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.

</dd> <dt>

*dwParam1* 
</dt> <dd>

État du téléphone qui a changé. Ce paramètre utilise l’une des [**\_ constantes PHONESTATE**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Téléphone des informations dépendantes de l’état détaillant le changement d’état. Ce paramètre n’est pas utilisé si plusieurs indicateurs sont définis dans *dwParam1*, car plusieurs éléments d’État ont été modifiés. L’application doit appeler [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) pour obtenir un ensemble complet d’informations.

Si *dwParam1* est PHONESTATE \_ Owner, *dwParam2* contient le nouveau nombre de propriétaires.

Si *dwParam1* est PHONESTATE \_ Monitors, *dwParam2* contient le nouveau nombre d’analyses.

Si *dwParam1* est PHONESTATE \_ LAMP, *dwParam2* contient l’identificateur de bouton/lampe de la lampe qui a changé.

Si *dwParam1* est PHONESTATE \_ RINGMODE, *dwParam2* contient le nouveau mode Ring.

Si *dwParam1* est PHONESTATE \_ combiné, haut-parleur ou casque, *dwParam2* contient le nouveau mode hookswitch de cet appareil hookswitch. Ce paramètre utilise l’une des [**\_ constantes PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

L’envoi du message d' **\_ État téléphonique** à l’application peut être contrôlé et interrogé à l’aide de [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) et [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages). Par défaut, ce message est désactivé pour toutes les modifications d’État, à l’exception de PHONESTATE \_ reinit, qui ne peut pas être désactivé. Ce message est envoyé à toutes les applications qui ont un handle vers le téléphone, y compris celles qui ont appelé [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) avec le paramètre *DWPRIVILEGES* défini sur PHONEPRIVILEGE \_ owner ou PHONEPRIVILEGE \_ Monitor.

Un message d' **\_ État de téléphone** avec un propriétaire et/ou une indication d’analyse est envoyé aux applications qui ont déjà un handle pour le téléphone. Cela peut être le résultat d’une autre application modifiant la propriété ou la surveillance du périphérique téléphonique avec [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) ou [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Fermer le téléphone**](phone-close.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




