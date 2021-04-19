---
description: Le \_ message de réponse de ligne TAPI est envoyé pour signaler les résultats des appels de fonction qui se sont terminés de façon asynchrone.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Message LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542762"
---
# <a name="line_reply-message"></a>Message de réponse de ligne \_

Le message **de \_ réponse de ligne** TAPI est envoyé pour signaler les résultats des appels de fonction qui se sont terminés de façon asynchrone.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Retourne l’instance de rappel de l’application.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificateur de demande pour lequel il s’agit de la réponse.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Indication de réussite ou d’erreur. L’application doit effectuer un cast de ce paramètre en LONG. Zéro indique une réussite ; un nombre négatif indique une erreur.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les fonctions qui exécutent de façon asynchrone renvoient une valeur d’identificateur de demande positive à l’application. Cet identificateur de demande est retourné avec le message de réponse pour identifier la demande qui a été effectuée. L’autre paramètre du message **de \_ réponse** à la ligne comporte l’indication de réussite ou d’échec. Les erreurs possibles sont les mêmes que celles définies par la fonction correspondante. Ce message ne peut pas être désactivé.

Dans certains cas, une application peut ne pas recevoir le message de **\_ réponse de ligne** correspondant à un appel à une fonction asynchrone. Cela se produit si la poignée d’appel correspondante est désallouée avant la réception du message.

> [!Note]  
> Lorsqu’une application appelle une opération asynchrone qui écrit des données dans la mémoire de l’application, l’application doit conserver cette mémoire disponible pour l’écriture jusqu’à la réception d’un message de **\_ réponse** de ligne ou de [**\_ GATHERDIGITS de ligne**](line-gatherdigits.md) .

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GATHERDIGITS de ligne \_**](line-gatherdigits.md)
</dt> </dl>

 

 




