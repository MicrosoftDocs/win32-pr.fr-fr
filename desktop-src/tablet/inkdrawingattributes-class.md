---
description: Représente les attributs qui sont appliqués à l’encre lorsqu’elle est dessinée.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: InkDrawingAttributes, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320138"
---
# <a name="inkdrawingattributes-class"></a>InkDrawingAttributes, classe

Représente les attributs qui sont appliqués à l’encre lorsqu’elle est dessinée.

**InkDrawingAttributes** possède les types de membres suivants :

-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="interfaces"></a>Interfaces

La classe **InkDrawingAttributes** définit ces interfaces.



| Interface                 | Description                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkDrawingAttributes** | Cet objet implémente l’interface com **IInkDrawingAttributes** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkDrawingAttributes** possède ces méthodes.



| Méthode                         | Description                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Répliqué**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Crée un objet [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** ou [**InkRecognizerContext**](inkrecognizercontext-class.md) dupliqué.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **InkDrawingAttributes** possède les propriétés suivantes.



| Propriété                                                                           | Type d’accès           | Description                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Crénelées**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Lecture/écriture<br/> | Obtient ou définit la valeur qui spécifie si les couleurs de premier plan et d’arrière-plan le long du bord de l’encre sont fusionnées pour augmenter la fluidité d’un trait d’encre.<br/> |
| [**Couleur**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Lecture/écriture<br/> | Obtient ou définit la couleur de l’encre dessinée avec cet objet **InkDrawingAttributes** .<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Lecture seule<br/>  | Obtient la collection de données définies par l’application qui est stockée dans l’objet **InkDrawingAttributes** .<br/>                                                                |
| [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Lecture/écriture<br/> | Obtient ou définit la valeur qui spécifie si l’entrée manuscrite est rendue sous la forme d’une série de courbes au lieu de lignes entre des points d’échantillon de stylet.<br/>                                    |
| [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Lecture/écriture<br/> | Obtient ou définit la hauteur du stylet lors du dessin de l’encre avec cet objet **InkDrawingAttributes** .<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Lecture/écriture<br/> | Obtient ou définit la valeur qui spécifie si l’encre dessinée devient automatiquement plus grande, avec une pression accrue du Conseil du stylet sur l’aire de tablette.<br/>                     |
| [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Lecture/écriture<br/> | Obtient ou définit l’info-bulle du stylet à utiliser (boule ou rectangle) lors du dessin de l’encre avec cet objet **InkDrawingAttributes** .<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Lecture/écriture<br/> | Obtient ou définit la manière dont la couleur du stylet interagit avec les couleurs d’arrière-plan existantes sur l’affichage lorsque l’encre est dessinée.<br/>                                                    |
| [**Transparence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Lecture/écriture<br/> | Obtient ou définit la valeur de transparence de l’encre dessinée. Les valeurs sont comprises entre zéro (entièrement opaque) et 255 (entièrement transparent).<br/>                                               |
| [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Lecture/écriture<br/> | Obtient ou définit la largeur du stylet lors du dessin de l’encre avec cet objet **InkDrawingAttributes** .<br/>                                                                         |



 

## <a name="remarks"></a>Notes

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Ces attributs de dessin peuvent être associés à un trait ou à un curseur et spécifier des paramètres tels que la couleur, la largeur et la transparence.

Pour spécifier les attributs de dessin d’un trait, utilisez la propriété [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) de l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . Pour spécifier les attributs de dessin de tous les traits dans une collection de traits, appelez la méthode [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Chaque objet [**InkCollector**](inkcollector-class.md) , objet [**InkOverlay**](inkoverlay-class.md) et contrôle [InkPicture](inkpicture-control-reference.md) peuvent spécifier un ensemble différent d’attributs de dessin pour le même curseur. Utilisez la propriété [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) pour obtenir ou définir les attributs de dessin d’un curseur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DrawingAttributes, propriété**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**DrawingAttributes, propriété**
</dt> <dt>

**DrawingAttributes, propriété**
</dt> <dt>

[**Propriété DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**Propriété DefaultDrawingAttributes**
</dt> <dt>

**Propriété DefaultDrawingAttributes**
</dt> <dt>

[**Méthode ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDisp, classe**](inkdisp-class.md)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

