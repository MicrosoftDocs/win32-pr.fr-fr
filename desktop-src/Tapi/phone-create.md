---
description: Le \_ message de création de téléphone TAPI est envoyé pour informer les applications de la création d’un nouveau périphérique téléphonique.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Message PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542467"
---
# <a name="phone_create-message"></a>Message de création de téléphone \_

Le message **de \_ création de téléphone** TAPI est envoyé pour informer les applications de la création d’un nouveau périphérique téléphonique.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPhone* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam1* 
</dt> <dd>

*HDeviceID* de l’appareil nouvellement créé.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les applications qui ont négocié la version 1,3 reçoivent un message d' [**\_ État de téléphone**](phone-state.md) spécifiant PHONESTATE \_ rein, ce qui leur demande d’arrêter leur utilisation de l’API et d’appeler à nouveau [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) pour obtenir le nouveau nombre d’appareils. Toutefois, TAPI version 1,4 et versions ultérieures ne nécessitent pas l’arrêt de toutes les applications avant d’autoriser la réinitialisation des applications. la réinitialisation peut avoir lieu immédiatement lors de la création d’un nouveau périphérique.

Les applications prenant en charge TAPI version 1,4 ou ultérieure reçoivent un message de **\_ création de téléphone** . Cela les informe de l’existence du nouvel appareil et de son nouvel identificateur d’appareil. L’application peut ensuite choisir s’il faut ou non essayer de travailler avec le nouvel appareil à loisir.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**État du téléphone \_**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




