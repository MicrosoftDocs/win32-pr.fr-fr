---
description: Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran. Ce message étend ABM \_ SETAUTOHIDEBAR en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.
title: Message ABM_SETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996464"
---
# <a name="abm_setautohidebarex-message"></a>\_Message ABM SETAUTOHIDEBAREX

Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran. Ce message étend [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Affectez la valeur **true** au membre **lParam** pour inscrire appbar ou **false** afin d’annuler son inscription. Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge**, **RC** et **lParam** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** si une erreur se produit ou si un appbar de masquage automatique est déjà inscrit pour le bord donné sur l’analyse donnée.

## <a name="remarks"></a>Notes

Le système n’autorise qu’un seul appbar de masquage automatique pour chaque bord de chaque moniteur. Le moniteur est déterminé par le membre **RC** et le bord est déterminé par le membre **uEdge** de la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> </dl>

 

 




