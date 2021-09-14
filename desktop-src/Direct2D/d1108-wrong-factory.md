---
title: D1108 défaut incorrect
ms.assetid: eb851118-0541-4c9a-a22d-b98f041852bb
description: La ressource a été allouée par la fabrique 1 et utilisée avec la fabrique 2.
keywords:
- D1108 de la fabrique incorrecte
topic_type:
- apiref
api_name:
- D1108 Wrong Factory
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 463909abeda1410804fa4b842dbdc829c3a74271
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114073"
---
# <a name="d1108-wrong-factory"></a>D1108 : fabrique incorrecte

La ressource de ressource \[  \] a été allouée par la fabrique de fabrique \[ *1* \] et utilisée avec la fabrique de fabrique \[ *2* \] .

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*ressource*
</dt> <dd>

Adresse de l’interface.

</dd> <dt>

<span id="factory_1"></span><span id="FACTORY_1"></span>*usine 1*
</dt> <dd>

Adresse de la fabrique qui a alloué la *ressource*.

</dd> <dt>

<span id="factory_2"></span><span id="FACTORY_2"></span>*usine 2*
</dt> <dd>

Adresse de la fabrique avec laquelle la *ressource* a été utilisée.

</dd> </dl> 




 

## <a name="examples"></a>Exemples

L’exemple suivant crée d’abord deux objets [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) activés pour le débogage. Il crée ensuite une géométrie à partir de la première fabrique et un pinceau de la deuxième fabrique. Enfin, il appelle [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry), en passant la géométrie et le pinceau.


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif


        // Domain violation. Create a second Direct2D factory.
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory1
            );

        // Create a geometry from the second factory.
        hr = m_pD2DFactory1->CreateRectangleGeometry(
            D2D1::RectF(100, 50, 400, 160),
            &m_pRectangleGeometry
            );
```





<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        // Create a render target from the first factory.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
                &m_pBlackBrush
                );
        }</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        m_pRenderTarget->FillGeometry(
            m_pRectangleGeometry,   //The rectangle geometry created from the second factory.
            m_pBlackBrush   //The black brush created from the first factory.
            );</code></pre></td>
</tr>
</tbody>
</table>



Cet exemple génère le message de débogage suivant :


```
 D2D DEBUG ERROR - The resource [003BD628] was allocated 
by factory [002ED698] and used with factory [002ED470].
```



## <a name="possible-causes"></a>Causes possibles

Utilisation des ressources non valide. Une ressource allouée par une fabrique a été utilisée avec une autre fabrique.

 

 
