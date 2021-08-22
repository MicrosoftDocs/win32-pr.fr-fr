---
title: Message d’WM_PSD_GREEKTEXTRECT (COMMDLG. h)
description: Notifie la procédure de raccordement d’une boîte de dialogue de mise en page, PagePaintHook, que la boîte de dialogue est sur le de dessiner du texte grec à l’intérieur du rectangle de marge de la page d’exemple.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- Boîtes de dialogue de WM_PSD_GREEKTEXTRECT message
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30e4873255a59a86da91b3145d0675f6940ce35081273696ce6c68b70a1560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726049"
---
# <a name="wm_psd_greektextrect-message"></a>\_ \_ Message GREEKTEXTRECT WM

Notifie la procédure de raccordement d’une boîte de dialogue de **mise en page** , PagePaintHook, que la boîte de dialogue est sur le [](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)de dessiner du texte grec à l’intérieur du rectangle de marge de la page d’exemple.


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le contexte de périphérique pour la page d’exemple.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées, en pixels, du rectangle de texte grec.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue ne dessine pas la partie du texte grec de la page d’exemple.

Si la procédure de raccordement retourne la **valeur false**, la boîte de dialogue dessine la partie du texte grec de la page d’exemple.

## <a name="remarks"></a>Remarques

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

 

