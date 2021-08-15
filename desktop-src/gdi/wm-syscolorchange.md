---
description: Le \_ message WM SYSCOLORCHANGE est envoyé à toutes les fenêtres de niveau supérieur quand une modification est apportée à un paramètre de couleur système.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Message WM_SYSCOLORCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e39ff8b5189da1a4cf48b7f6923c1cf12e8f30aa20fb26457d54a3f01d1b5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118483098"
---
# <a name="wm_syscolorchange-message"></a>\_Message WM SYSCOLORCHANGE

Le message **WM \_ SYSCOLORCHANGE** est envoyé à toutes les fenêtres de niveau supérieur quand une modification est apportée à un paramètre de couleur système.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le système envoie un message de [**\_ peinture WM**](wm-paint.md) à toute fenêtre affectée par une modification de couleur système.

Les applications qui ont des pinceaux utilisant les couleurs système existantes doivent supprimer ces pinceaux et les recréer à l’aide des nouvelles couleurs système.

Les fenêtres de niveau supérieur qui utilisent des contrôles communs doivent transférer le message **WM \_ SYSCOLORCHANGE** aux contrôles ; sinon, les contrôles ne sont pas notifiés de la modification de la couleur. Cela garantit que les couleurs utilisées par vos contrôles communs sont cohérentes avec celles utilisées par d’autres objets de l’interface utilisateur. Par exemple, un contrôle ToolBar utilise la couleur « objets 3D » pour dessiner ses boutons. Si l’utilisateur modifie la couleur des objets 3D mais que le message **WM \_ SYSCOLORCHANGE** n’est pas transféré à la barre d’outils, les boutons de la barre d’outils restent dans leur couleur d’origine, tandis que la couleur des autres boutons du système change.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des couleurs](colors.md)
</dt> <dt>

[Messages de couleur](color-messages.md)
</dt> <dt>

[**\_peinture WM**](wm-paint.md)
</dt> </dl>

 

 
