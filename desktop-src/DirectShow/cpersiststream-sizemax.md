---
description: Récupère la taille maximale en octets nécessaire pour le flux actuel, à l’exclusion du numéro de version.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Méthode CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b8f2c547e75303e4c54a49651f2118a90768bc0f42161ee3dae0de9bec2dcad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813299"
---
# <a name="cpersiststreamsizemax-method"></a>Méthode CPersistStream. SizeMax

Récupère la taille maximale en octets nécessaire pour le flux actuel, à l’exclusion du numéro de version.

## <a name="syntax"></a>Syntaxe


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le nombre d’octets nécessaires pour les données, à l’exclusion du numéro de version.

## <a name="remarks"></a>Remarques

La version par défaut retourne zéro ; elle doit être substituée pour fournir une autre valeur appropriée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




