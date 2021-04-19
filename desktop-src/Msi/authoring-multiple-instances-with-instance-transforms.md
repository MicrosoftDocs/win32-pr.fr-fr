---
description: Pour installer plusieurs instances d’un produit à partir d’un Windows Installer Package, vous devez créer un package d’installation de base pour le produit et une transformation d’instance pour chaque instance à installer en plus de l’instance de base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Création de plusieurs instances à l’aide de transformations d’instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544810"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Création de plusieurs instances à l’aide de transformations d’instance

Pour installer plusieurs instances d’un produit à partir d’un Windows Installer Package, vous devez créer un package d’installation de base pour le produit et une transformation d’instance pour chaque instance à installer en plus de l’instance de base. Utilisez les instructions suivantes lors de la création de votre package de base et des transformations :

-   Votre application de configuration peut vérifier la présence du programme d’installation qui s’exécute sur une version de Windows Vista, Windows Server 2003, Windows XP avec Service Pack 1 (SP1) et le Windows Installer 3,0 Redistributable. N’importe laquelle de ces versions du programme d’installation (ou version ultérieure) est requise pour installer plusieurs instances à partir d’un package unique à l’aide d’un code de produit – modification de la transformation.
-   Chaque instance doit avoir un code de produit et un identificateur d’instance uniques. Vous pouvez définir une propriété dans le package de base, dont la valeur peut être définie sur l’identificateur d’instance.
-   Pour que les fichiers de chaque instance restent isolés, le package de base doit installer les fichiers dans un emplacement de répertoire qui dépend de l’identificateur d’instance.
-   Pour que les données de chaque instance ne soient pas isolées, le package de base doit collecter des données qui ne sont pas des fichiers dans des ensembles de composants pour chaque instance. Les composants appropriés doivent ensuite être installés en fonction des instructions conditionnelles qui dépendent de l’identificateur d’instance.
-   Créez une transformation d’instance pour chaque instance installée en plus de l’instance de base. Le package de base peut installer sa propre instance.
-   La transformation d’instance doit modifier le code de produit et l’identificateur pour chaque instance.
-   Il est recommandé que la transformation du produit change également le nom du produit afin que l’instance soit facilement distinguée dans Ajout/suppression de programmes via le panneau de configuration.
-   Si la transformation d’instance installe des fichiers, ceux-ci doivent être installés dans un répertoire qui dépend de l’identificateur d’instance.
-   Toutes les données qui ne sont pas de type fichier, telles que les clés de Registre, doivent inclure le nom de l’instance dans leur chemin d’accès pour éviter les collisions. Pour ce faire, vous pouvez utiliser la propriété dont la valeur est l’identificateur d’instance dans le chemin d’accès, comme indiqué dans l’exemple suivant d’une [table de Registre](registry-table.md).



| Registre | Root | Clé                                            | Nom         | Valeur           | -\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Logiciel \\ Microsoft \\ MyProduct \\ \[ InstanceID\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Pour plus d’informations, consultez [installation de plusieurs instances de produits et correctifs](installing-multiple-instances-of-products-and-patches.md) et [installation de plusieurs instances à l’aide de transformations d’instance](installing-multiple-instances-with-instance-transforms.md).

 

 



