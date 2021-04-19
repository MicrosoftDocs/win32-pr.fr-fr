---
title: Message SBM_SETSCROLLINFO (winuser. h)
description: Le \_ message SBM SETSCROLLINFO est envoyé pour définir les paramètres d’une barre de défilement.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518096"
---
# <a name="sbm_setscrollinfo-message"></a>\_Message SBM SETSCROLLINFO

Le message **SBM \_ SETSCROLLINFO** est envoyé pour définir les paramètres d’une barre de défilement.

Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollInfo** fonctionne correctement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie si la barre de défilement est redessinée pour refléter la nouvelle position de la case de défilement. Si ce paramètre a la **valeur true**, la barre de défilement est redessinée. Si la **valeur est false**, la barre de défilement n’est pas redessinée.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Avant d’appeler [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), définissez le membre **cbSize** de la structure sur **sizeof**(**SCROLLINFO**), définissez le membre **fmask** pour indiquer les paramètres à définir et spécifiez les nouvelles valeurs de paramètre dans les membres appropriés.

Le membre **fmask** peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                           | Signification                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL SIF**</dt> </dl> | Désactive la barre de défilement au lieu de la supprimer, si les nouveaux paramètres de la barre de défilement rendent la barre de défilement inutile.<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_page SIF**</dt> </dl>                                  | Définit la page de défilement sur la valeur spécifiée dans le membre **nPage** .<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**\_pos SIF**</dt> </dl>                                     | Définit la position de défilement sur la valeur spécifiée dans le membre **nPos** . <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**\_plage SIF**</dt> </dl>                               | Affecte à la plage de défilement la valeur spécifiée dans les membres **nMin** et **nmax** . <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour correspond à la position actuelle de la case de défilement.

## <a name="remarks"></a>Notes

Les messages qui indiquent la position de la barre de défilement, [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md), fournissent uniquement 16 bits de données de position. Toutefois, la structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) utilisée par [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)et [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fournit 32 bits de données de position de la barre de défilement. Vous pouvez utiliser ces messages et ces fonctions lors du traitement des messages **WM \_ HSCROLL** ou **WM \_ VSCROLL** pour obtenir les données de position de la barre de défilement 32 bits.

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

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**\_GETSCROLLINFO SBM**](sbm-getscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

