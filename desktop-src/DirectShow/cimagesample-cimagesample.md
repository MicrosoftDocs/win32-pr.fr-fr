---
description: Méthode constructeur CImageSample. CImageSample.
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
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239142"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageSample, classe**](cimagesample.md)
</dt> </dl>

 

 




