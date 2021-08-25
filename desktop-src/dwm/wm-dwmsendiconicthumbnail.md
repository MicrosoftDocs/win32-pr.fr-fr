---
title: Message WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Indique à une fenêtre de fournir une bitmap statique à utiliser comme représentation miniature de cette fenêtre.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Message de WM_DWMSENDICONICTHUMBNAIL Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3263f34cd59ba68ee895e5d5c77e297144cbadd6c8d8bbaa49ca6272248c2024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842649"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>\_Message WM DWMSENDICONICTHUMBNAIL

Indique à une fenêtre de fournir une bitmap statique à utiliser comme représentation miniature de cette fenêtre.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de cette valeur est la coordonnée x maximale de la miniature. Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est la coordonnée y maximale. Si une miniature a une dimension qui dépasse l’une des deux valeurs ou les deux, le DWM n’accepte pas la miniature.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

DWM envoie ce message à une fenêtre si toutes les situations suivantes sont vraies :

-   DWM affiche une représentation sous forme de la fenêtre.
-   [**DWMWA a l’attribut \_ \_ \_ bitmap sous forme**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) est défini dans la fenêtre.
-   La fenêtre n’a pas défini une image bitmap mise en cache.
-   Il y a de la place dans le cache pour une autre bitmap.

La fenêtre qui reçoit ce message doit répondre en générant une image bitmap qui n’est pas supérieure à la taille demandée dans les paramètres du message. La fenêtre appelle ensuite la fonction [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) pour remplacer la miniature par défaut. Si la fenêtre ne fournit pas de bitmap dans un laps de temps donné, DWM utilise sa propre représentation sous forme par défaut pour la fenêtre.

La fenêtre doit appartenir au processus appelant.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment répondre au message **WM \_ DWMSENDICONICTHUMBNAIL** . L’exemple appelle [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), avec un handle vers une image bitmap personnalisée indépendante du périphérique à utiliser comme représentation Windows.


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



Pour obtenir un exemple complet, consultez les exemples de [miniatures Customize a sous forme et Live Preview](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**\_DWMSENDICONICLIVEPREVIEWBITMAP WM**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

