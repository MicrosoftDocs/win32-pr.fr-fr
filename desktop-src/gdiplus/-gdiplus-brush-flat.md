---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plate sont encapsulées par la classe C++ Brush.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Fonctions Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afdec5667dfcfe4b83e54af3fc0b88fcef991494e36f1e4788062029d1d6e29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888339"
---
# <a name="brush-functions-gdi"></a>Fonctions Brush (GDI+)

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Il est recommandé de ne pas appeler directement les fonctions dans l’API plate. chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. pour plus d’informations sur l’utilisation de ces méthodes wrapper, consultez [GDI+ l’API plate](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Fonctions de pinceau et méthodes Wrapper correspondantes



| Fonction plate                                                                        | Méthode Wrapper                                          | Description                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)          | [**Brush :: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | La méthode [**Brush :: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crée un nouvel objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basé sur ce pinceau. |
| GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)                                 | virtuel ~ Brush ()                                        | Nettoie les ressources utilisées par un objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* Brush, GpBrushType \* type)<br/> | [**Brush :: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | La méthode [**Brush :: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtient le type de ce pinceau.                                                      |



 

 

 




