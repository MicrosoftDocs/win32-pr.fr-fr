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
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a><span data-ttu-id="c9578-103">Comment effectuer un test de positionnement sur une disposition de texte</span><span class="sxs-lookup"><span data-stu-id="c9578-103">How to Perform Hit Testing on a Text Layout</span></span>

<span data-ttu-id="c9578-104">Fournit un bref didacticiel sur l’ajout d’un test de positionnement à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="c9578-104">Provides a short tutorial about how to add hit testing to a [DirectWrite](direct-write-portal.md) application that displays text by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="c9578-105">Le résultat de ce didacticiel est une application qui souligne le caractère sur lequel un clic a été effectué à l’aide du bouton gauche de la souris, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="c9578-105">The result of this tutorial is an application that underlines the character that is clicked on by the left mouse button, as shown in the following screen shot.</span></span>

![capture d’écran de « cliquez sur ce texte »](images/hittest.png)

<span data-ttu-id="c9578-107">Cette procédure contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c9578-107">This how to contains the following parts:</span></span>

- [<span data-ttu-id="c9578-108">Étape 1 : créer une disposition de texte.</span><span class="sxs-lookup"><span data-stu-id="c9578-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
- [<span data-ttu-id="c9578-109">Étape 2 : ajoutez une méthode OnClick.</span><span class="sxs-lookup"><span data-stu-id="c9578-109">Step 2: Add an OnClick method.</span></span>](#step-2-add-an-onclick-method)
- [<span data-ttu-id="c9578-110">Étape 3 : effectuer un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="c9578-110">Step 3: Perform Hit Testing.</span></span>](#step-3-perform-hit-testing)
- [<span data-ttu-id="c9578-111">Étape 4 : souligner le texte sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="c9578-111">Step 4: Underline the Clicked Text.</span></span>](#step-4-underline-the-clicked-text)
- [<span data-ttu-id="c9578-112">Étape 5 : gérer le \_ message WM LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="c9578-112">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>](/windows)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="c9578-113">Étape 1 : créer une disposition de texte.</span><span class="sxs-lookup"><span data-stu-id="c9578-113">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="c9578-114">Pour commencer, vous aurez besoin d’une application qui utilise un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="c9578-114">To begin, you will need an application that uses an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="c9578-115">Si vous disposez déjà d’une application qui affiche du texte avec une disposition de texte, passez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="c9578-115">If you already have an application that displays text with a text layout, go to Step 2.</span></span>

<span data-ttu-id="c9578-116">Pour ajouter une disposition de texte, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9578-116">To add a text layout you must do the following:</span></span>

1. <span data-ttu-id="c9578-117">Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe.</span><span class="sxs-lookup"><span data-stu-id="c9578-117">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. <span data-ttu-id="c9578-118">À la fin de la méthode **CreateDeviceIndependentResources** , créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="c9578-118">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>

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

3. <span data-ttu-id="c9578-119">Ensuite, vous devez remplacer l’appel à la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) par [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="c9578-119">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) as shown in the following code.</span></span>

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a><span data-ttu-id="c9578-120">Étape 2 : ajoutez une méthode OnClick.</span><span class="sxs-lookup"><span data-stu-id="c9578-120">Step 2: Add an OnClick method.</span></span>

<span data-ttu-id="c9578-121">À présent, ajoutez une méthode à la classe qui utilisera la fonctionnalité de test de positionnement de la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="c9578-121">Now add a method to the class that will use the hit testing functionality of the text layout.</span></span>

1. <span data-ttu-id="c9578-122">Déclarez une méthode **OnClick** dans le fichier d’en-tête de classe.</span><span class="sxs-lookup"><span data-stu-id="c9578-122">Declare an **OnClick** method in the class header file.</span></span>

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. <span data-ttu-id="c9578-123">Définissez une méthode **OnClick** dans le fichier d’implémentation de classe.</span><span class="sxs-lookup"><span data-stu-id="c9578-123">Define an **OnClick** method in the class implementation file.</span></span>

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a><span data-ttu-id="c9578-124">Étape 3 : effectuer un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="c9578-124">Step 3: Perform Hit Testing.</span></span>

<span data-ttu-id="c9578-125">Pour déterminer où l’utilisateur a cliqué sur la disposition du texte, nous utilisons la méthode [**IDWriteTextLayout :: HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="c9578-125">To determine where the user has clicked the text layout we will use the [**IDWriteTextLayout::HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

<span data-ttu-id="c9578-126">Ajoutez le code suivant à la méthode **OnClick** que vous avez définie à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="c9578-126">Add the following to the **OnClick** method that you defined in Step 2.</span></span>

1. <span data-ttu-id="c9578-127">Déclarez les variables que nous transmettons comme paramètres à la méthode.</span><span class="sxs-lookup"><span data-stu-id="c9578-127">Declare the variables we will pass as parameters to the method.</span></span>

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    <span data-ttu-id="c9578-128">La méthode [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) génère les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="c9578-128">The [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method outputs the following parameters.</span></span>

    | <span data-ttu-id="c9578-129">Variable</span><span class="sxs-lookup"><span data-stu-id="c9578-129">Variable</span></span>         | <span data-ttu-id="c9578-130">Description</span><span class="sxs-lookup"><span data-stu-id="c9578-130">Description</span></span>                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c9578-131">*hitTestMetrics*</span><span class="sxs-lookup"><span data-stu-id="c9578-131">*hitTestMetrics*</span></span> | <span data-ttu-id="c9578-132">Géométrie englobant complètement l’emplacement du test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="c9578-132">The geometry fully enclosing the hit-test location.</span></span>                                                                                     |
    | <span data-ttu-id="c9578-133">*isInside*</span><span class="sxs-lookup"><span data-stu-id="c9578-133">*isInside*</span></span>       | <span data-ttu-id="c9578-134">Indique si l’emplacement de test de positionnement est à l’intérieur ou non de la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="c9578-134">Indicates whether the hit-test location is inside the text string or not.</span></span> <span data-ttu-id="c9578-135">Lorsque la valeur est FALSe, la position la plus proche du bord du texte est retournée.</span><span class="sxs-lookup"><span data-stu-id="c9578-135">When FALSE, the position nearest the text's edge is returned.</span></span> |
    | <span data-ttu-id="c9578-136">*isTrailingHit*</span><span class="sxs-lookup"><span data-stu-id="c9578-136">*isTrailingHit*</span></span>  | <span data-ttu-id="c9578-137">Indique si l’emplacement du test de positionnement se trouve au début ou à la fin du caractère.</span><span class="sxs-lookup"><span data-stu-id="c9578-137">Indicates whether the hit-test location is at the leading or the trailing side of the character.</span></span>                                        |

2. <span data-ttu-id="c9578-138">Appelez la méthode [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) de l’objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="c9578-138">Call the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method of the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    <span data-ttu-id="c9578-139">Le code de cet exemple passe les variables *x* et *y* pour la position sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="c9578-139">The code in this example passes the *x* and *y* variables for the position without any modification.</span></span> <span data-ttu-id="c9578-140">Cela peut être fait dans cet exemple car la disposition du texte a la même taille que la fenêtre et provient de l’angle supérieur gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9578-140">This can be done in this example because the text layout is the same size as the window and originates in the upper-left corner of the window.</span></span> <span data-ttu-id="c9578-141">Si ce n’est pas le cas, vous devez déterminer les coordonnées par rapport à l’origine de la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="c9578-141">If this was not the case, you would have to determine the coordinates in relation to the origin of the text layout.</span></span>

## <a name="step-4-underline-the-clicked-text"></a><span data-ttu-id="c9578-142">Étape 4 : souligner le texte sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="c9578-142">Step 4: Underline the Clicked Text.</span></span>

<span data-ttu-id="c9578-143">Ajoutez le code suivant à l' **OnClick** que vous avez défini à l’étape 2, après l’appel à la méthode [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="c9578-143">Add the following to the **OnClick** you defined in Step 2, after the call to the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

<span data-ttu-id="c9578-144">Ce code effectue les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9578-144">This code does the following.</span></span>

1. <span data-ttu-id="c9578-145">Vérifie si le point de test de positionnement était à l’intérieur du texte à l’aide de la variable *isInside* .</span><span class="sxs-lookup"><span data-stu-id="c9578-145">Checks if the hit-test point was inside the text using the *isInside* variable.</span></span>
2. <span data-ttu-id="c9578-146">Le membre **TextPosition** de la structure *hitTestMetrics* contient l’index de base zéro du caractère sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="c9578-146">The **textPosition** member of the *hitTestMetrics* structure contains the zero-based index of the character clicked.</span></span>

    <span data-ttu-id="c9578-147">Obtient le soulignement de ce caractère en passant cette valeur à la méthode [**IDWriteTextLayout :: GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .</span><span class="sxs-lookup"><span data-stu-id="c9578-147">Gets the underline for this character by passing this value to the [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) method.</span></span>

3. <span data-ttu-id="c9578-148">Déclare une variable [**de \_ \_ portée de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) avec la position de début définie sur **hitTestMetrics. TextPosition** et une longueur de 1.</span><span class="sxs-lookup"><span data-stu-id="c9578-148">Declares a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable with the start position set to **hitTestMetrics.textPosition** and a length of 1.</span></span>
4. <span data-ttu-id="c9578-149">Active ou désactive le soulignement à l’aide de la méthode [**IDWriteTextLayout :: SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .</span><span class="sxs-lookup"><span data-stu-id="c9578-149">Toggles the underline by using the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>

<span data-ttu-id="c9578-150">Après avoir défini le soulignement, redessinez le texte en appelant la méthode **DrawD2DContent** de la classe.</span><span class="sxs-lookup"><span data-stu-id="c9578-150">After setting the underline, redraw the text by calling the **DrawD2DContent** method of the class.</span></span>

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a><span data-ttu-id="c9578-151">Étape 5 : gérer le \_ message WM LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="c9578-151">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>

<span data-ttu-id="c9578-152">Enfin, ajoutez le message **WM \_ LBUTTONDOWN** au gestionnaire de messages de votre application et appelez la méthode **OnClick** de la classe.</span><span class="sxs-lookup"><span data-stu-id="c9578-152">Finally, add the **WM\_LBUTTONDOWN** message to the message handler for your application and call the **OnClick** method of the class.</span></span>

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

<span data-ttu-id="c9578-153">En **savoir \_ plus Les macros x \_ lParam** et **obten \_ x \_ lParam** sont déclarées dans le fichier d’en-tête windowsx. h.</span><span class="sxs-lookup"><span data-stu-id="c9578-153">**GET\_X\_LPARAM** and **GET\_X\_LPARAM** macros are declared in the windowsx.h header file.</span></span> <span data-ttu-id="c9578-154">Ils récupèrent facilement la position x et y du clic de la souris.</span><span class="sxs-lookup"><span data-stu-id="c9578-154">They easily retrieve the x and y position of the mouse click.</span></span>
