---
description: L’analyse de la disposition opère sur une collection de traits et classe les traits en éléments d’écriture manuscrite et de dessin. L’objet diviseur fournit l’accès aux fonctionnalités d’analyse de la disposition du Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Analyse de la disposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8131859dd7e4c7bd6927db42bd605541001ac0f1222bfbf27b0e59809d4b7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934819"
---
# <a name="layout-analysis"></a>Analyse de la disposition

L’analyse de la disposition opère sur une collection de [**traits**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) et classe les traits en éléments d’écriture manuscrite et de dessin. L’objet [**diviseur**](inkdivider-class.md) fournit l’accès aux fonctionnalités d’analyse de la disposition du Tablet PC.

Le tableau suivant décrit les types d’éléments structurels de l’énumération [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) dans lesquels l’objet [**diviseur**](inkdivider-class.md) classifie les traits.



| Type          | Description                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segment**   | Un segment de reconnaissance.<br/>                                                |
| **Ligne**      | Ligne d’écriture manuscrite qui contient un ou plusieurs segments de reconnaissance.<br/> |
| **Paragraph** | Bloc de traits qui contient une ou plusieurs lignes d’écriture manuscrite.<br/>    |
| **Dessin**   | Entrée manuscrite qui n’est pas une écriture manuscrite.<br/>                                          |



 

L’objet [**diviseur**](inkdivider-class.md) possède une collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , que l’objet **diviseur** analyse dynamiquement chaque fois que vous ajoutez ou supprimez la collection. L’objet de **séparateur** n’est pas sérialisable, et vous ne pouvez pas enregistrer son état d’analyse. Par conséquent, l’objet **diviseur** est conçu pour les applications qui doivent faire la différence entre l’écriture de texte mixte et l’entrée de dessin, mais n’ont pas besoin de réanalyser de grandes quantités d’encre entre les sessions.

Vous pouvez obtenir un instantané statique du résultat de l’analyse actuelle, qui est retourné dans un objet [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) . Vous pouvez obtenir des objets [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , chacun représentant un élément structurel unique d’un objet **DivisionResult** . Les objets **DivisionResult** et **DivisionUnit** ne sont pas sérialisables. Toutefois, les informations d’état de ces objets sont disponibles.

L’objet [**diviseur**](inkdivider-class.md) fonctionne uniquement avec l’écriture manuscrite de gauche à droite. Pour que l’objet **diviseur** analyse les langues verticales telles que le chinois correctement, les caractères doivent être dessinés de gauche à droite et de haut en bas.

 

