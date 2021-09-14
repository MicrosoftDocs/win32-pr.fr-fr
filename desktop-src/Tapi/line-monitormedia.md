---
description: Le message d’LINE_MONITORMEDIA TAPI est envoyé lorsqu’une modification du type de média d’appels est détectée. L’envoi de ce message est contrôlé à l’aide de la fonction lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Message LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217708"
---
# <a name="line_monitormedia-message"></a>\_Message MONITORMEDIA de ligne

Le message **\_ MONITORMEDIA de ligne** TAPI est envoyé lorsqu’une modification est détectée dans le type de média de l’appel. L’envoi de ce message est contrôlé à l’aide de la fonction [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .


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

Nouveau type de média (ou mode). Ce paramètre doit être une et une seule des [**\_ constantes LINEMEDIAMODE**](linemediamode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

« nombre de cycles » (nombre de millisecondes depuis Windows démarré) auquel le média spécifié a été détecté. Pour les versions TAPI antérieures à 2,0, ce paramètre n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ MONITORMEDIA** est envoyé à l’application qui a activé la surveillance du média pour le type de média détecté.

Étant donné que cet horodateur peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour la comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements). Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.

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

[**MONITORDIGITS de ligne \_**](line-monitordigits.md)
</dt> <dt>

[**MONITORTONE de ligne \_**](line-monitortone.md)
</dt> </dl>

 

 




