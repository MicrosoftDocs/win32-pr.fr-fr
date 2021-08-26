---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plates sont encapsulées par la classe C++ SolidBrush.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Fonctions SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0a45d36a174e765990f284d99d18a18d420745967b36cdd40d4a0ee7d1c0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014699"
---
# <a name="solidbrush-functions"></a>Fonctions SolidBrush

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Nous vous recommandons de ne pas appeler directement les fonctions dans l’API plate. chaque fois que vous effectuez des appels à GDI+, nous vous recommandons de le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. pour plus d’informations sur l’utilisation de ces méthodes wrapper, consultez [GDI+ l’API plate](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Fonctions de pinceau et méthodes Wrapper correspondantes



| Fonction plate                                                                               | Méthode Wrapper                                                                                       | Remarques                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB Color, GpSolidFill \* \* Brush)**<br/>   | [**SolidBrush :: SolidBrush (dans la couleur const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Crée un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basé sur une couleur |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, ARGB Color)**<br/>   | [**SolidBrush :: SetColor (dans la couleur const Color& Color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Définit la couleur de ce pinceau Uni                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, ARGB \* Color)**<br/> | [**SolidBrush :: GetColor (couleur de sortie de sortie \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Obtient la couleur de ce pinceau Uni                                                      |



 

 

 
