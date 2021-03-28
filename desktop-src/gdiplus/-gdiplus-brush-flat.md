---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Fonctions Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319018"
---
# <a name="brush-functions-gdi"></a>Fonctions Brush (GDI+)

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Il est recommandé de ne pas appeler directement les fonctions dans l’API plate. Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Fonctions de pinceau et méthodes Wrapper correspondantes



| Fonction plate                                                                        | Méthode Wrapper                                          | Description                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)          | [**Brush :: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | La méthode [**Brush :: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crée un nouvel objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basé sur ce pinceau. |
| GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)                                 | virtuel ~ Brush ()                                        | Nettoie les ressources utilisées par un objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* Brush, GpBrushType \* type)<br/> | [**Brush :: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | La méthode [**Brush :: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtient le type de ce pinceau.                                                      |



 

 

 




