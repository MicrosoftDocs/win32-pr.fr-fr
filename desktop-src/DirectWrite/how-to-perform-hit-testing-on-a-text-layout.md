---
title: Comment effectuer un test de positionnement sur une disposition de texte
description: Fournit un bref didacticiel sur l’ajout d’un test de positionnement à une application DirectWrite qui affiche du texte à l’aide de l’interface IDWriteTextLayout.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103953482"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Comment effectuer un test de positionnement sur une disposition de texte

Fournit un bref didacticiel sur l’ajout d’un test de positionnement à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Le résultat de ce didacticiel est une application qui souligne le caractère sur lequel un clic a été effectué à l’aide du bouton gauche de la souris, comme illustré dans la capture d’écran suivante.

![capture d’écran de « cliquez sur ce texte »](images/hittest.png)

Cette procédure contient les éléments suivants :

- [Étape 1 : créer une disposition de texte.](#step-1-create-a-text-layout)
- [Étape 2 : ajoutez une méthode OnClick.](#step-2-add-an-onclick-method)
- [Étape 3 : effectuer un test de positionnement.](#step-3-perform-hit-testing)
- [Étape 4 : souligner le texte sur lequel l’utilisateur a cliqué.](#step-4-underline-the-clicked-text)
- [Étape 5 : gérer le \_ message WM LBUTTONDOWN.](/windows)

## <a name="step-1-create-a-text-layout"></a>Étape 1 : créer une disposition de texte.

Pour commencer, vous aurez besoin d’une application qui utilise un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Si vous disposez déjà d’une application qui affiche du texte avec une disposition de texte, passez à l’étape 2.

Pour ajouter une disposition de texte, vous devez effectuer les opérations suivantes :

1. Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe.

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. À la fin de la méthode **CreateDeviceIndependentResources** , créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .

    ```cpp
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    ```

3. Ensuite, vous devez remplacer l’appel à la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) par [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) comme indiqué dans le code suivant.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Étape 2 : ajoutez une méthode OnClick.

À présent, ajoutez une méthode à la classe qui utilisera la fonctionnalité de test de positionnement de la disposition du texte.

1. Déclarez une méthode **OnClick** dans le fichier d’en-tête de classe.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Définissez une méthode **OnClick** dans le fichier d’implémentation de classe.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Étape 3 : effectuer un test de positionnement.

Pour déterminer où l’utilisateur a cliqué sur la disposition du texte, nous utilisons la méthode [**IDWriteTextLayout :: HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

Ajoutez le code suivant à la méthode **OnClick** que vous avez définie à l’étape 2.

1. Déclarez les variables que nous transmettons comme paramètres à la méthode.

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    La méthode [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) génère les paramètres suivants.

    | Variable         | Description                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | Géométrie englobant complètement l’emplacement du test de positionnement.                                                                                     |
    | *isInside*       | Indique si l’emplacement de test de positionnement est à l’intérieur ou non de la chaîne de texte. Lorsque la valeur est FALSe, la position la plus proche du bord du texte est retournée. |
    | *isTrailingHit*  | Indique si l’emplacement du test de positionnement se trouve au début ou à la fin du caractère.                                        |

2. Appelez la méthode [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) de l’objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    Le code de cet exemple passe les variables *x* et *y* pour la position sans aucune modification. Cela peut être fait dans cet exemple car la disposition du texte a la même taille que la fenêtre et provient de l’angle supérieur gauche de la fenêtre. Si ce n’est pas le cas, vous devez déterminer les coordonnées par rapport à l’origine de la disposition du texte.

## <a name="step-4-underline-the-clicked-text"></a>Étape 4 : souligner le texte sur lequel l’utilisateur a cliqué.

Ajoutez le code suivant à l' **OnClick** que vous avez défini à l’étape 2, après l’appel à la méthode [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

Ce code effectue les opérations suivantes.

1. Vérifie si le point de test de positionnement était à l’intérieur du texte à l’aide de la variable *isInside* .
2. Le membre **TextPosition** de la structure *hitTestMetrics* contient l’index de base zéro du caractère sur lequel l’utilisateur a cliqué.

    Obtient le soulignement de ce caractère en passant cette valeur à la méthode [**IDWriteTextLayout :: GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .

3. Déclare une variable [**de \_ \_ portée de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) avec la position de début définie sur **hitTestMetrics. TextPosition** et une longueur de 1.
4. Active ou désactive le soulignement à l’aide de la méthode [**IDWriteTextLayout :: SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .

Après avoir défini le soulignement, redessinez le texte en appelant la méthode **DrawD2DContent** de la classe.

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Étape 5 : gérer le \_ message WM LBUTTONDOWN.

Enfin, ajoutez le message **WM \_ LBUTTONDOWN** au gestionnaire de messages de votre application et appelez la méthode **OnClick** de la classe.

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

En **savoir \_ plus Les macros x \_ lParam** et **obten \_ x \_ lParam** sont déclarées dans le fichier d’en-tête windowsx. h. Ils récupèrent facilement la position x et y du clic de la souris.
