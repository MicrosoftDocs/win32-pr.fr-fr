---
description: obtient l’élément parent dans l’arborescence qui représente un périphérique matériel WIA (Windows Image Acquisition) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'IWiaItem2 :: GetParentItem, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7b3ab6763cac004cea2b70e77f3bd750a22aad1d3950e3fc26d7f33664a69f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450399"
---
# <a name="iwiaitem2getparentitem-method"></a>IWiaItem2 :: GetParentItem, méthode

obtient l’élément parent dans l’arborescence qui représente un périphérique matériel WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppIWiaItem2* \[ à\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) du parent de l’élément dans l’arborescence d’objets Item. Si cette méthode est appelée à la racine de l’arborescence, l’adresse retournée est **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

À partir de n’importe quel objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence d’objets d’un périphérique matériel WIA 2,0, l’application récupère un pointeur vers l’élément parent en appelant cette fonction.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* si ces pointeurs ne sont pas **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
