---
description: Méthode de constructeur.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Constructeur CImageSample. CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540179"
---
# <a name="cimagesamplecimagesample-constructor"></a>Constructeur CImageSample. CImageSample

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAllocator* 
</dt> <dd>

Pointeur vers l’allocateur qui a créé cet exemple.

</dd> <dt>

*pName* 
</dt> <dd>

Ignoré.

</dd> <dt>

*phr* 
</dt> <dd>

Ignoré.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Pointeur vers une mémoire tampon allouée par l’appelant, de la *longueur* de la taille. La mémoire tampon doit contenir une image bitmap indépendante du périphérique (DIB) GDI.

</dd> <dt>

*length* 
</dt> <dd>

Longueur de la mémoire tampon.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe [**CImageAllocator**](cimageallocator.md) crée un DIB à l’aide d’un objet de mappage de fichiers qui est sauvegardé par le fichier de pagination du système d’exploitation. Le descripteur de l’objet de mappage de fichier est stocké dans le membre **hMapping** de la structure **m \_ DibData** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageSample, classe**](cimagesample.md)
</dt> </dl>

 

 




