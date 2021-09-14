---
description: Le message GATHERDIGITS de ligne TAPI \_ est envoyé lorsque la demande de collecte de chiffres mise en mémoire tampon est terminée ou annulée. La mémoire tampon de chiffres peut être examinée une fois que le message a été reçu par l’application.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Message LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217700"
---
# <a name="line_gatherdigits-message"></a>\_Message GATHERDIGITS de ligne

Le message **\_ GATHERDIGITS de ligne** TAPI est envoyé lorsque la demande de collecte de chiffres mise en mémoire tampon est terminée ou annulée. La mémoire tampon de chiffres peut être examinée une fois que le message a été reçu par l’application.


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

Raison pour laquelle la collecte de chiffres s’est terminée. Ce paramètre doit être une et une seule des [**\_ constantes LINEGATHERTERM**](linegatherterm--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

le « nombre de cycles » (nombre de millisecondes depuis Windows démarré) à partir duquel la collecte des chiffres est terminée. Pour les versions TAPI antérieures à 2,0, ce paramètre n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ GATHERDIGITS** est envoyé à l’application qui a initié la collecte des chiffres sur l’appel à l’aide de [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).

Si la fonction [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) est utilisée pour annuler une requête précédente en vue de recueillir des chiffres, TAPI envoie un message de **ligne \_ GATHERDIGITS** avec *dwParam1* défini sur LINEGATHERTERM \_ Cancel à l’application, indiquant que la mémoire tampon spécifiée à l’origine contient les chiffres regroupés jusqu’à l’annulation.

Étant donné que l’horodatage spécifié par *dwParam3* peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour effectuer une comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements). Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.

Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.

> [!Note]  
> Lorsqu’une application appelle une opération asynchrone qui écrit des données dans la mémoire de l’application, l’application doit conserver cette mémoire disponible pour l’écriture jusqu’à la réception d’un message de [**\_ réponse**](line-reply.md) de ligne ou de **\_ GATHERDIGITS de ligne** .

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**générer la ligne \_**](line-generate.md)
</dt> <dt>

[**MONITORDIGITS de ligne \_**](line-monitordigits.md)
</dt> <dt>

[**MONITORMEDIA de ligne \_**](line-monitormedia.md)
</dt> <dt>

[**MONITORTONE de ligne \_**](line-monitortone.md)
</dt> <dt>

[**réponse de ligne \_**](line-reply.md)
</dt> <dt>

[**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




