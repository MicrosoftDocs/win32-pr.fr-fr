---
title: Message TB_SETBITMAPSIZE (commctrl. h)
description: Définit la taille des images bitmap à ajouter à une barre d’outils.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- TB_SETBITMAPSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2a26dacd63c00d1dd793163facce0ab4a45302e85dde11522f8844977eb0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167972"
---
# <a name="tb_setbitmapsize-message"></a>TO \_ SETBITMAPSIZE message

Définit la taille des images bitmap à ajouter à une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la largeur, en pixels, des images bitmap. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la hauteur, en pixels, des images bitmap.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La taille ne peut être définie qu’avant l’ajout de bitmaps à la barre d’outils. Si une application ne définit pas explicitement la taille de la bitmap, la taille par défaut est de 16 par 15 pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

