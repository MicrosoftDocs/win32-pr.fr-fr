---
title: DVD. isAvailable
description: La propriété isAvailable indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée. | DVD. isAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. isAvailable lecteur Windows Media
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522533"
---
# <a name="dvdisavailable"></a>DVD. isAvailable

La propriété **isAvailable** indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>Paramètres

*name*

**Chaîne** contenant l’une des valeurs suivantes.



| String     | Description                                                                            |
|------------|----------------------------------------------------------------------------------------|
| Retour       | Détermine si la méthode **Back** est disponible.                                   |
| DVD        | Détermine si le DVD est chargé.                                                  |
| dvdDecoder | Détermine si le décodeur DVD est installé sur le système.                             |
| resume     | Détermine si la méthode **Resume** est disponible.                                 |
| titleMenu  | Détermine si la méthode **titleMenu** est disponible.                              |
| Menu de la    | Détermine si la méthode de **menu** est disponible. Communément appelé menu racine. |



 

## <a name="return-values"></a>Valeurs de retour

Cette méthode retourne une **valeur booléenne** en lecture seule qui indique si le paramètre spécifié est disponible.

## <a name="remarks"></a>Notes

Les fonctionnalités DVD du lecteur Windows Media ne fonctionneront pas sur les ordinateurs sur lesquels aucun décodeur de DVD tiers n’est installé. Vous pouvez déterminer si un décodeur est disponible en appelant **isAvailable**(« dvdDecoder »).

Chaque DVD est créé différemment. Les méthodes disponibles pendant la lecture et la navigation sur DVD dépendent de la façon dont le DVD est créé.

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Version<br/>                  | Lecteur Windows Media pour Windows XP ou version ultérieure<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> </dl>

 

 





