---
title: Message d’WM_PSD_PAGESETUPDLG (COMMDLG. h)
description: Notifie une procédure de hook PagePaintHook que la boîte de dialogue mise en page est sur le le présent pour dessiner le contenu de la page d’exemple. La procédure de raccordement peut utiliser ce message pour effectuer des tâches d’initialisation liées au dessin du contenu de la page d’exemple.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Boîtes de dialogue de WM_PSD_PAGESETUPDLG message
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d775bdeae029ff1657ce33bfb564a651bdee4fbce19ad79431dda2d6036bd0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787409"
---
# <a name="wm_psd_pagesetupdlg-message"></a>\_ \_ Message PAGESETUPDLG WM

Notifie une procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que la boîte de dialogue **mise en page** est sur le le présent pour dessiner le contenu de la page d’exemple. La procédure de raccordement peut utiliser ce message pour effectuer des tâches d’initialisation liées au dessin du contenu de la page d’exemple.


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie une valeur qui indique le format du papier. Cette valeur peut être l’une des **valeurs \_ DMPAPER** indiquées dans la description de la structure. Le mot de poids fort spécifie l’orientation du papier ou de l’enveloppe, et indique si l’imprimante est un appareil matricielle ou en HPPCL (Hewlett Packard Printer Control Language). Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                             | Signification                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>0x0001</dt> </dl> | Papier en mode paysage (matricielle)<br/>    |
| <dl> <dt>0x0003</dt> </dl> | Papier en mode paysage (en HPPCL)<br/>         |
| <dl> <dt>0x0005</dt> </dl> | Papier en mode Portrait (matricielle)<br/>     |
| <dl> <dt>0x0007</dt> </dl> | Papier en mode Portrait (en HPPCL)<br/>          |
| <dl> <dt>0x000b</dt> </dl> | Enveloppe en mode paysage (en HPPCL)<br/>      |
| <dl> <dt>0x000d</dt> </dl> | Enveloppe en mode Portrait (matricielle)<br/>  |
| <dl> <dt>0x0019</dt> </dl> | Enveloppe en mode paysage (matricielle)<br/> |
| <dl> <dt>0x001f</dt> </dl> | Enveloppe en mode Portrait (en HPPCL)<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) qui contient des informations utilisées pour initialiser la boîte de dialogue **mise en page** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue n’envoie plus de messages et ne dessine pas dans la page d’exemple tant que le système n’a pas besoin de redessiner la page d’exemple.

Si la procédure de hook retourne la **valeur false**, la boîte de dialogue envoie les messages restants de la séquence de dessin.

## <a name="remarks"></a>Remarques

La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée. Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple. Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.

Les trois premiers messages d’une séquence de dessin (**WM \_ PSD \_ PAGESETUPDLG**, [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)ou [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) fournissent des informations que la procédure de raccordement peut utiliser pour dessiner le contenu de la page d’exemple. Les messages restants ([**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md), [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notifient à la procédure de hook que la boîte de dialogue est sur le point de dessiner une partie spécifique de la page d’exemple. Cela permet à la procédure de raccordement de dessiner des parties de la page d’exemple de manière sélective.

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

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**\_ENVSTAMPRECT WM \_**](wm-psd-envstamprect.md)
</dt> <dt>

[**\_FULLPAGERECT WM \_**](wm-psd-fullpagerect.md)
</dt> <dt>

[**\_GREEKTEXTRECT WM \_**](wm-psd-greektextrect.md)
</dt> <dt>

[**\_MARGINRECT WM \_**](wm-psd-marginrect.md)
</dt> <dt>

[**\_MINMARGINRECT WM \_**](wm-psd-minmarginrect.md)
</dt> <dt>

[**\_YAFULLPAGERECT WM \_**](wm-psd-yafullpagerect.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

