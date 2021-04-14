---
title: Message WM_DELETEITEM (winuser. h)
description: Envoyé au propriétaire d’une zone de liste ou d’une zone de liste déroulante lorsque la zone de liste ou la zone de liste déroulante est détruite ou lorsque des éléments sont supprimés par le \_ message lb DELETESTRING, lb \_ RESETCONTENT, CB \_ DELETESTRING ou CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465146"
---
# <a name="wm_deleteitem-message"></a>\_Message WM DELETEITEM

Envoyé au propriétaire d’une zone de liste ou d’une zone de liste déroulante lorsque la zone de liste ou la zone de liste déroulante est détruite ou lorsque des éléments sont supprimés par le message [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)ou [**CB \_ RESETCONTENT**](cb-resetcontent.md) . Le système envoie un message **WM \_ DELETEITEM** pour chaque élément supprimé. Le système envoie le message **WM \_ DELETEITEM** pour tout élément de liste ou zone de liste déroulante supprimé avec des données d’élément non nulles.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’identificateur du contrôle qui a envoyé le message **WM \_ DELETEITEM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**deleteitemstruct,**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) qui contient des informations sur l’élément supprimé dans une zone de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner la **valeur true** si elle traite ce message.

## <a name="remarks"></a>Notes

Microsoft Windows NT et versions ultérieures : Windows envoie un message **WM \_ DELETEITEM** uniquement pour les éléments supprimés d’une zone de liste owner-drawn (avec le style [**\_ OWNERDRAWFIXED**](list-box-styles.md) ou [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) ) ou la zone de liste déroulante owner-drawn (avec le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) ou [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) ).

Windows 95 : Windows envoie le message **WM \_ DELETEITEM** pour tout élément de liste ou zone de liste déroulante supprimé avec des données d’élément non nulles.

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

[**\_DELETESTRING CB**](cb-deletestring.md)
</dt> <dt>

[**\_RESETCONTENT CB**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**\_DELETESTRING lb**](lb-deletestring.md)
</dt> <dt>

[**\_RESETCONTENT lb**](lb-resetcontent.md)
</dt> </dl>

 

 





