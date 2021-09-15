---
description: Une application envoie le \_ message WM MDICREATE à une fenêtre cliente d’interface multidocument (MDI) pour créer une fenêtre enfant MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Message WM_MDICREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522149"
---
# <a name="wm_mdicreate-message"></a>\_Message WM MDICREATE

Une application envoie le message **WM \_ MDICREATE** à une fenêtre cliente d’interface multidocument (MDI) pour créer une fenêtre enfant MDI.


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) contenant des informations que le système utilise pour créer la fenêtre enfant MDI.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HWND**

Si le message est correctement exécuté, la valeur de retour est le handle de la nouvelle fenêtre enfant.

Si le message échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

La fenêtre enfant MDI est créée avec le [**style de fenêtre**](window-styles.md) bits **WS \_ Child**, **WS \_ CLIPSIBLINGS**, **WS \_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** et **WS \_ MAXIMIZEBOX**, ainsi que les bits de style supplémentaires spécifiés dans la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . Le système ajoute le titre de la nouvelle fenêtre enfant au menu fenêtre de la fenêtre frame. Une application doit utiliser ce message pour créer toutes les fenêtres enfants de la fenêtre cliente.

Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants alors que la fenêtre enfant active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.

Quand une fenêtre enfant MDI est créée, le système envoie le message [**WM \_ Create**](wm-create.md) à la fenêtre. Le paramètre *lParam* du message **WM \_ Create** contient un pointeur vers une structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . Le membre *lpCreateParams* de cette structure contient un pointeur vers la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) passée avec le message **WM \_ MDICREATE** qui a créé la fenêtre enfant MDI.

Une application ne doit pas envoyer un deuxième message **WM \_ MDICREATE** lorsqu’un message **WM \_ MDICREATE** est toujours en cours de traitement. Par exemple, il ne doit pas envoyer de message **WM \_ MDICREATE** lorsqu’une fenêtre enfant MDI traite son message **WM \_ MDICREATE** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**création de WM \_**](wm-create.md)
</dt> <dt>

[**\_MDIDESTROY WM**](wm-mdidestroy.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 
