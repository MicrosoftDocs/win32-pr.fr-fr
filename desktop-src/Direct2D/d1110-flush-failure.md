---
title: Échec du vidage de D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Échec d’un appel de vidage par une cible de rendu
keywords:
- Erreur de vidage D1110 Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 12d6a990d3d65c1a711825e6d45720f3df977ca78efb16c1d39bb9b2251c53b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758149"
---
# <a name="d1110-flush-failure"></a>D1110 : échec de vidage

Un appel de vidage par une cible de rendu a échoué \[  \] . Balises \[ *: étiquette1*, *tag2* \] .

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*ressource*
</dt> <dd>

Adresse de la cible de rendu.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*: étiquette1*
</dt> <dd>

Première valeur de la balise. Pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Deuxième valeur de balise. Pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Niveau d’erreur | Avertissement |



 

## <a name="examples"></a>Exemples

**Exemple 1 :** Le code suivant montre qu’un appel de dessin est dans un État non valide. Pour éviter le message d’avertissement, utilisez [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) pour définir l’anticrénelage du mode anticrénelage d2d1 \_ \_ \_ avant un appel [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





Cet exemple génère le message de débogage suivant :

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Exemple 2 :** Le code suivant montre que le [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) est appelé après l’appel [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



Cet exemple génère le message de débogage suivant :

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Causes possibles

L’appel de [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) peut échouer pour l’une des deux raisons suivantes. Elle peut échouer parce que la méthode a été appelée en dehors de l’appel [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , ou elle peut échouer en raison d’une erreur produite par l’une des opérations de la cible de rendu qui ont été traitées depuis le dernier appel de **vidage** ou l’appel **EndDraw** . Pour résoudre le problème, l’application doit déterminer la cause de l’erreur et prendre les mesures appropriées.

## <a name="fixes"></a>Correctifs

Il existe de nombreuses raisons pour lesquelles un appel de [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) peut échouer. L’application doit déterminer la cause de l’erreur et prendre les mesures appropriées.

 

 