---
description: La méthode GetVideoPaletteEntries récupère une plage d’entrées de palette pour la vidéo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Méthode CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5eb1c017353ed3e5095f5ee5d24870773c11211c14eaa44a673b4f12913c56c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057039"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>Méthode CBaseControlVideo. GetVideoPaletteEntries

La `GetVideoPaletteEntries` méthode récupère une plage d’entrées de palette pour la vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartIndex* 
</dt> <dd>

Entrée de la palette de démarrage de base zéro.

</dd> <dt>

*Écritures* 
</dt> <dd>

Nombre d’entrées requises.

</dd> <dt>

*pRetrieved* 
</dt> <dd>

Pointeur vers le nombre de couleurs obtenues.

</dd> <dt>

*pPalette* 
</dt> <dd>

Pointeur vers la mémoire tampon de sortie pour les couleurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur noerreur en cas de réussite, VFW \_ e \_ no \_ palette \_ disponible si les exemples vidéo n’ont pas de palette de couleurs, e \_ OUTOFMEMORY si la mémoire disponible est insuffisante, e \_ INVALIDARG si *startIndex* n’est pas valide ou \_ a la valeur false s’il n’y a aucune couleur dans la palette.

## <a name="remarks"></a>Remarques

Cette fonction membre retourne la palette actuelle de la vidéo sous la forme d’un tableau alloué par l’utilisateur. Pour rester cohérent, utilisez les membres de la structure Win32 **PaletteEntry** pour retourner les couleurs, plutôt que les membres de la structure **RGBQUAD** (même si le paramètre est **long**). La mémoire est allouée par l’appelant. par conséquent, il suffit de copier chacun à son tour. Déterminez que le nombre d’entrées demandées et le décalage de position de début sont valides. Si le nombre d’entrées est égal à zéro, retourne un \_ faux code.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




