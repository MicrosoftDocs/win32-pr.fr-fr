---
description: Implémente l’interface IInkD2DRenderer.
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: InkD2DRenderer, classe
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkD2DRenderer
api_type:
- COM
api_location:
- Inkrenderer.idl
ms.openlocfilehash: 1649d52c2e9098513c115daaf295c4005e890b8e
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104211203"
---
# <a name="inkd2drenderer-class"></a><span data-ttu-id="cfdfd-103">InkD2DRenderer, classe</span><span class="sxs-lookup"><span data-stu-id="cfdfd-103">InkD2DRenderer class</span></span>

<span data-ttu-id="cfdfd-104">Implémente l’interface [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .</span><span class="sxs-lookup"><span data-stu-id="cfdfd-104">Implements the [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) interface.</span></span>

<span data-ttu-id="cfdfd-105">Un objet [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) permet le rendu des traits d’encre dans le contexte de périphérique Direct2D désigné d’une application Windows universelle, au lieu du contrôle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) par défaut.</span><span class="sxs-lookup"><span data-stu-id="cfdfd-105">An [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="members"></a><span data-ttu-id="cfdfd-106">Membres</span><span class="sxs-lookup"><span data-stu-id="cfdfd-106">Members</span></span>

<span data-ttu-id="cfdfd-107">La classe **InkD2DRenderer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cfdfd-107">The **InkD2DRenderer** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cfdfd-108">**InkD2DRenderer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cfdfd-108">**InkD2DRenderer** also has these types of members:</span></span>

- [<span data-ttu-id="cfdfd-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cfdfd-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cfdfd-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cfdfd-110">Methods</span></span>

<span data-ttu-id="cfdfd-111">La classe **InkD2DRenderer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cfdfd-111">The **InkD2DRenderer** class has these methods.</span></span>

| <span data-ttu-id="cfdfd-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="cfdfd-112">Method</span></span>                              | <span data-ttu-id="cfdfd-113">Description</span><span class="sxs-lookup"><span data-stu-id="cfdfd-113">Description</span></span>                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfdfd-114">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="cfdfd-114">**Draw**</span></span>](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | <span data-ttu-id="cfdfd-115">Restitue le trait d’encre dans le contexte de périphérique Direct2D désigné de l’application.</span><span class="sxs-lookup"><span data-stu-id="cfdfd-115">Renders the ink stroke to the designated Direct2D device context of the app.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="cfdfd-116">Fonctions d’accès de création \\</span><span class="sxs-lookup"><span data-stu-id="cfdfd-116">Creation\\Access Functions</span></span>

<span data-ttu-id="cfdfd-117">Appelez [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’identificateur de classe <strong>InkD2DRenderer</strong> pour récupérer une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="cfdfd-117">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkD2DRenderer</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a><span data-ttu-id="cfdfd-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="cfdfd-118">Examples</span></span>

<span data-ttu-id="cfdfd-119">Cet extrait de code du fichier « SceneComposer. cpp » de l' [exemple d’encrage complexe](/samples/microsoft/windows-universal-samples/complexink/) montre le rendu d’une collection de traits d’encre dans un contexte de périphérique Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cfdfd-119">This snippet from the "SceneComposer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) demonstrates the rendering of a collection of ink strokes to a Direct2D device context.</span></span>

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

<span data-ttu-id="cfdfd-120">Cet extrait de code du fichier « InkRenderer. cpp » de l' [exemple d’encrage complexe](/samples/microsoft/windows-universal-samples/complexink/) montre la méthode Render (appelée dans l’extrait de code précédent) qui appelle la méthode [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) pour le rendu des traits.</span><span class="sxs-lookup"><span data-stu-id="cfdfd-120">This snippet from the "InkRenderer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) shows the Render method (called in the previous snippet) that calls the [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) method for rendering the strokes.</span></span>

```C++
void InkRenderer::Render(
    Platform::Collections::Vector<
        Windows::UI::Input::Inking::InkStroke^>^ strokes,
        Microsoft::WRL::ComPtr<ID2D1DeviceContext> d2dContext)
{
    HRESULT hr = S_OK;
    if (_spInkD2DRenderer != nullptr)
    {
        if (strokes != nullptr && strokes->Size > 0)
        {
            // Cast the stroke collection into IUnknown to call Inkd2dRenderer
            ComPtr<IUnknown> spUnkStrokes = 
                reinterpret_cast<IUnknown*>(reinterpret_cast<__abi_IUnknown*>(strokes));
            hr = _spInkD2DRenderer->Draw(d2dContext.Get(), spUnkStrokes.Get(), false);
            if (FAILED(hr))
            {
                DX::ThrowIfFailed(hr);
            }
        }
    }
}
```

## <a name="requirements"></a><span data-ttu-id="cfdfd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfdfd-121">Requirements</span></span>

| <span data-ttu-id="cfdfd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfdfd-122">Requirement</span></span> | <span data-ttu-id="cfdfd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfdfd-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfdfd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfdfd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdfd-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfdfd-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cfdfd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfdfd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdfd-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfdfd-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="cfdfd-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfdfd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfdfd-129"><dt>Inkrenderer. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfdfd-129"><dt>Inkrenderer.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfdfd-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="cfdfd-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cfdfd-131"><dt>Inkrenderer. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cfdfd-131"><dt>Inkrenderer.idl</dt></span></span> </dl> |
| <span data-ttu-id="cfdfd-132">IID</span><span class="sxs-lookup"><span data-stu-id="cfdfd-132">IID</span></span><br/>                      | <span data-ttu-id="cfdfd-133">IID \_ IInkD2DRenderer est défini en tant que 4044e60c-7b01-4671-A97C-04e0210a07a5</span><span class="sxs-lookup"><span data-stu-id="cfdfd-133">IID\_IInkD2DRenderer is defined as 4044e60c-7b01-4671-a97c-04e0210a07a5</span></span><br/>         |

## <a name="related-topics"></a><span data-ttu-id="cfdfd-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfdfd-134">Related topics</span></span>

<span data-ttu-id="cfdfd-135">[Convertisseur d’encre](ink-renderer.md), [interactions du stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)du stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, [exemple d’encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe</span><span class="sxs-lookup"><span data-stu-id="cfdfd-135">[Ink renderer](ink-renderer.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
