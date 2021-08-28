---
Description: Envoyé à une fenêtre après la modification de sa taille.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Message WM_SIZE (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 473e4e63523c7b97968e54349e5882b7e589fc7238d717ccf96563b5ce93388e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548219"
---
# <a name="wm_size-message"></a>\_Message de taille WM

Envoyé à une fenêtre après la modification de sa taille.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type de redimensionnement demandé. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                   | Signification                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**Taille \_ MAXHIDE**</dt> <dt>4</dt> </dl>       | Le message est envoyé à toutes les fenêtres indépendantes lorsqu’une autre fenêtre est agrandie.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**Taille \_ AGRANDIe**</dt> <dt>2</dt> </dl> | La fenêtre a été agrandie.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**Taille \_ MAXSHOW**</dt> <dt>3</dt> </dl>       | Le message est envoyé à toutes les fenêtres indépendantes quand une autre fenêtre a été restaurée à sa taille précédente.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**Taille \_ RÉDUIT**</dt> <dt>1</dt> </dl> | La fenêtre a été réduite.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**Taille \_ RESTAURÉ**</dt> <dt>0</dt> </dl>    | La fenêtre a été redimensionnée, mais ni la **taille \_ réduite** ni la **valeur \_ agrandie** à la taille ne s’appliquent.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible de *lParam* spécifie la nouvelle largeur de la zone cliente.

Le mot de poids fort de *lParam* spécifie la nouvelle hauteur de la zone cliente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="example"></a>Exemples

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

exemple de [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) sur GitHub.

## <a name="remarks"></a>Remarques

Si la fonction [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) ou [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) est appelée pour une fenêtre enfant à la suite du message **de \_ taille WM** , le paramètre *bRedraw* ou *bRepaint* doit être différent de zéro pour provoquer la redessination de la fenêtre.

Bien que la largeur et la hauteur d’une fenêtre soient des valeurs 32 bits, le paramètre *lParam* contient uniquement les 16 bits de poids faible de chacun.

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie les messages de **\_ taille WM** et de **\_ déplacement WM** quand elle traite le message [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .
Les messages de **\_ taille WM** et de **\_ déplacement WM** ne sont pas envoyés si une application gère le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**\_WINDOWPOSCHANGED WM**](wm-windowposchanged.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
