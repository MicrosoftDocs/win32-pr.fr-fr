---
description: Récupère le handle du appbar de masquage automatique associé à un bord de l’écran. Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.
title: Message ABM_GETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412602"
---
# <a name="abm_getautohidebar-message"></a>\_Message ABM GETAUTOHIDEBAR

Récupère le handle du appbar de masquage automatique associé à un bord de l’écran. Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.

> [!Note]  
> Pour interroger un appbar de masquage automatique sur une analyse spécifique, utilisez [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui spécifie le bord d’écran. Vous devez spécifier les membres **cbSize** et **uEdge** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle du appbar de masquage automatique. La valeur de retour est **null** si une erreur se produit ou si aucun appbar de masquage automatique n’est associé au bord donné.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




