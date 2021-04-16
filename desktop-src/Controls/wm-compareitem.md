---
title: Message WM_COMPAREITEM (winuser. h)
description: Envoyé pour déterminer la position relative d’un nouvel élément dans la liste triée d’une zone de liste déroulante ou d’une zone de liste owner-drawn.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464239"
---
# <a name="wm_compareitem-message"></a>\_Message WM COMPAREITEM

Envoyé pour déterminer la position relative d’un nouvel élément dans la liste triée d’une zone de liste déroulante ou d’une zone de liste owner-drawn. Chaque fois que l’application ajoute un nouvel élément, le système envoie ce message au propriétaire d’une zone de liste déroulante ou d’une zone de liste créée avec le style de [**\_ Tri**](list-box-styles.md) [**CBS \_**](combo-box-styles.md) .


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’identificateur du contrôle qui a envoyé le message **WM \_ COMPAREITEM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**compareitemstruct,**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) qui contient les identificateurs et les données fournies par l’application pour deux éléments dans la zone de liste ou de liste déroulante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour indique la position relative des deux éléments. Il peut s’agir de l’une des valeurs répertoriées dans le tableau suivant.



| Code de retour                                                                          | Description                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Valeur**</dt> </dl> | Signification<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | L’élément 1 précède l’élément 2 dans l’ordre de tri.<br/>       |
| <dl> <dt>**0**</dt> </dl>     | Les éléments 1 et 2 sont équivalents dans l’ordre de tri.<br/> |
| <dl> <dt>**1**</dt> </dl>     | L’élément 1 suit l’élément 2 dans l’ordre de tri.<br/>        |



 

## <a name="remarks"></a>Notes

Lorsque le propriétaire d’une zone de liste déroulante ou d’une zone de liste owner-drawn reçoit ce message, le propriétaire retourne une valeur indiquant les éléments spécifiés par la structure [**compareitemstruct,**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) qui apparaîtront avant l’autre. En règle générale, le système envoie ce message plusieurs fois jusqu’à ce qu’il détermine la position exacte du nouvel élément.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement. La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**COMPAREITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

