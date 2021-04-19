---
description: La fonction DbgSetModuleLevel définit le niveau de journalisation pour un ou plusieurs types de messages. Ignoré dans les builds de vente au détail.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: DbgSetModuleLevel, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528108"
---
# <a name="dbgsetmodulelevel-function"></a>DbgSetModuleLevel fonction)

La fonction **DbgSetModuleLevel** définit le niveau de journalisation pour un ou plusieurs types de messages. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Types* 
</dt> <dd>

Combinaison d’opérations de bits d’un ou plusieurs types de messages.

</dd> <dt>

*Niveau* 
</dt> <dd>

Niveau de journalisation pour les types de messages spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




