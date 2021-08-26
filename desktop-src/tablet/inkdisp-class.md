---
description: 'Classe InkDisp : représente les traits d’encre collectés dans un espace d’encre.'
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: InkDisp, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 928bda8af246b41bab2c285a5292155917ba8903c6dd71c20177dbf906c64924
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939159"
---
# <a name="inkdisp-class"></a>InkDisp, classe

Représente les traits d’encre collectés dans un espace d’encre.

**InkDisp** possède les types de membres suivants :

-   [Événements](#events)
-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

La classe **InkDisp** contient ces événements.



| Événement                                    | Description                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Se produit lorsqu’un trait est ajouté à l’objet **InkDisp** .<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Se produit lorsqu’un trait est supprimé de l’objet **InkDisp** .<br/> |



 

### <a name="interfaces"></a>Interfaces

La classe **InkDisp** définit ces interfaces.



| Interface    | Description                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Cet objet implémente l’interface com **IInkDisp** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkDisp** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Insère une collection de traits dans l’objet **InkDisp** au niveau du rectangle spécifié.<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Indique si [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) peut être converti en objet **InkDisp** .<br/>                                                                                       |
| [**Clip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Supprime des parties d’un trait ou d’une collection de traits situés à l’extérieur d’un rectangle.<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Copie la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dans le presse-papiers.<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Copie les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenus dans le rectangle connu dans le presse-papiers.<br/>                                                               |
| [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Copie [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) du presse-papiers vers l’objet **InkDisp** .<br/>                                                                                               |
| [**Répliqué**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Crée un objet **InkDisp** dupliqué.<br/>                                                                                                                                                   |
| [**CreateStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Crée un trait à partir des points ou des données de paquet.<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Crée une collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) pour cet objet **InkDisp** .<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Supprime un trait de l’objet **InkDisp** .<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Supprime les traits de l’objet **InkDisp** .<br/>                                                                                                                                              |
| [**Méthode ExtractStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Extrait les traits de l’objet **InkDisp** et retourne un nouvel objet **InkDisp** contenant les traits extraits.<br/>                                                                       |
| [**Méthode ExtractWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Coupe ou copie les traits d’un objet de **classe InkDisp** existant et les colle dans un nouvel objet de **classe InkDisp** , en utilisant le rectangle connu pour déterminer les traits à extraire.<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Récupère le cadre englobant de tous les traits dans l’objet **InkDisp** .<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Récupère la collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui est entièrement à l’intérieur ou à l’intersection d’un cercle connu.<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Récupère les traits dans une zone de sélection de polylignes.<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Récupère les traits qui sont contenus dans un rectangle spécifié.<br/>                                                                                                                    |
| [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Remplit un nouvel objet **InkDisp** avec des données binaires connues.<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Récupère le [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dans l’objet **InkDisp** le plus proche d’un point connu, en fournissant éventuellement des informations supplémentaires.<br/>                       |
| [**Enregistrer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Convertit l’encre dans un format spécifié et retourne les données binaires.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propriétés

La classe **InkDisp** possède les propriétés suivantes.



| Propriété                                                                           | Type d’accès           | Description                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Lecture seule<br/>  | Obtient la collection [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) à rendre persistante avec l’encre.<br/>                             |
| [**Dirt**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Lecture/écriture<br/> | Obtient ou définit la valeur qui indique si un objet **InkDisp** a été modifié depuis le dernier enregistrement de l’encre.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Lecture seule<br/>  | Obtient la collection de données définies par l’application.<br/>                                                                             |
| [**Traits**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Lecture seule<br/>  | Obtient la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenue dans l’objet **InkDisp** .<br/>                             |



 

## <a name="remarks"></a>Remarques

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

> [!Note]  
> la première instanciation de cet objet provoque également l’instanciation de GDI+. un effet secondaire est que si vous utilisez un seul objet ink dans une boucle et que vous le créez et le détruisez dans la boucle, vous risquez d’instancier GDI+. Cela peut entraîner une dégradation des performances dans votre application. Pour éviter cela, conservez une seule instance d’un objet Ink à tout moment pendant que votre application utilise de l’encre.

 

Un objet **InkDisp** est un conteneur de données de trait (point). Les données de trait, ou les points recueillis par le stylet, sont placés dans un objet **InkDisp** . La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contient les données de tous les traits de l’objet **InkDisp** .

L’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) et le contrôle [InkPicture](inkpicture-control-reference.md) collectent les points de l’appareil d’entrée et les place dans un objet **InkDisp** . Ces objets agissent essentiellement comme la source qui distribue l’encre dans un ou plusieurs objets **InkDisp** différents, qui jouent le rôle de conteneurs qui contiennent l’encre distribuée.

L’espace d’encre est un espace de coordonnées virtuelles auquel les coordonnées du contexte de tablette sont mappées. Cet espace est fixe à un système de coordonnées HIMETRIC. Dans les coordonnées d’espace d’encre, un déplacement de 0 à 1 est égal à 1 unité HIMETRIC. Ce mappage facilite la mise en relation de plusieurs objets **InkDisp** .

L’objet [**InkRenderer**](inkrenderer-class.md) gère les mappages entre l’encre et la fenêtre d’affichage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Interface IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

