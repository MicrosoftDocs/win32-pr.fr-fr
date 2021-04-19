---
title: Message WM_INITDIALOG (winuser. h)
description: Envoyé à la procédure de boîte de dialogue immédiatement avant l’affichage d’une boîte de dialogue. Les procédures de boîte de dialogue utilisent généralement ce message pour initialiser des contrôles et effectuer d’autres tâches d’initialisation qui affectent l’apparence de la boîte de dialogue.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Boîtes de dialogue de WM_INITDIALOG message
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513621"
---
# <a name="wm_initdialog-message"></a>\_Message WM INITDIALOG

Envoyé à la procédure de boîte de dialogue immédiatement avant l’affichage d’une boîte de dialogue. Les procédures de boîte de dialogue utilisent généralement ce message pour initialiser des contrôles et effectuer d’autres tâches d’initialisation qui affectent l’apparence de la boîte de dialogue.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du contrôle qui doit recevoir le focus clavier par défaut. Le système affecte le focus clavier par défaut uniquement si la procédure de boîte de dialogue retourne la **valeur true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Données d’initialisation supplémentaires. Ces données sont passées au système en tant que paramètre *lParam* dans un appel à la [**fonction CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)ou [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) utilisée pour créer la boîte de dialogue. Pour les feuilles de propriétés, ce paramètre est un pointeur vers la structure [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) utilisée pour créer la page. Ce paramètre est égal à zéro si une autre fonction de création de boîte de dialogue est utilisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La procédure de la boîte de dialogue doit retourner **true** pour indiquer au système de définir le focus clavier sur le contrôle spécifié par *wParam*. Dans le cas contraire, elle doit retourner la **valeur false** pour empêcher le système de définir le focus clavier par défaut.

La procédure de boîte de dialogue doit retourner la valeur directement. La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

## <a name="remarks"></a>Notes

Le contrôle qui doit recevoir le focus clavier par défaut est toujours le premier contrôle dans la boîte de dialogue qui est visible, et non désactivé, et qui a le style **WS \_ TABSTOP** . Lorsque la procédure de la boîte de dialogue retourne la **valeur true**, le système vérifie le contrôle pour s’assurer que la procédure ne l’a pas désactivée. Si elle a été désactivée, le système définit le focus clavier sur le contrôle suivant qui est visible, non désactivé, et possède le paramètre **WS \_ TABSTOP**.

Une application ne peut retourner la **valeur false** que si elle a défini le focus clavier sur l’un des contrôles de la boîte de dialogue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

