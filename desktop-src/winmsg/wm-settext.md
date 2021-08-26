---
description: Définit le texte d’une fenêtre.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Message WM_SETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc2ab860fd89d726b9763c198fe8d58caa1376a3b919fd3587ad39a612d6667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055979"
---
# <a name="wm_settext-message"></a>\_Message WM SETTEXT

Définit le texte d’une fenêtre.


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne se terminant par null qui est le texte de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

La valeur de retour est **true** si le texte est défini. Il a la **valeur false** (pour un contrôle d’édition), **lb \_ ERRSPACE** (pour une zone de liste) ou **CB \_ ERRSPACE** (pour une zone de liste déroulante) si l’espace disponible est insuffisant pour définir le texte dans le contrôle d’édition. Il est **CB \_ Err** si ce message est envoyé à une zone de liste déroulante sans contrôle d’édition.

## <a name="remarks"></a>Remarques

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) définit et affiche le texte de la fenêtre. Pour un contrôle d’édition, le texte est le contenu du contrôle d’édition. Pour une zone de liste modifiable, le texte est le contenu de la partie de contrôle de modification de la zone de liste déroulante. Pour un bouton, le texte est le nom du bouton. Pour les autres fenêtres, le texte est le titre de la fenêtre.

Ce message ne modifie pas la sélection actuelle dans la zone de liste d’une zone de liste déroulante. Une application doit utiliser le message [**CB \_ SELECTSTRING**](../controls/cb-selectstring.md) pour sélectionner l’élément dans une zone de liste qui correspond au texte du contrôle d’édition.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**\_SELECTSTRING CB**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
