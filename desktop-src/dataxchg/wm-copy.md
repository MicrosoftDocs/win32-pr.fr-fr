---
title: Message WM_COPY (winuser. h)
description: Une application envoie le \_ message de copie WM à un contrôle d’édition ou une zone de liste déroulante pour copier la sélection actuelle dans le presse-papiers au \_ format de texte cf.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY l’échange de données de message
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106542102"
---
# <a name="wm_copy-message"></a>\_Message de copie WM

Une application envoie le message de **\_ copie WM** à un contrôle d’édition ou une zone de liste déroulante pour copier la sélection actuelle dans le presse-papiers au format de [**\_ texte CF**](standard-clipboard-formats.md) .


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, sinon zéro.

## <a name="remarks"></a>Notes

Lorsqu’il est envoyé à une zone de liste déroulante, le message de **\_ copie WM** est géré par son contrôle d’édition. Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .

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

[**WM- \_ Clear**](wm-clear.md)
</dt> <dt>

[**découpe WM \_**](wm-cut.md)
</dt> <dt>

[**\_coller WM**](wm-paste.md)
</dt> <dt>

[**désannulation WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

