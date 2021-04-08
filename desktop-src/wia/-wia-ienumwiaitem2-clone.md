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
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752869"
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

## <a name="remarks"></a>Notes

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnum* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
