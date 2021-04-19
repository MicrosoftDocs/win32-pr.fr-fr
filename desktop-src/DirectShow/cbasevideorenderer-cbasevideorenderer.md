---
description: Méthode de constructeur.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Constructeur CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532251"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Constructeur CBaseVideoRenderer. CBaseVideoRenderer

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RenderClass* 
</dt> <dd>

Identificateur de classe pour ce convertisseur.

</dd> <dt>

*pName* 
</dt> <dd>

Pointeur vers une description utilisée à des fins de débogage.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’objet propriétaire agrégé.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




