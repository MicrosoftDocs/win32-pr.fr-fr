---
description: L’utilisation de symboles publics pour vos fichiers binaires image de mise à niveau et cible peut réduire d’environ une demi-taille des correctifs binaires.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Utilisation de symboles pour réduire la taille des correctifs binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5ccf33dbf3ffefbee909d99bd0204ea2f49aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514646"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Utilisation de symboles pour réduire la taille des correctifs binaires

L’utilisation de symboles publics pour vos fichiers binaires image de mise à niveau et cible peut réduire d’environ une demi-taille des correctifs binaires. La réduction réelle dépend des symboles utilisés. Notez que l’utilisation de symboles peut entraîner des temps de création de correctifs plus lents, car le traitement des fichiers de symboles est plus long.

Pour réduire la taille d’un correctif binaire à l’aide de symboles, vous devez fournir des symboles pour les fichiers binaires de l’image cible et de la mise à niveau. Spécifiez les symboles dans la colonne SymbolPaths de la table [TargetImages](targetimages-table-patchwiz-dll-.md) et la colonne SymbolPaths de la table [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) . Vous devez utiliser Visual C++ pour générer des symboles dans le format de fichier de la base de données du programme (PDB). Les versions plus récentes de Visual C++ fournissent toutes les informations nécessaires dans le fichier PDB. Les versions antérieures de Visual C++ également générer le format de fichier de débogage (DBG). Dans ce cas, la valeur SymbolsPaths doit spécifier l’emplacement des fichiers PDB et DBG.

Par exemple, le TargetImage pour un correctif peut être le package d’installation fourni avec Windows 2000 et qui installe la version 1.1.1029.0 de MSI.DLL. Le UpgradedImage peut être le package d’installation mis à jour fourni avec Windows 2000 avec Service Pack 1 (SP1) et qui installe la version 1.11.1314.0 de MSI.DLL. Deux fichiers de propriétés de création de correctifs (PCP) doivent alors être créés, l’un avec la colonne SymbolPaths des tables [TargetImages](targetimages-table-patchwiz-dll-.md) et [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) gauche null (vide) et l’autre avec la colonne SymbolPaths des tables TargetImages et UpgradedImages remplies avec l’emplacement des symboles pour les fichiers binaires. Dans ce cas, la taille du correctif généré sans utiliser de symboles peut être approximativement trois fois supérieure à la taille du correctif généré à l’aide de symboles.

L’utilitaire Mpatch.exe peut être utilisé pour tester la génération de correctifs binaires pour un seul fichier et pour vérifier si les symboles sont valides. L’utilitaire Mpatch.exe est inclus dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). La sortie de Mpatch.exe indique si les symboles ne correspondent pas.

Par exemple, entrez la ligne de commande suivante pour vérifier si les symboles sont valides.

**mpatch.exe-NEWSYMPATH : d : \\ Update-OLDSYMPATH : d : \\ target d : \\ cible \\example.dll d : \\ Update \\example.dll example. Pat**

Si les symboles ne se trouvent pas à l’emplacement correct, la sortie de Mpatch.exe peut inclure l’avertissement suivant.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



