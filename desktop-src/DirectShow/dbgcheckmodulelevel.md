---
description: La fonction DbgCheckModuleLevel vérifie si la journalisation est activée pour les types de messages et le niveau donnés. Ignoré dans les builds de vente au détail.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: DbgCheckModuleLevel, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537875"
---
# <a name="dbgcheckmodulelevel-function"></a>DbgCheckModuleLevel fonction)

La `DbgCheckModuleLevel` fonction vérifie si la journalisation est activée pour les types de messages et le niveau donnés. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
BOOL DbgCheckModuleLevel(
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

Niveau de journalisation

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la journalisation de l’un des types de messages spécifiés est définie au niveau spécifié ou supérieur. Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




