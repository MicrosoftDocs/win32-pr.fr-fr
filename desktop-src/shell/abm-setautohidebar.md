---
description: Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran. Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.
title: Message ABM_SETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d8db0a9cc692054f924aa66e90347c31351c9a29539d6e614af72af52ee627d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884849"
---
# <a name="abm_setautohidebar-message"></a>\_Message ABM SETAUTOHIDEBAR

Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran. Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.

> [!Note]  
> Pour inscrire ou désinscrire un appbar de masquage automatique sur un moniteur spécifique, utilisez [**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md).

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Affectez la valeur **true** au membre **lParam** pour inscrire appbar ou **false** afin d’annuler son inscription. Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge** et **lParam** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** si une erreur se produit ou si un appbar de masquage automatique est déjà inscrit pour le bord donné.

## <a name="remarks"></a>Remarques

Le système n’autorise qu’un seul appbar de masquage automatique pour chaque bord de l’écran. Cela est déterminé lorsque le membre **uEdge** de la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




