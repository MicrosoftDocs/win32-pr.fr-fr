---
description: Une application envoie le \_ message WM MDIMAXIMIZE à une fenêtre cliente d’interface multidocument (MDI) pour agrandir une fenêtre enfant MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Message WM_MDIMAXIMIZE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b187d4aed71d8582e4ea72686e30ee6339934a2bf6f5b4849fd8600c4a5552c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810509"
---
# <a name="wm_mdimaximize-message"></a>\_Message WM MDIMAXIMIZE

Une application envoie le message **WM \_ MDIMAXIMIZE** à une fenêtre cliente d’interface multidocument (MDI) pour agrandir une fenêtre enfant MDI. Le système redimensionne la fenêtre enfant pour que sa zone cliente remplisse la fenêtre cliente. Le système place l’icône de menu fenêtre de la fenêtre enfant à la position la plus à droite de la barre de menus de la fenêtre frame et place l’icône de restauration de la fenêtre enfant à la position la plus à gauche. Le système ajoute également le texte de la barre de titre de la fenêtre enfant à celle de la fenêtre frame.


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers la fenêtre enfant MDI à agrandir.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **zéro**

La valeur de retour est toujours zéro.

## <a name="remarks"></a>Remarques

Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants alors que la fenêtre enfant MDI active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.

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

[**\_MDIRESTORE WM**](wm-mdirestore.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




