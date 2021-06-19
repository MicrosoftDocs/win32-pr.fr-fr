---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plates sont encapsulées par la classe C++ CachedBitmap.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: CachedBitmap, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce265592ad8aa10744ed124d246be69e258773f5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396195"
---
# <a name="cachedbitmap-functions"></a>CachedBitmap, fonctions

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Il est recommandé de ne pas appeler directement les fonctions dans l’API plate. Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Fonctions CachedBitmap et méthodes Wrapper correspondantes



| Fonction plate                                                                                                             | Méthode Wrapper                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap (GpBitmap \* bitmap, GpGraphics \* Graphics, GpCachedBitmap \* \* cachedBitmap)   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Crée un objet [**CachedBitmap :: CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) basé sur un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) et un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La bitmap mise en cache prend les données de pixels de l’objet **bitmap** et les stocke dans un format optimisé pour le périphérique d’affichage associé à l’objet **Graphics** . |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap (GpCachedBitmap \* cachedBitmap)<br/>                                      | ~ CachedBitmap ()                                                                                 | Nettoie les ressources utilisées par un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap (GpGraphics \* Graphics, GpCachedBitmap \* CACHEDBITMAP, int x, int y)            | [**Graphics ::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | La méthode [**Graphics ::D rawcachedbitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) dessine l’image stockée dans un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits (HENHMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags)<br/> | [**Métafichier :: EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Convertit un métafichier de format amélioré en métafichier Windows Metafile Format (WMF) et stocke les enregistrements convertis dans une mémoire tampon spécifiée.                                                                                                                                                                                                                                                                                       |



 

 

