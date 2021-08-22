---
description: Méthode constructeur CBaseVideoRenderer. CBaseVideoRenderer.
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
ms.openlocfilehash: ec6a5e12d12b12f22cf1089d85ed4c07656da86cda071d8645355890996e2cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954758"
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
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




