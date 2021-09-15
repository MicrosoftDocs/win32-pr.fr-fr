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
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312469"
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

## <a name="return-value"></a>Valeur de retour

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

 

 




