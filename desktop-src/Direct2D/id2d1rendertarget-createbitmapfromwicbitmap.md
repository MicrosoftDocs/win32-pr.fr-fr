---
title: Méthodes ID2D1RenderTarget CreateBitmapFromWicBitmap
description: crée un ID2D1Bitmap en copiant la bitmap WIC (Microsoft Windows Imaging Component) spécifiée.
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- Méthodes CreateBitmapFromWicBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 23ad055beab9f24c39f032a3e28456c231480c68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112801"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>ID2D1RenderTarget :: CreateBitmapFromWicBitmap, méthodes

crée un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) en copiant la bitmap WIC (Microsoft Windows Imaging Component) spécifiée.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                              | Description                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | crée un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) en copiant la bitmap WIC (Microsoft Windows Imaging Component) spécifiée.<br/>  |
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , d2d1 \_ \_ Propriétés bitmap&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | crée un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) en copiant la bitmap WIC (Microsoft Windows Imaging Component) spécifiée.<br/> |
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , d2d1 \_ , \_ Propriétés de bitmap \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | crée un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) en copiant la bitmap WIC (Microsoft Windows Imaging Component) spécifiée.<br/> |



## <a name="remarks"></a>Notes

Pour que Direct2D puisse charger une image WIC, il doit être converti en un format de pixel pris en charge et en mode Alpha. Pour obtenir la liste des formats de pixel et des modes alpha pris en charge, consultez [formats de pixel pris en charge et modes alpha](supported-pixel-formats-and-alpha-modes.md).

## <a name="examples"></a>Exemples

Pour obtenir des exemples, consultez [Comment charger une image bitmap à partir d’un fichier](how-to-load-a-direct2d-bitmap-from-a-file.md) et [Comment charger une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Chargement d’une image bitmap à partir d’un fichier](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[Formats de pixel et modes alpha pris en charge](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

