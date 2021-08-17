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
ms.openlocfilehash: b6d8b74b5f0643f619a58beeea2dcd5526889d1a65de4815b06d2d6047777d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821557"
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

## <a name="remarks"></a>Remarques

Dans les versions Debug, cette fonction génère toujours la chaîne, indépendamment des niveaux de sortie de débogage actuels. Pour un contrôle plus fin de la sortie, utilisez la macro [**DbgLog**](dbglog.md) .

## <a name="examples"></a>Exemples


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




