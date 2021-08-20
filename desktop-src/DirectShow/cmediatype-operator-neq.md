---
description: Cet opérateur vérifie l’inégalité entre les objets CMediaType.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: 'CMediaType. CMediaType :: Operator ! =, méthode (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c17db60821be2f5243afab83ed62ec9b5b5b50e5d7a3f500d159ec185260a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156237"
---
# <a name="cmediatypecmediatypeoperator-method"></a>CMediaType. CMediaType :: Operator ! =, méthode

Cet opérateur vérifie l’inégalité entre les objets [**CMediaType**](cmediatype.md) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à l’objet **CMediaType** à comparer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si *RT* n’est pas égal à cet objet. Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




