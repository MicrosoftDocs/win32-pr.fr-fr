---
description: En savoir plus sur la méthode de constructeur CMediaPosition. CMediaPosition (Ctlutil. h). Cette méthode utilise les paramètres « pName », « pUnk » et « PHR ».
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Constructeur CMediaPosition. CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106523864"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>CMediaPosition. CMediaPosition, constructeur (Ctlutil. h)-pName, pUnk, PHR, paramètres

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers le nom de l’objet, à des fins de débogage. Allouez ce paramètre dans la mémoire statique.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet, ou **null** si l’objet n’est pas agrégé.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Ctlutil. h (include streams. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaPosition, classe**](cmediaposition.md)
</dt> </dl>

 

 




