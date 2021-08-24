---
description: CMediaType. CMediaType, constructeur (mtype. h)-méthode constructeur.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: CMediaType. CMediaType, constructeur (mtype. h)-cmtype et PHR, paramètres
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f686d1338073c65ce3e5bc3871ae8f4a5b9102e78d7678d5bcf6f77a565397d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792949"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Constructeur CMediaType. CMediaType (mtype. h)

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cmtype* \[ Réf\]
</dt> <dd>

Référence à un `CMediaType` objet. Le constructeur copie le type de média vers le nouvel objet, y compris le bloc de format, le cas échéant.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur HRESULT. Ce paramètre peut être un pointeur **null** . Dans le cas contraire, l’appelant doit définir la valeur sur S \_ OK avant d’appeler le constructeur. Si le constructeur échoue, il définit la valeur sur un code d’échec.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




