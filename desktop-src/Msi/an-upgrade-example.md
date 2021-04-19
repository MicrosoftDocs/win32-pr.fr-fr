---
description: Les sections suivantes présentent un exemple de création d’un package de mise à niveau pour l’application décrite dans un exemple d’installation.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Exemple de mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527855"
---
# <a name="an-upgrade-example"></a>Exemple de mise à niveau

Les sections suivantes présentent un exemple de création d’un package de mise à niveau pour l’application décrite dans [un exemple d’installation](an-installation-example.md). Un exemple d’interface utilisateur minimale pour cet exemple est fourni dans les [composants SDK Windows pour Windows Installer les développeurs](platform-sdk-components-for-windows-installer-developers.md) comme Uisample.msi de fichier. Si vous avez le kit de développement logiciel (SDK), vous avez accès à tous les outils et données nécessaires pour reproduire l’exemple de package d’installation, l’interface utilisateur et le package de mise à niveau.

Cet exemple montre comment créer un package Windows Installer qui met à niveau le produit hypothétique MNP2000 vers un nouveau produit appelé MNP2001. L’exemple de package de mise à niveau applique une mise à niveau majeure au produit qui nécessite la modification du code du produit. Pour plus d’informations sur les mises à niveau majeures, consultez la rubrique sur les [principales mises à](major-upgrades.md) niveau dans la section [correctifs et mises à niveau](patching-and-upgrades.md) .

L’exemple de package de mise à niveau présente les spécifications suivantes :

-   Pour bénéficier de cette mise à niveau vers MNP2001, un utilisateur doit avoir préalablement installé les versions 1,0 à 1,4 (inclusive) de la langue anglaise MNP2000 à l’aide de Windows Installer.
-   Lorsqu’un utilisateur tente d’installer le package de mise à niveau, la fonctionnalité de mise à niveau de Windows Installer recherche sur l’ordinateur de l’utilisateur tous les produits qui sont éligibles à la mise à niveau.
-   Windows Installer migre tous les paramètres de fonctionnalité du produit d’origine vers le produit mis à niveau.
-   Le programme d’installation supprime toutes les fonctionnalités obsolètes de l’ordinateur de l’utilisateur.
-   Le programme d’installation installe toutes les nouvelles fonctionnalités appartenant à la mise à niveau.
-   Une désinstallation du package de mise à niveau supprime le produit de l’ordinateur de l’utilisateur et ne restaure pas la version antérieure du produit.
-   L’exemple de mise à niveau met à jour les raccourcis vers les nouveaux fichiers et fonctionnalités.

    [Planification d’une mise à niveau majeure](planning-a-major-upgrade.md)

    [Importation de la base de données d’installation d’origine](importing-original-installation-database.md)

    [Mise à jour de la structure de répertoires pour une mise à niveau](updating-directory-structure-for-an-upgrade.md)

    [Mise à jour des fichiers et des attributs de fichier pour une mise à niveau](updating-files-and-file-attributes-for-an-upgrade.md)

    [Mise à jour des composants d’une mise à niveau](updating-components-for-an-upgrade.md)

    [Mise à jour des fonctionnalités pour une mise à niveau](updating-features-for-an-upgrade.md)

    [Mise à jour des raccourcis pour une mise à niveau](updating-shortcuts-for-an-upgrade.md)

    [Mise à jour de la table de mise à niveau pour une mise à niveau](updating-upgrade-table-for-an-upgrade.md)

    [Mise à jour des propriétés d’une mise à niveau](updating-properties-for-an-upgrade.md)

    [Mise à jour des tables de séquences pour une mise à niveau](updating-sequence-tables-for-an-upgrade.md)

    [Mise à jour des informations récapitulatives pour une mise à niveau](updating-summary-information-for-an-upgrade.md)

    [Validation de la mise à niveau d’une installation](validating-an-installation-upgrade.md)

 

 



