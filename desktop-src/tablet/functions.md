---
description: Cette section contient les fonctions principales pour Tablet PC.
ms.assetid: 8f94a82c-de93-4649-a9b5-0adcbe01333d
title: Fonctions principales de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb9e58300321f2b483cc062472950f5d252a292dc1380b3e5c030993ddbe6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967541"
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



 

 

 
