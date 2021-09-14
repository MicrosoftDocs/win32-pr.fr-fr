---
title: Méthodes ID2D1Factory CreateWicBitmapRenderTarget
description: crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Méthodes CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112957"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>ID2D1Factory :: CreateWicBitmapRenderTarget, méthodes

crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                            | Description                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ Propriétés de la \_ cible \_ de rendu \* , ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).<br/> |
| [**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ Propriétés de la cible de rendu \_ \_&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).<br/> |



## <a name="remarks"></a>Notes

Votre application doit créer des cibles de rendu une seule fois et les conserver pendant toute la durée de vie de l’application ou jusqu’à ce que l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) soit reçue. Lorsque vous recevez cette erreur, vous devez recréer la cible de rendu (et toutes les ressources qu’elle a créées).

**Remarque**   cette méthode n’est pas prise en charge sur les Windows Phone et échoue quand elle est appelée sur un appareil avec le code d’erreur 0x8899000b (aucun périphérique de rendu matériel n’est disponible pour cette opération). étant donné que le Windows Phone Emulator prend en charge le rendu de distorsion, cette méthode échouera quand elle est appelée sur l’émulateur avec un code d’erreur différent, 0x88982f80 (wincodec \_ err \_ unsupportedpixelformat).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

