---
title: Message WM_PASTE (winuser. h)
description: Une application envoie un \_ message de collage WM à un contrôle d’édition ou une zone de liste déroulante pour copier le contenu actuel du presse-papiers dans le contrôle d’édition à l’emplacement actuel du signe insertion. Les données sont insérées uniquement si le presse-papiers contient des données au \_ format de texte cf.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE des données de message Exchange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124498"
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

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Lorsqu’il est envoyé à une zone de liste déroulante, le message **WM \_ Paste** est géré par son contrôle d’édition. Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .

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

[**WM- \_ Clear**](wm-clear.md)
</dt> <dt>

[**\_copie WM**](wm-copy.md)
</dt> <dt>

[**découpe WM \_**](wm-cut.md)
</dt> <dt>

[**désannulation WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

