---
description: La méthode SetFormat Initialise le bloc de format.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Méthode CMediaType. SetFormat (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99726a466b6bf273b654a5d459fa2391a75882f1adee64b981d91a514a988b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108449"
---
# <a name="cmediatypesetformat-method"></a>Méthode CMediaType. SetFormat

La `SetFormat` méthode initialise le bloc de format.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFormat* 
</dt> <dd>

Pointeur vers un bloc de mémoire qui contient le bloc de format.

</dd> <dt>

*length* 
</dt> <dd>

Longueur du bloc de format, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** si une erreur s’est produite.

## <a name="remarks"></a>Remarques

Cette méthode alloue de la mémoire pour le bloc de format et copie la mémoire tampon spécifiée par *pFormat* dans le nouveau bloc de format. Si le type de média contient déjà un bloc de format, l’ancien est libéré. La méthode définit également le membre **cbFormat** de la structure du **\_ \_ type de média am** .

Pour définir le type de format, appelez la méthode [**CMediaType :: SetFormatType**](cmediatype-setformattype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




