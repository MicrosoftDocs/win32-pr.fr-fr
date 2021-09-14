---
description: Le \_ message de réponse du téléphone TAPI est envoyé à une application pour signaler les résultats de l’appel de fonction qui s’est terminé de façon asynchrone.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Message PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011079"
---
# <a name="phone_reply-message"></a>\_Message de réponse téléphonique

Le message **de \_ réponse du téléphone** TAPI est envoyé à une application pour signaler les résultats de l’appel de fonction qui s’est terminé de façon asynchrone.


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

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les fonctions qui exécutent de façon asynchrone renvoient une valeur d’identificateur de demande positive à l’application. Cet identificateur de demande est retourné avec le message de réponse pour identifier la demande qui a été effectuée. L’autre paramètre du message **de \_ réponse téléphonique** porte l’indication de réussite ou d’échec. Les erreurs possibles sont les mêmes que celles définies par la fonction correspondante. Ce message ne peut pas être désactivé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




