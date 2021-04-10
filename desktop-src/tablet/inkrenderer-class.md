---
description: Représente la gestion des mappages de l’entrée manuscrite à la fenêtre d’affichage. Utilisez l’objet InkRenderer pour afficher l’encre dans une fenêtre. Vous pouvez également l’utiliser pour repositionner et redimensionner le trait.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: InkRenderer, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210825"
---
# <a name="inkrenderer-class"></a>InkRenderer, classe

Représente la gestion des mappages de l’entrée manuscrite à la fenêtre d’affichage. Utilisez l’objet **InkRenderer** pour afficher l’encre dans une fenêtre. Vous pouvez également l’utiliser pour repositionner et redimensionner le trait.

**InkRenderer** possède les types de membres suivants :

-   [Interfaces](#interfaces)
-   [Méthodes](#methods)

### <a name="interfaces"></a>Interfaces

La classe **InkRenderer** définit ces interfaces.



| Interface        | Description                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | Cet objet implémente l’interface com **IInkRenderer** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkRenderer** possède ces méthodes.



| Méthode                                                                     | Description                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dessin**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Dessine des traits sur un contexte de périphérique.<br/>                                                                                                            |
| [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Dessine un trait sur le contexte de périphérique Windows spécifié.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Récupère la transformation d’objet qui a été utilisée pour restituer l’encre.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Récupère la transformation de vue qui est utilisée pour restituer l’encre.<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Convertit un emplacement dans les coordonnées de l’espace d’encre en espace en pixels.<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Convertit un tableau de points dans les coordonnées d’espace d’encre en espace de pixels.<br/>                                                                          |
| [**Unité**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Calcule le rectangle sur le contexte de périphérique qui contient une collection de traits s’ils ont été dessinés avec l’objet **InkRenderer** .<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Calcule le rectangle sur le contexte de périphérique qui contiendra un trait s’il a été dessiné avec l’objet **InkRenderer** .<br/>                |
| [**Activer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Applique une translation à la transformation de vue dans les coordonnées d’espace d’encre.<br/>                                                                         |
| [**PixelToInkSpace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Convertit un emplacement en coordonnées en pixels en espace d’encre.<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Convertit un tableau de points en coordonnées d’espace de pixels en espace d’encre.<br/>                                                                          |
| [**Faire pivoter**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Applique une rotation à la transformation de la vue.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Met à l’échelle la transformation de la vue dans la dimension X et Y.<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Définit la transformation d’objet utilisée pour restituer l’encre.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Définit la transformation de vue utilisée pour restituer l’encre.<br/>                                                                                           |



 

## <a name="remarks"></a>Notes

L’impression s’effectue également par le biais de l’objet **InkRenderer** .

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Renderer (propriété)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**InkDrawingAttributes, classe**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

