---
description: Le \_ message MONITORTONE de ligne TAPI est envoyé lorsqu’un ton est détecté. L’envoi de ce message est contrôlé à l’aide de la fonction lineMonitorTones.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Message LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526447"
---
# <a name="line_monitortone-message"></a>\_Message MONITORTONE de ligne

Le message **\_ MONITORTONE de ligne** TAPI est envoyé lorsqu’un ton est détecté. L’envoi de ce message est contrôlé à l’aide de la fonction [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .


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

Membre **dwAppSpecific** spécifique à l’application de la structure [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) pour le ton détecté.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

« Nombre de cycles » (nombre de millisecondes écoulées depuis le démarrage de Windows) auquel le ton a été détecté. Pour les versions d’API antérieures à 2,0, ce paramètre n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ MONITORTONE** est envoyé uniquement à l’application qui a demandé l’analyse du ton.

Étant donné que cet horodateur peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour la comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), **line \_ MONITORTONE**), afin de déterminer leur minutage relatif (séparation entre les événements). Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.

Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.

## <a name="requirements"></a>Configuration requise



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

[**MONITORDIGITS de ligne \_**](line-monitordigits.md)
</dt> <dt>

[**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




