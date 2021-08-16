---
title: Message TB_GETPRESSEDIMAGELIST (commctrl. h)
description: Obtient la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans un état appuyé.
ms.assetid: 116d4212-48ea-4b00-a752-21e5e1f10e36
keywords:
- TB_GETPRESSEDIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34093db3899205249fce934335e7aefa6393bc5bc588c8e797400e9359d9c54e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829660"
---
# <a name="tb_getpressedimagelist-message"></a>TO \_ GETPRESSEDIMAGELIST message

Obtient la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans un état appuyé.

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

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images, ou **null** si aucune liste d’images n’est définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





