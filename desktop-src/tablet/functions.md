---
description: Cette section contient les fonctions principales pour Tablet PC.
ms.assetid: 8f94a82c-de93-4649-a9b5-0adcbe01333d
title: Fonctions principales de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9d0369a223959f011612b5aefc820a3668eeff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412296"
---
# <a name="core-tablet-pc-functions"></a>Fonctions principales de Tablet PC

Cette section contient les fonctions principales pour Tablet PC.

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                         | Description                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddOneStroke**](addonestroke.md)                             | Ajoute un nouvel objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) à l’objet [**InkDivider**](inkdivider-class.md) qui a été passé.                                                                 |
| [**CallDivide**](calldivide.md)                                 | Récupère des informations d’analyse à partir de l’objet [**InkDivider**](inkdivider-class.md) .                                                                                                              |
| [**CallDivideResults**](calldivideresults.md)                   | Retourne les résultats de l’analyse à partir de l’objet [**InkDivider**](inkdivider-class.md) .                                                                                                                    |
| [**CallDivideResultsStrokeIds**](calldivideresultsstrokeids.md) | Récupère les propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) du mot, de la ligne, du paragraphe ou du dessin correspondants, déterminés par l’analyse de l’encre. |
| [**CreateInkDivider**](createinkdivider.md)                     | Instancie une implémentation de l’interface [**InkDivider**](inkdivider-class.md) et retourne son handle.                                                                                      |
| [**DeleteInkDivider**](deleteinkdivider.md)                     | Supprime un objet [**InkDivider**](inkdivider-class.md) et libère les ressources associées.                                                                                                         |
| [**InvokeIDispatch**](invokeidispatch.md)                       | Appelle la fonctionnalité d’assistance pour l’interface IDispatch.                                                                                                                                           |
| [**RecognizerContextSet**](recognizercontextset.md)             | Teste si l’objet [**InkDivider**](inkdivider-class.md) peut utiliser la classe [**InkRecognizerContext**](inkrecognizercontext-class.md) pour analyser des mots.                                      |
| [**RemoveStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-removestrokes)                | Supprime les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) du [**InkDivider**](inkdivider-class.md).                                                                                           |
| [**SetLineHeight**](setlineheight.md)                           | Définit la propriété [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) sur l’objet [**InkDivider**](inkdivider-class.md) .                                                                                 |
| [**SetLineRecoCallback**](setlinerecocallback.md)               | Définit une fonction de rappel à utiliser pendant la reconnaissance de ligne.                                                                                                                                        |



 

 

 
