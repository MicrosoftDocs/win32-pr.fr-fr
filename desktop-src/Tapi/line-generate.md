---
description: Le \_ message de génération de la ligne TAPI est envoyé pour notifier l’application que la génération de chiffres ou de tonalités en cours a été arrêtée.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Message LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217713"
---
# <a name="line_generate-message"></a>Message de génération de ligne \_

Le message **de \_ génération** de la ligne TAPI est envoyé pour notifier l’application que la génération de chiffres ou de tonalités en cours a été arrêtée. Une seule demande de génération de ce type peut être en cours d’exécution d’un appel donné à tout moment. Ce message est également envoyé lorsque la génération d’un chiffre ou d’un ton est annulée.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’appel.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Raison pour laquelle la génération de chiffre ou de tonalité a été arrêtée. Ce paramètre doit être une et une seule des [**\_ constantes LINEGENERATETERM**](linegenerateterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

« tick count » (nombre de millisecondes depuis Windows démarré) auquel la génération de chiffre ou de tonalité est terminée. Pour les versions d’API antérieures à 2,0, ce paramètre n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **\_ génération de ligne** est envoyé uniquement à l’application qui a demandé la génération de chiffres ou de tonalités.

Étant donné que l’horodatage spécifié par *dwParam3* peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour effectuer une comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**ligne \_ MONITORDIGITS**](line-monitordigits.md), [**ligne \_ MONITORMEDIA**](line-monitormedia.md), [**ligne \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements). Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.

Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GATHERDIGITS de ligne \_**](line-gatherdigits.md)
</dt> <dt>

[**MONITORDIGITS de ligne \_**](line-monitordigits.md)
</dt> <dt>

[**MONITORMEDIA de ligne \_**](line-monitormedia.md)
</dt> <dt>

[**MONITORTONE de ligne \_**](line-monitortone.md)
</dt> </dl>

 

 




