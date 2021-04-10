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
# <a name="inkd2drenderer-class"></a>InkD2DRenderer, classe

Implémente l’interface [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .

Un objet [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) permet le rendu des traits d’encre dans le contexte de périphérique Direct2D désigné d’une application Windows universelle, au lieu du contrôle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) par défaut.

## <a name="members"></a>Membres

La classe **InkD2DRenderer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkD2DRenderer** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **InkD2DRenderer** possède ces méthodes.

| Méthode                              | Description                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Dessin**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Restitue le trait d’encre dans le contexte de périphérique Direct2D désigné de l’application.<br/> |

## <a name="creationaccess-functions"></a>Fonctions d’accès de création \\

Appelez [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’identificateur de classe <strong>InkD2DRenderer</strong> pour récupérer une référence à l’objet.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Exemples

Cet extrait de code du fichier « SceneComposer. cpp » de l' [exemple d’encrage complexe](/samples/microsoft/windows-universal-samples/complexink/) montre le rendu d’une collection de traits d’encre dans un contexte de périphérique Direct2D.

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Cet extrait de code du fichier « InkRenderer. cpp » de l' [exemple d’encrage complexe](/samples/microsoft/windows-universal-samples/complexink/) montre la méthode Render (appelée dans l’extrait de code précédent) qui appelle la méthode [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) pour le rendu des traits.

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

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| En-tête<br/>                   | <dl> <dt>Inkrenderer. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Inkrenderer. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer est défini en tant que 4044e60c-7b01-4671-A97C-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Rubriques connexes

[Convertisseur d’encre](ink-renderer.md), [interactions du stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)du stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, [exemple d’encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe
