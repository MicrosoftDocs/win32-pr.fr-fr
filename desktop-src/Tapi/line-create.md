---
description: Le \_ message de création de la ligne TAPI est envoyé pour informer l’application de la création d’un nouveau périphérique de ligne.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Message LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217780"
---
# <a name="line_create-message"></a>Créer un message de ligne \_

Le message **de \_ création** de la ligne TAPI est envoyé pour informer l’application de la création d’un nouveau périphérique de ligne.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
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

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les applications plus anciennes (qui ont négocié la version 1,3 de TAPI) reçoivent un message de [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) qui spécifie LINEDEVSTATE \_ rein, ce qui leur demande d’arrêter leur utilisation de l’API et d’appeler à nouveau [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) pour obtenir le nouveau nombre d’appareils. Toutefois, contrairement aux versions précédentes de TAPI, cette version ne requiert pas l’arrêt de toutes les applications avant d’autoriser la réinitialisation des applications. la réinitialisation peut avoir lieu immédiatement lors de la création d’un nouveau périphérique (l’arrêt complet est toujours nécessaire lorsqu’un fournisseur de services est supprimé du système).

Les applications prenant en charge TAPI version 1,4 ou ultérieure reçoivent un message de **\_ création de ligne** . Cela les informe de l’existence du nouvel appareil et de son nouvel identificateur d’appareil. L’application peut ensuite choisir s’il faut ou non essayer de travailler avec le nouvel appareil à loisir. Ce message est envoyé à toutes les applications prenant en charge cette version ou les versions ultérieures de l’API qui ont appelé [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), y compris celles qui n’ont pas d’appareils de ligne ouverts à ce moment-là.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEDEVSTATE de ligne \_**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




