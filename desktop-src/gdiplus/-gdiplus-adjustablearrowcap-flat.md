---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: AdjustableArrowCap, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d377b319169a2a10c864db5aec402fe633beb3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991456"
---
# <a name="adjustablearrowcap-functions"></a>AdjustableArrowCap, fonctions

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Il est recommandé de ne pas appeler directement les fonctions dans l’API plate. Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) .

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Fonctions AdjustableArrowCap et méthodes Wrapper correspondantes



| Fonction plate                                                                                                          | Méthode Wrapper                                                                                                                | Description                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap (hauteur réelle, largeur réelle, valeur BOOLÉENNE isFilled, \* \* Cap GpAdjustableArrowCap) | [**AdjustableArrowCap::AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Crée un embout de ligne réglable avec la hauteur et la largeur spécifiées. Le plafond de la ligne de flèche peut être rempli ou ne peut pas être rempli. L’incrustation intermédiaire a par défaut la valeur zéro.                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight ( \* Cap GpAdjustableArrowCap, hauteur réelle)                           | [**AdjustableArrowCap :: SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | La méthode [**AdjustableArrowCap :: SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) définit la hauteur de l’embout de la flèche. Il s’agit de la distance entre la base de la flèche et son sommet.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight ( \* Cap GpAdjustableArrowCap, \* hauteur réelle)                         | [**AdjustableArrowCap :: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | La méthode [**AdjustableArrowCap :: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) obtient la hauteur de l’embout de flèche. La hauteur est la distance entre la base de la flèche et son sommet.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth ( \* Cap GpAdjustableArrowCap, largeur réelle)                             | [**AdjustableArrowCap :: SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | La méthode [**AdjustableArrowCap :: SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) définit la largeur de l’embout de la flèche. La largeur est la distance entre les points de terminaison de la base de la flèche.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth ( \* Cap GpAdjustableArrowCap, \* largeur réelle)                           | [**AdjustableArrowCap :: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | La méthode [**AdjustableArrowCap :: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) obtient la largeur de l’embout de flèche. La largeur est la distance entre les points de terminaison de la base de la flèche.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* Cap, Real middleInset)                 | [**AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | La méthode [**AdjustableArrowCap :: SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) définit le nombre d’unités que le milieu de la base déplace vers le vertex.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* Cap, Real \* middleInset)<br/>    | [**AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | La méthode [**AdjustableArrowCap :: GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) obtient la valeur de l’incrustation. L’incrustation intermédiaire est le nombre d’unités que le point médian de la base déplace vers le vertex. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState (GpAdjustableArrowCap \* Cap, bool fillState)<br/>          | [**AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | La méthode [**AdjustableArrowCap :: SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) définit l’état de remplissage de l’embout de flèche. Si l’embout de flèche n’est pas rempli, seul le contour est dessiné.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState (GpAdjustableArrowCap \* Cap, bool \* fillState)<br/>        | [**AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | La méthode [**AdjustableArrowCap :: IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) détermine si l’embout de flèche est rempli.                                                                                               |



 

 

