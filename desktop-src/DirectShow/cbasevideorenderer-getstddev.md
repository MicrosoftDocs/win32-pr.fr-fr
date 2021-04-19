---
description: La méthode GetStdDev évalue l’écart type en millisecondes entre le moment où chaque image est due et le moment où elle est réellement rendue, pour les statistiques par image.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Méthode CBaseVideoRenderer. GetStdDev (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523541"
---
# <a name="cbasevideorenderergetstddev-method"></a>Méthode CBaseVideoRenderer. GetStdDev

La `GetStdDev` méthode évalue l’écart type en millisecondes entre le moment où chaque image est due et le moment où elle est réellement rendue, pour les statistiques par image.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nSamples* 
</dt> <dd>

Valeur entière qui contient le nombre d’échantillons vidéo reçus par le convertisseur vidéo.

</dd> <dt>

*piResult* 
</dt> <dd>

Pointeur vers une valeur entière qui contiendra l’écart type.

</dd> <dt>

*llSumSq* 
</dt> <dd>

Valeur qui représente l’écart type, en millisecondes, de tous les échantillons vidéo rendus. Plus la valeur est faible, plus le rendu est cohérent.

</dd> <dt>

*iTot* 
</dt> <dd>

Valeur qui représente la valeur moyenne, en millisecondes, entre le temps horodaté et l’heure affichée pour tous les échantillons vidéo rendus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




