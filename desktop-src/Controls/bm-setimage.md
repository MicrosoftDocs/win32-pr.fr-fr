---
title: Message BM_SETIMAGE (winuser. h)
description: Associe une nouvelle image (icône ou bitmap) au bouton.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8948c73c04d3b01230a47ab91529764c9e20281e4f45803f71d82f59dedb14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674812"
---
# <a name="bm_setimage-message"></a>\_Message SETIMAGE BM

Associe une nouvelle image (icône ou bitmap) au bouton.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type d’image à associer au bouton. Ce paramètre peut prendre l’une des valeurs suivantes :

-   IMAGE \_ bitmap
-   icône d’IMAGE \_

</dd> <dt>

*lParam* 
</dt> <dd>

Handle (**HICON** ou **HBITMAP**) de l’image à associer au bouton.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle vers l’image précédemment associée au bouton, le cas échéant ; dans le cas contraire, la **valeur est null**.

## <a name="remarks"></a>Remarques

L’apparence du texte, une icône ou les deux sur un contrôle Button dépend de l' [**\_ icône BS**](button-styles.md) et des styles [**\_ bitmap BS**](button-styles.md) , et de l’appel ou non du message **\_ SETIMAGE BM** . Les résultats possibles sont les suivants :



| \_Icône BS ou \_ ensemble de bitmaps BS ? | BM \_ SETIMAGE appelé ? | Résultats              |
|-----------------------------|----------------------|---------------------|
| Oui                         | Oui                  | Afficher l’icône uniquement.     |
| Non                          | Oui                  | Affichez l’icône et le texte. |
| Oui                         | Non                   | Afficher uniquement le texte.     |
| Non                          | Non                   | Afficher le texte uniquement      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GETIMAGE de BM \_**](bm-getimage.md)
</dt> </dl>

 

 





