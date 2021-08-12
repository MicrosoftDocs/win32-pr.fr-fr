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
ms.openlocfilehash: 101678ebcb851ef0fcdc8eeaa202435ca80eb796555c81e5e5d95eb4998131c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655260"
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
| En-tête | Ctlutil. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaPosition, classe**](cmediaposition.md)
</dt> </dl>

 

 




