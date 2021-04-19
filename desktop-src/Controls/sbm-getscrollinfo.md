---
title: Message SBM_GETSCROLLINFO (winuser. h)
description: Le \_ message SBM GETSCROLLINFO est envoyé pour récupérer les paramètres d’une barre de défilement.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510786"
---
# <a name="sbm_getscrollinfo-message"></a>\_Message SBM GETSCROLLINFO

Le message **SBM \_ GETSCROLLINFO** est envoyé pour récupérer les paramètres d’une barre de défilement.

Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollInfo** fonctionne correctement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Avant d’appeler [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), définissez le membre **cbSize** de la structure sur **sizeof**(**SCROLLINFO**) et définissez le membre **fmask** pour spécifier les paramètres de barre de défilement à récupérer. Avant de retourner, le message copie les paramètres spécifiés dans les membres appropriés de la structure.

Le membre **fmask** peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                      | Signification                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**SIF \_ tout**</dt> </dl>                | Combinaison de la \_ page SIF, de SIF \_ pos, de la \_ plage SIF et de SIF \_ TRACKPOS.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_page SIF**</dt> </dl>             | Copie la page de défilement dans le membre nPage.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**\_pos SIF**</dt> </dl>                | Copie la position de défilement dans le membre nPos. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**\_plage SIF**</dt> </dl>          | Copie la plage de défilement vers les membres nMin et nMax. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**\_TRACKPOS SIF**</dt> </dl> | Copie la position actuelle du suivi de la case de défilement dans le membre nTrackPos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message a récupéré des valeurs, la valeur de retour est **true**. Sinon, la **valeur est false**.

## <a name="remarks"></a>Notes

Les messages qui indiquent la position de la barre de défilement, [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md), fournissent uniquement 16 bits de données de position. Toutefois, la structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) utilisée par **SBM \_ GETSCROLLINFO**, [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md), [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)et [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fournit 32 bits de données de position de la barre de défilement. Vous pouvez utiliser ces messages et ces fonctions lors du traitement des messages **WM \_ HSCROLL** ou **WM \_ VSCROLL** pour obtenir les données de position de la barre de défilement 32 bits.

Pour obtenir la position 32 bits de la case de défilement (Thumb) au cours d’un \_ Code de demande SB THUMBTRACK dans un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) , envoyez **\_ GETSCROLLINFO SBM** avec la \_ valeur d’TRACKPOS SIF dans le membre **fmask** de la structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Le message retourne la position de suivi de la case de défilement dans le membre **nTrackPos** de la structure **SCROLLINFO** . Cela vous permet d’afficher la position de la case de défilement lorsque l’utilisateur la déplace. Vous pouvez également utiliser la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) pour récupérer les mêmes informations.

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

[**\_SETSCROLLINFO SBM**](sbm-setscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

