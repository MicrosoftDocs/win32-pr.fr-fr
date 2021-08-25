---
title: Message WM_GETDLGCODE (winuser. h)
description: Envoyé à la procédure de fenêtre associée à un contrôle.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Boîtes de dialogue de WM_GETDLGCODE message
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d9ef69c2a6e89154cd6d931e05f9e52b4c51b214319bca8dffa9f86786a3da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022189"
---
# <a name="wm_getdlgcode-message"></a>\_Message WM GETDLGCODE

Envoyé à la procédure de fenêtre associée à un contrôle. Par défaut, le système gère toutes les entrées au clavier du contrôle. le système interprète certains types d’entrée au clavier comme des touches de navigation de boîte de dialogue. Pour remplacer ce comportement par défaut, le contrôle peut répondre au message **WM \_ GETDLGCODE** pour indiquer les types d’entrée qu’il souhaite traiter lui-même.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

touche virtuelle, appuyée par l’utilisateur, qui vous invite Windows à émettre cette notification. Le gestionnaire doit gérer ces clés de manière sélective. Par exemple, le gestionnaire peut accepter et traiter **le \_ retour VK** mais **l' \_ onglet VK** délégué à la fenêtre propriétaire. Pour obtenir la liste des valeurs, consultez [**la section codes de clé virtuelle**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) (ou **null** si le système exécute une requête).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une ou plusieurs des valeurs suivantes, indiquant le type d’entrée traité par l’application.



| Code/valeur de retour                                                                                                                                                | Description                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_ BOUTON**</dt> <dt>0x2000</dt> </dl>          | Bouton.<br/>                                                                                                         |
| <dl> <dt>**DLGC \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt> </dl>   | Bouton de commande par défaut.<br/>                                                                                            |
| <dl> <dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt> </dl>       | [**Em \_ Messages SETSEL**](/windows/desktop/Controls/em-setsel) .<br/>                                                           |
| <dl> <dt>**DLGC \_ RadioButton**</dt> <dt>0x0040</dt> </dl>     | Case d’option.<br/>                                                                                                   |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0100</dt> statique </dl>          | Contrôle statique.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt> </dl> | Bouton de commande non défini par défaut.<br/>                                                                                        |
| <dl> <dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt> </dl>     | Toutes les entrées au clavier.<br/>                                                                                             |
| <dl> <dt>**DLGC \_ WANTARROWS**</dt> <dt>0x0001</dt> </dl>      | Touches de direction.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ WANTCHARS**</dt> <dt>0x0080</dt> </dl>       | [**WM \_ Messages de type CHAR**](/windows/desktop/inputdev/wm-char) .<br/>                                                                      |
| <dl> <dt>**DLGC \_ WANTMESSAGE**</dt> <dt>0x0004</dt> </dl>     | Toutes les entrées au clavier (l’application transmet ce message dans la structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) au contrôle).<br/> |
| <dl> <dt>**DLGC \_ WANTTAB**</dt> <dt>0x0002</dt> </dl>         | Touche TAB.<br/>                                                                                                        |



 

## <a name="remarks"></a>Remarques

Bien que la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne toujours la valeur zéro en réponse au message **WM \_ GETDLGCODE** , la procédure de fenêtre pour les classes de contrôle prédéfinies retourne un code approprié pour chaque classe.

Le message **WM \_ GETDLGCODE** et les valeurs retournées sont utiles uniquement avec les contrôles de boîte de dialogue définis par l’utilisateur ou les contrôles standard modifiés par le sous-classement.

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

[**\_SETSEL em**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**FRAGMENT**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**\_caractère WM**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> </dl>

 

