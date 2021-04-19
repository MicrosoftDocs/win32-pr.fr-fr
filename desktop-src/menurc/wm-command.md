---
title: Message WM_COMMAND (winuser. h)
description: Envoyé lorsque l’utilisateur sélectionne un élément de commande dans un menu, lorsqu’un contrôle envoie un message de notification à sa fenêtre parente, ou lorsqu’une touche d’accès rapide est traduite.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535298"
---
# <a name="wm_command-message"></a>\_Message de commande WM

Envoyé lorsque l’utilisateur sélectionne un élément de commande dans un menu, lorsqu’un contrôle envoie un message de notification à sa fenêtre parente, ou lorsqu’une touche d’accès rapide est traduite.


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pour obtenir une description de ce paramètre, consultez la section Notes.

</dd> <dt>

*lParam* 
</dt> <dd>

Pour obtenir une description de ce paramètre, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="example"></a>Exemple

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
Exemple tiré des [exemples Windows classiques](https://github.com/microsoft/Windows-classic-samples) sur GitHub.


## <a name="remarks"></a>Notes

L’utilisation des paramètres *wParam* et *lParam* est résumée ici.



| Source du message | wParam (mot élevé)                | wParam (mot bas)                | lParam                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| Menu           | 0                                 | Identificateur de menu (IDM \_ \* )        | 0                            |
| Accélérateur    | 1                                 | Identificateur d’accélérateur (IDM \_ \* ) | 0                            |
| Contrôler        | Code de notification défini par le contrôle | Identificateur de contrôle               | Handle vers la fenêtre de contrôle |



 

### <a name="menus"></a>Menus

Si une application active un séparateur de menu, le système envoie un message de **\_ commande WM** avec le mot de poids faible du paramètre *wParam* défini sur zéro lorsque l’utilisateur sélectionne le séparateur.

Si un menu est défini avec une valeur [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) de **MNS \_ NOTIFYBYPOS**, [**WM \_ MENUCOMMAND**](wm-menucommand.md) est envoyé à la place de la **\_ commande WM**.

### <a name="accelerators"></a>Accélérateurs

Les séquences de touches d’accélérateur qui sélectionnent des éléments dans le menu fenêtre sont traduites en messages [**WM \_ SYSCOMMAND**](wm-syscommand.md) .

Si une touche d’accès rapide qui correspond à un élément de menu se produit lorsque la fenêtre qui possède le menu est réduite, aucun message de **\_ commande WM** n’est envoyé. Toutefois, si une frappe de touche d’accès rapide ne correspond à aucun des éléments du menu de la fenêtre ou du menu fenêtre, un message de **\_ commande WM** est envoyé, même si la fenêtre est réduite.

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

[Menus](menus.md)
</dt> </dl>

 

