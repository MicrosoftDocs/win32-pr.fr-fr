---
title: FreeUiInfo, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à une structure UiInfo.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- FreeUiInfo fonction NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e2008ddabdb412c117a3cfac5f2eb5ebf1e722f5f3729fb7c8b2ee0c394c454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939046"
---
# <a name="freeuiinfo-function"></a>FreeUiInfo fonction)

La fonction **FreeUiInfo** libère la mémoire allouée en interne à une structure [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) . Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Type : **[ **UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\***

Structure. La mémoire allouée vers laquelle pointe cette structure sera libérée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

