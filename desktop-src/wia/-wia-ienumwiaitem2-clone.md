---
description: Crée une instance supplémentaire de l’interface IEnumWiaItem2 et retourne un pointeur vers celui-ci.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'IEnumWiaItem2 :: Clone, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 21c94c634a6930f28f48cdc35a4d3cf199b8fa33e9fb5f08444797fd76f50c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965848"
---
# <a name="ienumwiaitem2clone-method"></a>IEnumWiaItem2 :: Clone, méthode

Crée une instance supplémentaire de l’interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) et retourne un pointeur vers celui-ci.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppIEnum* \[ à\]
</dt> <dd>

Type : **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Reçoit l’adresse de l’instance d’interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que **IEnumWiaItem2 :: Clone** crée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnum* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
