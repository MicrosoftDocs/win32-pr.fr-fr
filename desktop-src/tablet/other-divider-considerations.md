---
description: 'Prenez en compte les éléments suivants lorsque vous décidez quand et comment utiliser l’objet diviseur dans une application :'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Autres considérations relatives aux séparateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3328fd553a16aeee1e1dfa5459b78a45732a55494e0481950d730dab7ce0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449359"
---
# <a name="other-divider-considerations"></a>Autres considérations relatives aux séparateurs

Prenez en compte les éléments suivants lorsque vous décidez quand et comment utiliser l’objet [**diviseur**](inkdivider-class.md) dans une application :

-   L’objet [**diviseur**](inkdivider-class.md) est conçu pour séparer les dessins et les blocs d’écriture manuscrite, mais pas pour reconnaître les plus hauts niveaux de structure, tels que les tables ou les colonnes.
-   L’objet [**diviseur**](inkdivider-class.md) ne fournit pas d’interfaces spécifiquement pour la correction des résultats de l’analyse de la disposition.
-   L’utilisation du délai d’attente et du nombre d’heuristiques de trait pour ajouter ou supprimer plusieurs traits à la fois dans les traits de l’objet de [**séparateur**](inkdivider-class.md) peut améliorer les performances.

## <a name="reanalysis-considerations"></a>Considérations relatives à la réanalyse

Si vous envisagez d’utiliser l’objet [**diviseur**](inkdivider-class.md) dans une application où l’objet **diviseur** devra peut-être réanalyser de grandes quantités d’encre, gardez les points suivants à l’esprit.

### <a name="retaining-copies-of-ink-and-strokes"></a>Conservation des copies des encres et des traits

Une application peut conserver des copies d’objets [**Ink**](inkdisp-class.md) et [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) pour les éléments d’application qui peuvent être revisités plus tard dans la session de l’application. Cela élimine la nécessité de réanalyser l’objet **Ink** si l’utilisateur retourne à l’élément. Cette approche consiste à déconnecter de la mémoire pour de meilleures performances.

### <a name="data-reduction-heuristics"></a>Heuristique de réduction des données

Vous pouvez enregistrer les résultats d’analyse en tant que données d’application et implémenter des heuristiques pour déterminer quand réanalyser un ensemble de traits. Cette pratique réduirait la nécessité de réanalyser toute l’encre dans l’application entre les sessions d’application. Toutefois, il convient de veiller à préserver les limites des éléments structurels ou à réanalyser tous les traits des éléments affectés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**InkDivider, classe**](inkdivider-class.md)
</dt> <dt>

[Classe Microsoft. Ink. diviseur](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
