---
title: Message WM_CHAR (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’un \_ message de KEYversion WM est traduit par la fonction TranslateMessage. Le \_ message WM char contient le code de caractère de la touche qui a été enfoncée.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 16f9f1160f9766bd6284f62f2203b940ab6336f326aa31a0d9fa2894d243cf59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247948"
---
# <a name="wm_char-message"></a>\_Message WM char

Publié dans la fenêtre qui a le focus clavier lorsqu’un message de [**\_ keyversion WM**](wm-keydown.md) est traduit par la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Le message **WM \_ char** contient le code de caractère de la touche qui a été enfoncée.


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de caractère de la clé.

</dd> <dt>

*lParam* 
</dt> <dd>

Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.



| Bits  | Signification                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions du message en cours. La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée. Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés. Toutefois, le nombre de répétitions n’est pas cumulatif. |
| 16-23 | Code d’analyse. La valeur dépend du fabricant d’ordinateurs OEM.                                                                                                                                                                                                                          |
| 24    | Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches. La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.                                                              |
| 25-28 | Réservé n’utilisez pas.                                                                                                                                                                                                                                                 |
| 29    | Code de contexte. La valeur est 1 si la touche ALT est maintenue enfoncée pendant que la touche est enfoncée ; dans le cas contraire, la valeur est 0.                                                                                                                                                     |
| 30    | État de la clé précédente. La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.                                                                                                                                                    |
| 31    | État de transition. La valeur est 1 si la touche est relâchée, ou 0 si la touche est enfoncée.                                                                                                                                                            |

Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Une application doit retourner zéro si elle traite ce message.

## <a name="example"></a>Exemple

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
exemple de [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) sur GitHub.

## <a name="remarks"></a>Notes

Le message **WM \_ char** utilise le format UTF (Unicode Transformation Format)-16.

Il n’existe pas nécessairement une correspondance un-à-un entre les touches enfoncées et les messages de caractères générés. par conséquent, les informations contenues dans le mot de poids fort du paramètre *lParam* ne sont généralement pas utiles aux applications. Les informations contenues dans le mot de poids fort ne s’appliquent qu’au dernier message de la [**\_ touche WM**](wm-keydown.md) qui précède la publication du message **WM \_ char** .

Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et droite de la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .

Le message [**WM \_ UNICHAR**](wm-unichar.md) est identique à **WM \_ char**, sauf qu’il utilise UTF-32. Il est conçu pour envoyer ou poster des caractères Unicode dans des fenêtres ANSI et peut gérer des caractères de plan supplémentaires Unicode.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM- \_ touche**](wm-keydown.md)
</dt> <dt>

[**\_UNICHAR WM**](wm-unichar.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

