---
title: Message d’WM_PSD_YAFULLPAGERECT (COMMDLG. h)
description: Notifie la procédure de raccordement d’une boîte de dialogue de mise en page, PagePaintHook, que la boîte de dialogue est sur le de dessiner la partie adresse de retour d’une page d’exemple d’enveloppe.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- Boîtes de dialogue de WM_PSD_YAFULLPAGERECT message
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033213"
---
# <a name="wm_psd_yafullpagerect-message"></a>\_ \_ Message YAFULLPAGERECT WM

Notifie la procédure de raccordement d’une boîte de dialogue de **mise en page** , PagePaintHook, que la boîte de dialogue est sur le [](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)de dessiner la partie adresse de retour d’une page d’exemple d’enveloppe.


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le contexte de périphérique pour la page d’exemple.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées, en pixels, de la page d’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue ne dessine pas la partie adresse de retour d’une page d’exemple d’enveloppe.

Si la procédure de raccordement retourne la **valeur false**, la boîte de dialogue dessine la partie adresse de retour d’une page d’exemple d’enveloppe.

Si le type de papier n’est pas une enveloppe, la valeur de retour n’a aucun effet.

## <a name="remarks"></a>Notes

La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée. Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple. Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**\_PAGESETUPDLG WM \_**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

