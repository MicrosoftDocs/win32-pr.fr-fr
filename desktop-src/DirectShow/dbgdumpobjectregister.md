---
description: La fonction DbgDumpObjectRegister affiche des informations sur les objets actifs. Ignoré dans les builds de vente au détail.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: DbgDumpObjectRegister, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312401"
---
# <a name="dbgdumpobjectregister-function"></a>DbgDumpObjectRegister fonction)

La `DbgDumpObjectRegister` fonction affiche des informations sur les objets actifs. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Dans les versions Debug, la bibliothèque de débogage gère une liste d’objets actifs. La liste comprend tous les objets qui dérivent de [**CBaseObject**](cbaseobject.md), qui ont été créés par le module en cours et qui n’ont pas été détruits. Le constructeur **CBaseObject** et les méthodes de destructeur mettent à jour la liste.

Cette fonction génère plusieurs messages de mémoire de journal \_ . Au niveau de la journalisation 1, la fonction affiche uniquement le nombre total d’objets. Au niveau de la journalisation 2 ou supérieur, elle affiche une liste des objets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




