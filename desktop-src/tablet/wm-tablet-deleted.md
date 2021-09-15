---
description: Le message de la \_ tablette WM \_ supprimée est publié lorsqu’un appareil tablette est supprimé de Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Message WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312865"
---
# <a name="wm_tablet_deleted-message"></a>Message de suppression de la \_ tablette WM \_

Le message de la **\_ tablette WM \_ supprimée** est publié lorsqu’un appareil tablette est supprimé de Windows.


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index du périphérique tablette en cours de suppression.

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



 

 
