---
title: Message WM_PASTE (winuser. h)
description: Une application envoie un \_ message de collage WM à un contrôle d’édition ou une zone de liste déroulante pour copier le contenu actuel du presse-papiers dans le contrôle d’édition à l’emplacement actuel du signe insertion. Les données sont insérées uniquement si le presse-papiers contient des données au \_ format de texte cf.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385095"
---
# <a name="wm_paste-message"></a>\_Message de collage WM

Une application envoie un message de **\_ Collage WM** à un contrôle d’édition ou une zone de liste déroulante pour copier le contenu actuel du presse-papiers dans le contrôle d’édition à l’emplacement actuel du signe insertion. Les données sont insérées uniquement si le presse-papiers contient des données au format de [**\_ texte CF**](standard-clipboard-formats.md) .


```C++
#define WM_PASTE                        0x0302
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

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Lorsqu’il est envoyé à une zone de liste déroulante, le message **WM \_ Paste** est géré par son contrôle d’édition. Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .

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

[**\_copie WM**](wm-copy.md)
</dt> <dt>

[**découpe WM \_**](wm-cut.md)
</dt> <dt>

[**désannulation WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

