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
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095837"
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

 

 




