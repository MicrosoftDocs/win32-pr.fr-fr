---
description: La procédure suivante décrit un scénario permettant de générer une transformation qui masque définitivement une fonctionnalité.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Génération d’une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df605dd01a494089d2e6ecd38c8b3c6d03ecb5d6335e2348682e1af16f79faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635987"
---
# <a name="generating-a-transform"></a>Génération d’une transformation

La procédure suivante décrit un scénario permettant de générer une transformation qui masque définitivement une fonctionnalité.

**Pour masquer définitivement une fonctionnalité de produit**

1.  Copiez le package d’installation d’origine.
2.  Modifiez la copie en affectant à la colonne d’affichage de la [table de fonctionnalités](feature-table.md) la valeur zéro. Cela permet de masquer la fonctionnalité.
3.  Créez une transformation à partir du package d’installation d’origine vers les nouveaux packages d’installation en appelant [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Créez les informations de résumé dans la transformation en appelant [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

La transformation est ensuite prête à être appliquée lors de l’installation. Pour plus d’informations, consultez [application de transformations](applying-transforms.md).

 

 



