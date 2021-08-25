---
description: Le message de suppression de téléphone TAPI \_ est envoyé pour informer une application de la suppression (suppression du système) d’un appareil téléphonique.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Message PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26be60c55b16d0126d0b3be107a95af17dd490c9329343bb27ac6496403d46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773899"
---
# <a name="phone_remove-message"></a>Message de suppression de téléphone \_

Le message **de \_ Suppression de téléphone** TAPI est envoyé pour informer une application de la suppression (suppression du système) d’un appareil téléphonique. En général, cela n’est pas utilisé pour les suppressions temporaires, telles que l’extraction d’appareils PCMCIA, mais uniquement pour les suppressions permanentes dans lesquelles l’appareil n’est plus signalé par le fournisseur de services si l’interface TAPI a été réinitialisée.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificateur du périphérique téléphonique qui a été supprimé.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Les applications TAPI version 2,0 ou ultérieure reçoivent un message de **\_ Suppression de téléphone** . Cela les informe que l’appareil a été supprimé du système. Le message de **\_ Suppression de téléphone** est précédé d’un message de [**\_ fermeture de téléphone**](phone-close.md) sur chaque descripteur téléphonique, si l’application a ouvert le téléphone. Ce message est envoyé à toutes les applications prenant en charge TAPI version 2,0 ou ultérieure qui ont appelé [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), y compris celles qui n’ont pas d’appareils téléphoniques ouverts à ce moment-là.

Les applications plus anciennes (qui ont négocié la version 1,4 ou une version antérieure) reçoivent un message d' [**\_ État de téléphone**](phone-state.md) spécifiant PHONESTATE \_ supprimé, suivi d’un message de [**\_ fermeture du téléphone**](phone-close.md) . Contrairement au message de **\_ Suppression de téléphone** , toutefois, ces anciennes applications ne peuvent recevoir ces messages que si elles ont ouvert le téléphone lorsqu’elles sont supprimées. Si le téléphone n’est pas ouvert, leur seule indication que l’appareil a été supprimé recevrait un \_ NODEVICE PHONEERR lorsqu’il tentera d’accéder à l’appareil.

Une fois qu’un appareil a été supprimé, toute tentative d’accès à l’appareil par son identificateur d’appareil entraîne une \_ erreur PHONEERR nodevice. Une fois que toutes les applications TAPI ont été arrêtées afin que l’interface TAPI puisse redémarrer et, lorsque l’interface TAPI est réinitialisée, l’appareil supprimé n’occupe plus d’identificateur d’appareil.

> [!Note]  
> Implémentation : TAPI qui retourne ce \_ message PHONEERR nodevice après \_ réception d’un message de suppression de téléphone d’un fournisseur de services ; aucun autre appel n’est effectué à ce fournisseur de services à l’aide de cet identificateur de périphérique téléphonique.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Fermer le téléphone**](phone-close.md)
</dt> <dt>

[**État du téléphone \_**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




