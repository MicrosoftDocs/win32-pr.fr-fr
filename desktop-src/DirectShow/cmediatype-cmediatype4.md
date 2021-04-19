---
description: Méthode de constructeur.
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
ms.openlocfilehash: a40929bb6f53df7ce721e20eefba3019eb71cb0e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106545723"
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

## <a name="remarks"></a>Notes

Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




