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
ms.openlocfilehash: fe3d5b60ed1990423d5ad9375ffdf192da313b8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312482"
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

## <a name="return-value"></a>Valeur de retour

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

 

 




