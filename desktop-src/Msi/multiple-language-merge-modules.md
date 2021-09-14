---
description: Plusieurs modules linguistiques peuvent fournir des composants avec plusieurs langues différentes en tant que fichier composé unique.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Modules de fusion multilingues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d414cce484022bf81647110ac032d0db270d383
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416878"
---
# <a name="multiple-language-merge-modules"></a>Modules de fusion multilingues

Plusieurs modules linguistiques peuvent fournir des composants avec plusieurs langues différentes en tant que fichier composé unique. La conception et les fonctionnalités des modules de fusion multilingues sont similaires aux modules de langue unique. Un module de fusion multilingue a plusieurs langues dans la propriété [**Résumé du modèle**](template-summary.md) . La base de données d’un module de fusion de plusieurs langues contient toutes les informations de configuration pour plusieurs langues. Le fichier CAB MergeModule. cab à l’intérieur d’un module de fusion de plusieurs langues contient tous les fichiers de toutes les langues prises en charge.

Lors de l’application d’un fichier. msm multilingue à un fichier .msi, vous devez indiquer la langue finale du package d’installation après la fusion. Dans le cas d’un module de fusion de langue unique, la [table de fichiers](file-table.md) du module de fusion répertorie tous les fichiers présents dans le fichier CAB MergeModule. cab. Dans le cas d’un module de fusion à plusieurs langues, MergeModule. CABinet contient tous les fichiers pour chaque langue prise en charge par le module, mais seul le sous-ensemble de fichiers pour la langue finale est inséré dans la table de fichiers du module. L’outil de fusion doit s’assurer que le module fournit le sous-ensemble d’informations et de fichiers requis pour la langue finale demandée.

Chaque module de fusion a une langue par défaut spécifiée dans la colonne Language de la [table ModuleSignature](modulesignature-table.md). La langue par défaut d’un module de fusion est également indiquée comme étant la première ou seule langue dans la propriété [**Résumé du modèle**](template-summary.md) . Selon la langue finale demandée et la langue par défaut du module, l’outil de fusion peut appliquer des transformations de langage à un module de fusion à plusieurs langues afin qu’il puisse être ouvert dans la langue demandée, ou une approximation de la langue demandée. Les transformations de langage sont incorporées dans le module de fusion. Les outils de fusion doivent appliquer des transformations de langage en respectant les règles générales suivantes :

-   Si les langues par défaut et finales sont identiques, le module peut être fusionné sans utiliser de transformations de langage.
-   Si la langue par défaut est 0 (module indépendant de la langue), le module peut être fusionné sans utiliser de transformations de langage.
-   Si la langue finale n’est pas la langue par défaut, l’outil de fusion doit appliquer l’une des transformations de langue incorporées dans le module pour remplacer le module par le dernier langage ou une approximation de la langue finale.

Par exemple, aucune transformation de langue n’est requise si la langue finale est 1033 (anglais des États-Unis) et la langue par défaut du module est 1033 (anglais des États-Unis), 0 (langue neutre) ou 9 (anglais générique).

Les transformations linguistiques sont nécessaires si la langue finale est 1033 (anglais des États-Unis) et la langue par défaut est 1031 (allemand). Dans ce cas, l’outil de fusion peut commencer par Rechercher dans le module de langue multiple une transformation de langue incorporée sur 1033 (anglais des États-Unis). En cas d’échec, il peut ensuite rechercher une transformation dans une langue avec un ID de langue principal correspondant, même si l’ID de langue secondaire ne correspond pas. Par exemple, si l’outil ne trouve pas de transformation vers 1033 (anglais des États-Unis), il recherche une transformation à 9 (anglais générique). En cas d’échec, l’outil de fusion recherche une transformation à 0 (indépendant de la langue). Si toutes ces recherches d’une transformation appropriée échouent, le module ne s’ouvre pas.

Pour plus d’informations, consultez [création de modules de fusion multilingues](authoring-multiple-language-merge-modules.md).

 

 



