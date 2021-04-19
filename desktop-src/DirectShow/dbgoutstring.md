---
description: La fonction DbgOutString envoie une chaîne à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: DbgOutString, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542550"
---
# <a name="dbgoutstring-function"></a>DbgOutString fonction)

La fonction **DbgOutString** envoie une chaîne à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*psz* 
</dt> <dd>

Chaîne à sortir.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Dans les versions Debug, cette fonction génère toujours la chaîne, indépendamment des niveaux de sortie de débogage actuels. Pour un contrôle plus fin de la sortie, utilisez la macro [**DbgLog**](dbglog.md) .

## <a name="examples"></a>Exemples


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




