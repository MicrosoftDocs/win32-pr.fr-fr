---
description: Le message de suppression de ligne TAPI \_ est envoyé pour informer une application de la suppression (suppression du système) d’un périphérique en ligne.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Message LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541149"
---
# <a name="line_remove-message"></a>Message de suppression de ligne \_

Le message **de \_ Suppression de ligne** TAPI est envoyé pour informer une application de la suppression (suppression du système) d’un périphérique en ligne. En général, cela n’est pas utilisé pour les suppressions temporaires, telles que l’extraction d’appareils PCMCIA, mais uniquement pour les suppressions permanentes dans lesquelles l’appareil n’est plus signalé par le fournisseur de services si l’interface TAPI a été réinitialisée.


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

Identificateur du périphérique de ligne qui a été supprimé.

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

## <a name="remarks"></a>Notes

Les applications prenant en charge TAPI version 2,0 ou ultérieure reçoivent un message de **\_ Suppression de ligne** . Cela les informe que l’appareil a été supprimé du système. Le message de **\_ Suppression de ligne** est précédé d’un message de [**\_ fermeture de ligne**](line-close.md) sur chaque handle de ligne, si la ligne est ouverte dans l’application. Ce message est envoyé à toutes les applications prenant en charge TAPI version 2,0 ou ultérieure, appelées [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), y compris celles qui n’ont pas d’appareils de ligne ouverts à ce moment-là.

Les applications plus anciennes reçoivent un message de [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) en spécifiant LINEDEVSTATE \_ supprimé, suivi d’un message de fermeture de ligne \_ . Toutefois, contrairement au message de **\_ Suppression de ligne** , ces anciennes applications ne peuvent recevoir ces messages que si la ligne est ouverte lorsqu’elle est supprimée. S’ils n’ont pas de ligne ouverte, leur seule indication que l’appareil a été supprimé recevrait une \_ erreur LINEERR nodevice lorsqu’ils tenteront d’accéder à l’appareil.

Une fois qu’un appareil a été supprimé, toute tentative d’accès à l’appareil par son identificateur d’appareil entraîne une \_ erreur LINEERR nodevice. Une fois que toutes les applications TAPI ont été arrêtées afin que l’interface TAPI puisse redémarrer et, lorsque l’interface TAPI est réinitialisée, l’appareil supprimé n’occupe plus d’identificateur d’appareil.

> [!Note]  
> Implémentation : il s’agit de l’interface TAPI qui retourne ce LINEERR \_ nodevice ; après réception d’un message de **\_ Suppression de ligne** d’un fournisseur de services, aucun autre appel n’est effectué à ce fournisseur de services à l’aide de cet identificateur de périphérique de ligne.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**fermeture de ligne \_**](line-close.md)
</dt> <dt>

[**LINEDEVSTATE de ligne \_**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




