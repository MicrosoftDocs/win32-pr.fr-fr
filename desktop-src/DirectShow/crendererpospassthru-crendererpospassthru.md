---
description: Méthode de constructeur.
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Constructeur CRendererPosPassThru. CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97b21ba3ad9438189f97c3e0bb9f011b210a0195
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534801"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a>Constructeur CRendererPosPassThru. CRendererPosPassThru

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
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

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Ignoré.

</dd> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée du filtre.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




