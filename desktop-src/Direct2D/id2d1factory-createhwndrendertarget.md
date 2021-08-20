---
title: Méthodes ID2D1Factory CreateHwndRenderTarget (D2d1. h)
description: Crée un ID2D1HwndRenderTarget, une cible de rendu qui est rendue dans une fenêtre.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Méthodes CreateHwndRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 241d0977adb4ec19472303165538e1a4c1fcafe87d0b781cd64bd34cdac92190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118002921"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a>ID2D1Factory :: CreateHwndRenderTarget, méthodes

Crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), une cible de rendu qui est rendue dans une fenêtre.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                                                                              | Description                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**CreateHwndRenderTarget (propriétés de la \_ cible de rendu d2d1, propriétés de la cible de \_ \_ \* \_ rendu HWND d2d1 \_ \_ \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) | Crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), une cible de rendu qui est rendue dans une fenêtre.<br/> |
| [**CreateHwndRenderTarget (propriétés de la \_ cible de rendu D2D1 \_ \_&, propriétés de la cible de \_ rendu HWND d2d1 \_ \_ \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))   | Crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), une cible de rendu qui est rendue dans une fenêtre.<br/> |



## <a name="remarks"></a>Remarques

Lorsque vous créez une cible de rendu et que l’accélération matérielle est disponible, vous allouez des ressources sur le GPU de l’ordinateur. En créant une cible de rendu une fois et en la conservant le plus longtemps possible, vous obtenez des avantages en matière de performances. Votre application doit créer des cibles de rendu une seule fois et les conserver pendant toute la durée de vie de l’application ou jusqu’à ce que l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) soit reçue. Lorsque vous recevez cette erreur, vous devez recréer la cible de rendu (et toutes les ressources qu’elle a créées).

## <a name="examples"></a>Exemples

L’exemple suivant crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
