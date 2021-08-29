---
description: LPFNNewCOMObject fonction pointeur pointeur vers une fonction qui crée une instance de l’objet.
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
ms.openlocfilehash: f589404cd2a4bf5ff42b331cdf48a978d97e9a274a5fc01a483c804f5878b3eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501949"
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
| En-tête<br/> | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




