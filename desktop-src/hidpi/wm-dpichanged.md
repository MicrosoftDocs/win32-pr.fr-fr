---
title: Message WM_DPICHANGED (WinUser. h)
description: Envoyé lorsque les points effectifs par pouce (dpi) d’une fenêtre ont été modifiés.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED message haute résolution
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120198"
---
# <a name="wm_dpichanged-message"></a>\_Message WM DPICHANGED

Envoyé lorsque les points effectifs par pouce (dpi) d’une fenêtre ont été modifiés. La résolution PPP est le facteur d’échelle d’une fenêtre. Plusieurs événements peuvent entraîner la modification de la résolution PPP. La liste suivante indique les causes possibles de la modification de PPP.

-   La fenêtre est déplacée vers une nouvelle analyse qui a une résolution différente.
-   La résolution du moniteur qui héberge la fenêtre change.

La valeur PPP actuelle d’une fenêtre est toujours égale à la dernière DPI envoyée par **WM \_ DPICHANGED**. Il s’agit du facteur d’échelle auquel la fenêtre doit être mise à l’échelle pour les threads qui prennent en charge les modifications PPP.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) du *wParam* contient la valeur de l’axe Y de la nouvelle résolution PPP de la fenêtre. Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) du *wParam* contient la valeur de l’axe X de la nouvelle résolution PPP de la fenêtre. Par exemple, 96, 120, 144 ou 192. les valeurs de l’axe des X et de l’axe des Y sont identiques pour les applications Windows.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/windows/desktop/api/windef/ns-windef-rect) qui fournit une taille et une position suggérées de la fenêtre active mise à l’échelle pour la nouvelle résolution. Dans l’attente, les applications repositionneront et redimensionneront les fenêtres en fonction des suggestions fournies par *lParam* lors du traitement de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Ce message concerne uniquement les applications **\_ prenant en \_ \_ \_ charge la résolution par moniteur** ou la prise en charge **dpi par threads \_ \_ \_ \_ sensibles** à l’analyse. Il peut être reçu sur certaines modifications PPP si la fenêtre ou le processus de niveau supérieur s’exécute avec une prise en charge **dpi** ou si le système prend en **charge** les DPI, mais dans ce cas, il peut être ignoré en toute sécurité. Pour plus d’informations sur les différents types de reconnaissance, [**consultez \_ \_ prise**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) en la reconnaissance de la résolution des processus et [**\_ prise en dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness). les versions antérieures de Windows une prise en face des ppp nécessaire pour être liées au niveau d’une application. Ces applications utilisent **la \_ \_ reconnaissance des PPP de processus**. Actuellement, la reconnaissance DPI est liée aux threads et aux fenêtres individuelles plutôt qu’à l’ensemble de l’application. Ces applications utilisent **la \_ reconnaissance dpi**.

Vous devez uniquement utiliser l’axe des X ou la valeur de l’axe des Y lors de la mise à l’échelle de votre application, car elles sont identiques.

Pour gérer correctement ce message, vous devez redimensionner et repositionner votre fenêtre en fonction des suggestions fournies par *lParam* et à l’aide de [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si vous ne le faites pas, votre fenêtre augmente ou diminue par rapport à tout le reste sur le nouvel écran. Par exemple, si un utilisateur utilise plusieurs moniteurs et fait glisser votre fenêtre d’un moniteur 96 ppp vers une analyse 192 PPP, votre fenêtre apparaîtra en moitié aussi importante que d’autres éléments sur le moniteur de 192 PPP.

La valeur de base de DPI est définie en tant que **\_ \_ \_ dpi d’écran par défaut** de l’utilisateur, qui est défini sur 96. Pour déterminer le facteur de mise à l’échelle d’une analyse, prenez la valeur PPP et divisez par la valeur **\_ \_ \_ PPP d’écran par défaut** de l’utilisateur. Le tableau suivant fournit des exemples de valeurs PPP et les facteurs de mise à l’échelle associés.



| Valeur DPI | Pourcentage de mise à l’échelle |
|-----------|--------------------|
| 96        | 100 %               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200%               |



 

L’exemple suivant fournit un exemple de gestionnaire de modifications de PPP.


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



Le code suivant met à l’échelle de façon linéaire une valeur comprise entre 100% (96 ppp) et une valeur PPP arbitraire définie par *g \_ PPP*.


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



Une autre façon de mettre à l’échelle une valeur consiste à convertir la valeur PPP en un facteur d’échelle et à l’utiliser.


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_reconnaissance dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**\_détection des PPP de processus \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

