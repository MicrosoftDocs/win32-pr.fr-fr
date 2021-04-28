---
description: SMC_GETSFOBJECT message-demande un pointeur vers un objet spécifié.
title: Message SMC_GETSFOBJECT (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 612b43c193cd1919db4a5cf9dba3a8fdba1c81c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086607"
---
# <a name="smc_getsfobject-message"></a>\_Message SMC GETSFOBJECT

Demande un pointeur vers un objet spécifié.


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vaut* 
</dt> <dd>

IID associé à l’objet demandé.

</dd> <dt>

*va* 
</dt> <dd>

Pointeur void qui reçoit un pointeur vers l’interface demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK.

## <a name="remarks"></a>Notes 

Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) . Il est similaire à [**SMC \_ GETOBJECT**](smc-getobject.md) , mais est utilisé pour les éléments de dossier shell. Créez l’objet demandé et assignez un pointeur vers l’interface demandée à *va*.

Les interfaces suivantes peuvent être demandées.

-   [**IStream**](/windows/win32/api/objidl/nn-objidl-istream)
-   [**IShellMenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**IShellMenuCallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 
