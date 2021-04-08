---
title: Message SBM_SETRANGE (winuser. h)
description: Le \_ message SBM SEtrange est envoyé pour définir les valeurs de position minimale et maximale pour le contrôle de barre de défilement.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- SBM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844193"
---
# <a name="sbm_setrange-message"></a>\_Message de DÉtrange SBM

Le message **SBM \_ SetRange** est envoyé pour définir les valeurs de position minimale et maximale pour le contrôle de barre de défilement.

Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollRange** fonctionne correctement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie la position de défilement minimale.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie la position de défilement maximale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**ComCtl32.dll version 5,0**: si la position de la case de défilement a changé, la valeur de retour est la position précédente de la case de défilement ; dans le cas contraire, il est égal à zéro.

**ComCtl32.dll version 6,0**: position actuelle de la case de défilement, qu’elle ait été modifiée ou non.

## <a name="remarks"></a>Notes

Les valeurs par défaut de la position minimale et maximale sont égales à zéro. La différence entre les valeurs spécifiées par les paramètres *wParam* et *lParam* ne doit pas être supérieure à MAXLONG.

Si les valeurs de position minimale et maximale sont égales, le contrôle de barre de défilement est masqué et, en fait, désactivé.

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

[**\_GETPOS SBM**](sbm-getpos.md)
</dt> <dt>

[**\_GETRANGE SBM**](sbm-getrange.md)
</dt> <dt>

[**\_SetPos SBM**](sbm-setpos.md)
</dt> <dt>

[**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)
</dt> </dl>

 

