---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: Fonctions HatchBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d444fea500ce1e56e4c59420b913d5ff6cee965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991333"
---
# <a name="hatchbrush-functions"></a>Fonctions HatchBrush

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Il est recommandé de ne pas appeler directement les fonctions dans l’API plate. Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) .

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>Fonctions HatchBrush et méthodes Wrapper correspondantes



| Fonction plate                                                                                                               | Méthode Wrapper                                                                                                                                                                                   | Notes                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush (GpHatchStyle HatchStyle, ARGB forecol, ARGB backcol, GpHatch \* \* Brush)<br/> | [**HatchBrush :: HatchBrush (dans HatchStyle hatchStyle, dans la couleur const& foreColor, dans la couleur const& BackColor = Color ())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Crée un objet [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) basé sur un style de hachurage, une couleur de premier plan et une couleur d’arrière-plan. |
| GpStatus WINGDIPAPI GdipGetHatchStyle (GpHatch \* Brush, GpHatchStyle \* HatchStyle)<br/>                                | [**HatchStyle HatchBrush :: GetHatchStyle () const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Obtient le style de hachurage de ce pinceau hachuré.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor (GpHatch \* Brush, ARGB \* forecol)<br/>                                 | [**Status HatchBrush :: GetForegroundColor (couleur de sortie de sortie \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Obtient la couleur de premier plan de ce pinceau de hachurage.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor (GpHatch \* Brush, ARGB \* backcol)<br/>                                 | [**Status HatchBrush :: GetBackgroundColor (couleur de sortie de sortie \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Obtient la couleur d’arrière-plan de ce pinceau de hachurage.                                                                                             |



 

 

 
