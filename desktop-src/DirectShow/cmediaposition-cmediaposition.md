---
description: En savoir plus sur la méthode de constructeur CMediaPosition. CMediaPosition (Ctlutil. h). Cette méthode utilise les paramètres’pName’et’pUnk'.
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: CMediaPosition. CMediaPosition, constructeur (Ctlutil. h)-pName, paramètres pUnk
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106535847"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>CMediaPosition. CMediaPosition, constructeur (Ctlutil. h)-pName, paramètres pUnk

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
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

 

 




