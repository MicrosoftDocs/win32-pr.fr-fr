---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plates sont encapsulées par la classe C++ SolidBrush.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Fonctions SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395554"
---
# <a name="solidbrush-functions"></a>Fonctions SolidBrush

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Nous vous recommandons de ne pas appeler directement les fonctions dans l’API plate. Chaque fois que vous effectuez des appels à GDI+, nous vous recommandons de le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Fonctions de pinceau et méthodes Wrapper correspondantes



| Fonction plate                                                                               | Méthode Wrapper                                                                                       | Remarques                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB Color, GpSolidFill \* \* Brush)**<br/>   | [**SolidBrush :: SolidBrush (dans la couleur const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Crée un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basé sur une couleur |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, ARGB Color)**<br/>   | [**SolidBrush :: SetColor (dans la couleur const Color& Color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Définit la couleur de ce pinceau Uni                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, ARGB \* Color)**<br/> | [**SolidBrush :: GetColor (couleur de sortie de sortie \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Obtient la couleur de ce pinceau Uni                                                      |



 

 

 
