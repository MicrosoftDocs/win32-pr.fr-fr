---
description: 'Permet au rappel de modifier les valeurs de CFM \_ xxx passées à IContextMenu :: QueryContextMenu.'
title: Message DFM_MODIFYQCMFLAGS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62ce86426b31abfb6dec67d7ee45b01a8bc47ba10c40ce9ed00051dd414a0ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223589"
---
# <a name="dfm_modifyqcmflags-message"></a>\_Message DFM MODIFYQCMFLAGS

Permet au rappel de modifier les valeurs de CFM \_ xxx passées à [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*puNewFlags* \[ dans\]
</dt> <dd>

Pointeur vers les nouvelles valeurs d’indicateur.

</dd> <dt>

*uFlags* \[ dans\]
</dt> <dd>

Indicateurs qui spécifient comment le menu contextuel peut être modifié. Ce paramètre utilise les \_ valeurs CMF xxx décrites dans [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




