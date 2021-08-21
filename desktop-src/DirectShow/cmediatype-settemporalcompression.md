---
description: La méthode SetTemporalCompression spécifie si les échantillons sont compressés à l’aide de la compression temporelle (intertrame).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Méthode CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29efb0ec16f99c7354621bc49bd36c4e367375d5eb68a2d94a69c27bfdce2f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954398"
---
# <a name="cmediatypesettemporalcompression-method"></a>Méthode CMediaType. SetTemporalCompression

La `SetTemporalCompression` méthode spécifie si les échantillons sont compressés à l’aide de la compression temporelle (intertrame).

## <a name="syntax"></a>Syntaxe


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bCompressed* 
</dt> <dd>

Valeur booléenne qui spécifie si le flux utilise la compression temporelle. Si le flux utilise la compression temporelle, définissez la valeur sur **true**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode définit le membre **bTemporalCompression** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




