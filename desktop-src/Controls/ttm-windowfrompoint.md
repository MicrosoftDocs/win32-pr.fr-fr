---
title: Message TTM_WINDOWFROMPOINT (commctrl. h)
description: Permet à une procédure de sous-classe de faire en sorte qu’une info-bulle affiche du texte pour une fenêtre autre que celle située sous le curseur de la souris.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115769"
---
# <a name="ttm_windowfrompoint-message"></a>\_Message atténuation WINDOWFROMPOINT

Permet à une procédure de sous-classe de faire en sorte qu’une info-bulle affiche du texte pour une fenêtre autre que celle située sous le curseur de la souris.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**point**](/previous-versions//dd162805(v=vs.85)) qui définit le point à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est le handle de la fenêtre qui contient le point, ou **null** si aucune fenêtre n’existe au point spécifié.

## <a name="remarks"></a>Notes

Ce message est destiné à être traité par une application qui sous-classe une info-bulle. Elle n’est pas destinée à être envoyée par une application. Une info-bulle envoie ce message à lui-même avant d’afficher le texte d’une fenêtre. En modifiant les coordonnées du point spécifié par *lParam*, la procédure de sous-classe peut faire en sorte que l’info-bulle affiche du texte pour une fenêtre autre que celle située sous le curseur de la souris.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

