---
description: Le \_ \_ message ajouté à la tablette WM est publié lorsqu’un appareil tablette est ajouté à Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Message WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9c56b475eb63c292d2638d5a34b831862da967868944f823c90b184bdbc076a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934329"
---
# <a name="wm_tablet_added-message"></a>\_ \_ Message ajouté à la tablette WM

Le **message \_ \_ ajouté à la tablette WM** est publié lorsqu’un appareil tablette est ajouté à Windows.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index du périphérique tablette ajouté

</dd> <dt>

*lParam* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce message est envoyé à toutes les fenêtres de niveau supérieur du système, y compris les fenêtres sans propriétaire désactivées ou inactives, les fenêtres superposées et les fenêtres indépendantes. mais le message n’est pas envoyé aux fenêtres enfants.

Les index passés dans *wParam* sont liés à l’index utilisé par la méthode [**ITabletManager :: GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
