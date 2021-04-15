---
description: L’objet diviseur fournit des fonctionnalités d’analyse de la disposition qui classifient et regroupent les traits en différents éléments structurels.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Analyse de l’encre avec l’objet diviseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f1df175f8746e56cf6ebd1b222b3901fbef36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525317"
---
# <a name="ink-analysis-with-the-divider-object"></a>Analyse de l’encre avec l’objet diviseur

L’objet [diviseur](/previous-versions/ms583616(v=vs.100)) fournit des fonctionnalités d’analyse de la disposition qui classifient et regroupent les traits en différents éléments structurels.

## <a name="divider-object"></a>Objet diviseur

L’objet [diviseur](/previous-versions/ms583616(v=vs.100)) analyse les traits au fur et à mesure que vous les ajoutez ou supprimez. Vous pouvez récupérer la classification et le regroupement actuels des traits analysés dans un objet [DivisionResult](/previous-versions/ms583620(v=vs.100)) en appelant la méthode [Divide](/previous-versions/ms568936(v=vs.100)) de l’objet diviseur.

Les traits analysés par l’objet de [séparateur](/previous-versions/ms583616(v=vs.100)) sont conservés dans la propriété [Strokes](/previous-versions/ms582090(v=vs.100)) de l’objet diviseur. Comme une collection [Strokes](/previous-versions/ms552701(v=vs.100)) est une référence aux données d’entrée manuscrite et n’est pas les données proprement dites, les modifications apportées à l’objet [Ink](/previous-versions/ms583670(v=vs.100)) parent de la collection Strokes peuvent invalider la collection Strokes. Pour plus d’informations sur les données d’entrée manuscrite, consultez [données manuscrites](ink-data.md).

L’objet [diviseur](/previous-versions/ms583616(v=vs.100)) utilise un contexte de module de reconnaissance pour améliorer son analyse des segments de reconnaissance et pour générer un texte de reconnaissance pour les éléments d’écriture manuscrite. Si aucun contexte de module de reconnaissance n’est affecté à la propriété [RecognizerContext](/previous-versions/ms582089(v=vs.100)) de l’objet de séparateur ou que les module de reconnaissance ne sont pas installés, la fonction d’analyse de la disposition effectue la Division du segment de reconnaissance, et aucun texte n’est associé à l’objet [DivisionResult](/previous-versions/ms583620(v=vs.100)) . Pour plus d’informations sur la reconnaissance de l’encre, consultez [reconnaissance manuscrite](ink-recognition.md).

## <a name="divisionresult-object"></a>Objet DivisionResult

Chaque objet [DivisionResult](/previous-versions/ms583620(v=vs.100)) enregistre l’analyse de la disposition des traits contenus dans l’objet [diviseur](/previous-versions/ms583616(v=vs.100)) au moment de l’appel de la méthode de [Division](/previous-versions/ms568936(v=vs.100)) . L’objet DivisionResult stocke également une copie des traits qui ont été utilisés dans l’analyse.

L’objet [DivisionResult](/previous-versions/ms583620(v=vs.100)) regroupe les résultats de l’analyse par type d’élément structurel. La méthode [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) de l’objet DivisionResult retourne dans une collection [DivisionUnits](/previous-versions/ms583625(v=vs.100)) la collection de tous les éléments structurels d’un type donné. L’énumération [InkDivisionType](/previous-versions/ms552251(v=vs.100)) définit les types d’éléments reconnus par l’analyse de la disposition.

Le tableau suivant décrit les types d’éléments dans l’énumération [InkDivisionType](/previous-versions/ms552251(v=vs.100)) .



| Nom                 | Description                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Un segment de reconnaissance.<br/>                                                |
| Lignes<br/>      | Ligne d’écriture manuscrite qui contient un ou plusieurs segments de reconnaissance.<br/> |
| Paragraph<br/> | Bloc de traits qui contient une ou plusieurs lignes d’écriture manuscrite.<br/>    |
| Dessin<br/>   | Entrée manuscrite qui n’est pas du texte.<br/>                                                 |



 

L’illustration suivante montre un exemple des différents types d’éléments que l’objet [DivisionResult](/previous-versions/ms583620(v=vs.100)) reconnaît.

![illustration de différents types d’éléments reconnus par l’objet DivisionResult](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>Collection DivisionUnits et objets DivisionUnit

Chaque collection [DivisionUnits](/previous-versions/ms583625(v=vs.100)) est une copie du résultat de l’analyse de la disposition pour un seul type d’élément structurel. L’objet [DivisionUnit](/previous-versions/ms583624(v=vs.100)) représente un élément individuel dans la collection DivisionUnits. Chaque élément structurel a une référence aux traits qui composent l’élément. Si des détecteurs sont installés, un texte de reconnaissance est disponible pour les éléments d’écriture manuscrite. Les éléments de segment Line et Recognition incluent également une matrice de rotation qui peut faire pivoter les traits d’un élément de vertical à horizontal.

L' [exemple de rubrique diviseur d’encre](ink-divider-sample.md) montre comment utiliser un objet de [séparateur](/previous-versions/ms583616(v=vs.100)) avec des objets [Ink](/previous-versions/ms583670(v=vs.100)) pour effectuer une analyse de la disposition de l’encre.

Pour plus d’informations sur l’utilisation de l’analyse de l’encre, consultez [l’objet diviseur](the-divider-object.md).

 

