---
description: Le \_ message MONITORDIGITS de ligne TAPI est envoyé lors de la détection d’un chiffre. L’envoi de ce message est contrôlé à l’aide de la fonction lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Message LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217684"
---
# <a name="line_monitordigits-message"></a>\_Message MONITORDIGITS de ligne

Le message **\_ MONITORDIGITS de ligne** TAPI est envoyé lors de la détection d’un chiffre. L’envoi de ce message est contrôlé à l’aide de la fonction [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .


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

Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.

</dd> <dt>

*dwParam1* 
</dt> <dd>

L’octet de poids faible contient le dernier chiffre reçu dans une représentation textuelle.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Mode de chiffrement détecté. Ce paramètre doit être une et une seule des [**\_ constantes LINEDIGITMODE**](linedigitmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

« tick count » (nombre de millisecondes depuis Windows démarré) à partir duquel le chiffre spécifié a été détecté. Pour les versions TAPI antérieures à 2,0, ce paramètre n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ MONITORDIGITS** est envoyé à l’application qui a activé la surveillance des chiffres.

Étant donné que cet horodateur peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour la comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ generate**](line-generate.md), [**line \_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements). Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.

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

[**générer la ligne \_**](line-generate.md)
</dt> <dt>

[**MONITORMEDIA de ligne \_**](line-monitormedia.md)
</dt> <dt>

[**MONITORTONE de ligne \_**](line-monitortone.md)
</dt> <dt>

[**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




