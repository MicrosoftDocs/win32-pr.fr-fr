---
description: Pointeur vers une fonction qui crée une instance de l’objet.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Pointeur de fonction LPFNNewCOMObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543251"
---
# <a name="lpfnnewcomobject-function-pointer"></a>Pointeur de fonction LPFNNewCOMObject

Pointeur vers une fonction qui crée une instance de l’objet.

## <a name="syntax"></a>Syntaxe


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnkOuter* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** de l’objet qui agrège le nouvel objet, le cas échéant. Ce pointeur peut avoir la **valeur null**.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Si le constructeur échoue, ce paramètre reçoit un code d’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers une nouvelle instance de l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>ComBase. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




