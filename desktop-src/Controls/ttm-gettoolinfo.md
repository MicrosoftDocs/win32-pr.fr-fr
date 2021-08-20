---
title: Message TTM_GETTOOLINFO (commctrl. h)
description: Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- TTM_GETTOOLINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f19243603ab5d2ba62d498a5595528e39b33658c7a8e4aa0638888806684ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166372"
---
# <a name="ttm_gettoolinfo-message"></a>\_Message atténuation GETTOOLINFO

Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Lors de l’envoi du message, les membres **HWND** et **UID** identifient un outil et le membre **cbSize** doit spécifier la taille de la structure. Lorsque vous utilisez ce message pour récupérer le texte d’info-bulle, assurez-vous que le membre **lpszText** de la structure **TOOLINFO** pointe vers une mémoire tampon de taille adquate valide

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Si le contrôle ToolTip comprend l’outil, la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) reçoit des informations sur l’outil.

## <a name="examples"></a>Exemples

L’exemple suivant repositionne un contrôle ToolTip.


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ GETTOOLINFOW** (Unicode) et **atténuation \_ GETTOOLINFOA** (ANSI)<br/>           |



 

 





