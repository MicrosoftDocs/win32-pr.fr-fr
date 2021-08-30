---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Stocke une paire ordonnée d'entiers, représentant généralement la largeur et la hauteur d'un rectangle.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b60627021e55e088a35692dffb8292d5c57fcf0932de255c19f4380ee29e8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967099"
---
# <a name="d2d1_size_u"></a>Taille de D2D1 \_ \_ U

Stocke une paire ordonnée d'entiers, représentant généralement la largeur et la hauteur d'un rectangle.


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>Remarques

Comme les points, les tailles sont un autre concept graphique important. Dans Direct2D, les tailles sont représentées par les structures **d2d1 \_ size \_ U** ou [**d2d1 \_ size \_ F**](d2d1-size-f.md) . Elles contiennent toutes deux une paire ordonnée de nombres. La **structure \_ \_ U de taille d2d1** contient une paire ordonnée de valeurs **UInt32** et la **structure \_ d2d1 taille \_ F** contient une paire ordonnée de valeurs **float** .

La **structure \_ \_ U de taille d2d1** offre un moyen pratique de stocker une paire ordonnée de nombres, tels que la largeur et la hauteur d’un rectangle.

**D2d1 \_ TAILLE \_ u** est un nouveau nom pour un type déjà défini **de \_ taille \_ D2D (u**). Vous pouvez utiliser la fonction **d2d1 :: Resize** pour créer une structure **de \_ taille \_ d2d1** . Cette structure est couramment utilisée pour spécifier la taille en pixels d’une structure [**de \_ \_ Propriétés de \_ cible \_ de rendu HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) . L’exemple suivant illustre l’utilisation de cette structure.


```C++
    if (!m_pRenderTarget)
    {
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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2DBaseTypes. h (inclure D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Taille ( \_ U) D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**D2D1 \_ taille \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

