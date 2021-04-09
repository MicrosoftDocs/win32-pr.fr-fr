---
description: Le fichier de fonctionnalité de concert du produit d’origine, MNP2000, contient une erreur dans le fichier Concert.txt.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Planification d’un correctif logiciel de petite mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869633"
---
# <a name="planning-a-small-update-patch"></a>Planification d’un correctif logiciel de petite mise à jour

Le fichier de fonctionnalité de concert du produit d’origine, MNP2000, contient une erreur dans le fichier Concert.txt. Étant donné que Windows Installer a été utilisé pour l’installation et la configuration de l’application, des correctifs mineurs pour l’application peuvent être gérés par l’installation d’un package correctif de mise à jour de petite taille. Une [petite mise à jour](small-updates.md) apporte des modifications à un ou plusieurs fichiers d’application qui sont trop mineurs pour modifier le code du produit. L’exemple suivant montre comment créer un package de correctifs Windows Installer qui peut appliquer la petite mise à jour et fournir un correctif rapide au produit MNP2000.

Pour créer la petite mise à jour, commencez par obtenir une image entièrement non compressée du produit MNP2000 qui comprend l’erreur dans Concert.txt. L’image doit inclure MNP2000.msi et tous les fichiers sources décrits dans [planification de l’installation](planning-the-installation.md). Dans la discussion suivante, il s’agit de l’image cible. L’image cible doit être entièrement décompressée, car le processus de création de correctif ne peut pas générer de correctifs binaires pour les fichiers compressés dans des armoires. Placez le fichier. msi et tous les fichiers sources de l’image cible dans un dossier nommé target.

Ensuite, obtenez une image entièrement non compressée du produit MNP2000 avec un fichier Concert.txt qui est fixe. C’est ce que l’on appelle l’image mise à niveau dans la discussion suivante. Utilisez un outil d’édition de base de données d’installation, tel qu’Orca, pour mettre à jour le fichier. msi. Par exemple, si la taille de la Concert.txt corrigée est inférieure à celle d’origine, veillez à entrer la nouvelle taille dans le champ FileSize de la table file de l’image mise à niveau. Notez que, étant donné que le package a changé, vous devez attribuer un nouveau code de package dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) . Placez le fichier. msi et tous les fichiers sources de l’image mise à niveau dans un dossier nommé Upgraded.

Dans le cadre de cet exemple, supposez que la taille du fichier de Concert.txt change. Cela signifie que les champs FileSize dans les tables de fichiers de la base de données cible et mise à niveau contiennent des données différentes.

La [table de fichiers](file-table.md) suivante identifie l’enregistrement de l’image cible.



| Fichier        | -\_ | FileName    | FileSize | Version | Language | Attributs | Séquence |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concert     | Concert.txt | 1 000     |         |          | 0          | 1        |



 

La table de fichiers suivante identifie l’enregistrement à partir de l’image mise à niveau.



| Fichier        | -\_ | FileName    | FileSize | Version | Language | Attributs | Séquence |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concert     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> Le fichier doit avoir la même clé dans les [tables de fichiers](file-table.md) de l’image cible et de l’image mise à jour. Les valeurs de chaîne dans la colonne file des deux tables doivent être identiques. Les majuscules et les minuscules doivent également être identiques.
> 
> Suivez les instructions décrites dans [création d’un package de correctifs](creating-a-patch-package.md). Ne créez pas de package avec des clés de [table de fichiers](file-table.md) qui diffèrent uniquement par la casse, car [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md) appel Makecab.exe, ce qui ne respecte pas la casse et la génération de correctifs échoue.

[Continuer](creating-a-patch-creation-properties-file.md)

 

 



