---
description: Récupère le handle du appbar de masquage automatique associé à un bord de l’écran. Ce message étend ABM \_ GETAUTOHIDEBAR en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.
title: Message ABM_GETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982970"
---
# <a name="abm_getautohidebarex-message"></a>\_Message ABM GETAUTOHIDEBAREX

Récupère le handle du appbar de masquage automatique associé à un bord de l’écran. Ce message étend [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui spécifie le bord d’écran et le moniteur. Vous devez spécifier les membres **cbSize**, **uEdge** et **RC** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du appbar de masquage automatique. La valeur de retour est **null** si une erreur se produit ou si aucun appbar de masquage automatique n’est associé au bord donné du moniteur donné.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




