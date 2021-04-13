---
title: Message WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Indique à une fenêtre de fournir une image bitmap statique à utiliser comme aperçu instantané (également appelé aperçu de lecture) de cette fenêtre.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Message de WM_DWMSENDICONICLIVEPREVIEWBITMAP Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465498"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>\_Message WM DWMSENDICONICLIVEPREVIEWBITMAP

Indique à une fenêtre de fournir une image bitmap statique à utiliser comme *aperçu instantané* (également appelé aperçu de *lecture*) de cette fenêtre.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Un *aperçu instantané* (également appelé *Aperçu avant impression*) d’une fenêtre s’affiche lorsqu’un utilisateur déplace le pointeur de la souris sur la miniature de la fenêtre dans la barre des tâches ou donne le focus de la miniature dans la fenêtre ALT + TAB. Cette vue est un aperçu complet de la fenêtre et peut être un instantané en direct ou une représentation sous forme.

Gestionnaire de fenêtrage (DWM) envoie ce message à une fenêtre si toutes les situations suivantes sont vraies :

-   L’aperçu instantané a été appelé dans la fenêtre.
-   [**DWMWA a l’attribut \_ \_ \_ bitmap sous forme**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) est défini dans la fenêtre.
-   Une représentation sous forme est la seule qui existe pour cette fenêtre.

La fenêtre qui reçoit ce message doit répondre en générant une image bitmap à l’échelle complète. La fenêtre appelle ensuite la fonction [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) pour définir l’aperçu instantané. Si la fenêtre ne définit pas de bitmap dans un laps de temps donné, DWM utilise sa propre représentation sous forme par défaut pour la fenêtre.

## <a name="examples"></a>Exemples

L’exemple suivant illustre une réponse au message **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP** . L’exemple appelle la fonction [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) avec un handle vers une image bitmap personnalisée indépendante du périphérique à utiliser comme représentation de la fenêtre.


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



Pour obtenir le code complet, consultez les exemples de [miniatures Customize a sous forme et Live Preview](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_DWMSENDICONICTHUMBNAIL WM**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





