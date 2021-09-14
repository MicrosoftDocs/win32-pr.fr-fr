---
description: 'Méthode CSourceSeeking. ConvertTimeFormat : la méthode ConvertTimeFormat convertit d’un format d’heure en un autre. Cette méthode implémente la méthode IMediaSeeking :: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Méthode CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923579"
---
# <a name="csourceseekingconverttimeformat-method"></a>Méthode CSourceSeeking. ConvertTimeFormat

La `ConvertTimeFormat` méthode convertit d’un format d’heure en un autre. Cette méthode implémente la méthode [**IMediaSeeking :: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTarget* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure convertie.

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

Pointeur vers le GUID du format cible. Si la **valeur est null**, le format actuel est utilisé. Consultez [**GUID de format d’heure**](time-format-guids.md).

</dd> <dt>

*Source* 
</dt> <dd>

Valeur de temps à convertir.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Pointeur vers le GUID du format d’heure du format à convertir. Si la **valeur est null**, le format actuel est utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                                  | Description                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Succès<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide<br/>          |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Notes

Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes). Cette méthode retourne E \_ INVALIDARG, sauf dans le cas trivial où *PTargetFormat* et *pSourceFormat* spécifient tous deux le temps de \_ format du \_ média \_ .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




