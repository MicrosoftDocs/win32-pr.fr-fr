---
title: Message WM_MENUCHAR (winuser. h)
description: Envoyé lorsqu’un menu est actif et que l’utilisateur appuie sur une touche qui ne correspond à aucun mnémonique ou touche d’accès rapide. Ce message est envoyé à la fenêtre qui possède le menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743829"
---
# <a name="wm_menuchar-message"></a>\_Message WM MENUCHAR

Envoyé lorsqu’un menu est actif et que l’utilisateur appuie sur une touche qui ne correspond à aucun mnémonique ou touche d’accès rapide. Ce message est envoyé à la fenêtre qui possède le menu.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie le code de caractère qui correspond à la touche sur laquelle l’utilisateur a appuyé.

Le mot de poids fort spécifie le type de menu actif. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                 | Signification                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_**</dt> <dt>0x00000010L</dt> Popup </dl>       | Menu déroulant, sous-menu ou menu contextuel.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | Menu fenêtre.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers le menu actif.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application qui traite ce message doit retourner l’une des valeurs suivantes dans le mot de poids fort de la valeur de retour.



| Code/valeur de retour                                                                                                                                  | Description                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ FERMER**</dt> <dt>1</dt> </dl>   | Informe le système qu’il doit fermer le menu actif.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_ EXÉCUTER**</dt> <dt>2</dt> </dl> | Informe le système qu’il doit choisir l’élément spécifié dans le mot de poids faible de la valeur de retour. La fenêtre propriétaire reçoit un message de [**\_ commande WM**](wm-command.md) .<br/> |
| <dl> <dt>**MNC \_ IGNORER**</dt> <dt>0</dt> </dl>  | Informe le système qu’il doit ignorer le caractère que l’utilisateur a appuyé et créer un bref signal sonore sur le haut-parleur du système.<br/>                                                       |
| <dl> <dt>**MNC \_ SÉLECTIONNER**</dt> <dt>3</dt> </dl>  | Informe le système qu’il doit sélectionner l’élément spécifié dans le mot de poids faible de la valeur de retour. <br/>                                                                       |



 

## <a name="remarks"></a>Notes

Le mot de poids faible est ignoré si le mot de poids fort contient 0 ou 1.

Une application doit traiter ce message lorsqu’un accélérateur est utilisé pour sélectionner un élément de menu qui affiche une image bitmap.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

 

