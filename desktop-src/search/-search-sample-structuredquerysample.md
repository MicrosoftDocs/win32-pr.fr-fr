---
description: L’exemple de code StructuredQuerySample montre comment lire des lignes à partir de la console, les analyser à l’aide du schéma système et afficher les arborescences de condition résultantes.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab8f32a3ed58133893ed5c38c16c2ac242e9a28c6384a4e354bb6b0524c5a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462574"
---
# <a name="structuredquerysample"></a>StructuredQuerySample

L’exemple de code StructuredQuerySample montre comment lire des lignes à partir de la console, les analyser à l’aide du schéma système et afficher les arborescences de condition résultantes.

Cette rubrique contient les sections suivantes.

- [Requirements](#requirements)
- [Téléchargement de l’exemple](#downloading-the-sample)
- [Génération de l'exemple](#building-the-sample)
- [Exécution de l’exemple](#running-the-sample)
- [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Configuration requise

| Produit     | Version du produit          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 ou 10    |
| Kit de développement logiciel (SDK) Windows | 7,0 ou version ultérieure           |

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible à l’emplacement suivant.

| Emplacement      | URL du chemin                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [StructuredQuerySample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

## <a name="building-the-sample"></a>Génération de l'exemple

1. ouvrez Windows Explorer et accédez au répertoire du projet **StructuredQuerySample** .
2. Double-cliquez sur l’icône du fichier StructuredQuerySample. sln pour ouvrir le projet dans Visual Studio.

    > [!NOTE]  
    > le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version ultérieure. Cela n’aura pas d’impact sur le comportement de l’exemple.

3. Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1. accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de Windows Explorer.
2. à l’invite de commandes, entrez `StructuredQuerySample.exe` ou dans Windows Explorer, double-cliquez sur l’icône de StructuredQuerySample.exe.

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Informations de référence

[**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[**IQueryParserManager**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a>Autres exemples

[Rechercher des exemples de code](-search-samples-ovw.md)
