---
title: Message TB_GETIMAGELIST (commctrl. h)
description: Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans leur état par défaut. Un contrôle ToolBar utilise cette liste d’images pour afficher les boutons lorsqu’ils ne sont pas à chaud ou désactivés.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116766"
---
# <a name="tb_getimagelist-message"></a>TO \_ GETIMAGELIST message

Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans leur état par défaut. Un contrôle ToolBar utilise cette liste d’images pour afficher les boutons lorsqu’ils ne sont pas à chaud ou désactivés.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la liste d’images, ou **null** si aucune liste d’images n’est définie.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





