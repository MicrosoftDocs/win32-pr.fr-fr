---
description: Commencez à créer le package de mise à niveau en copiant le package d’installation et l’arborescence du répertoire source du produit d’origine.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importation de la base de données d’installation d’origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521836"
---
# <a name="importing-original-installation-database"></a>Importation de la base de données d’installation d’origine

Commencez à créer le package de mise à niveau en copiant le package d’installation et l’arborescence du répertoire source du produit d’origine. Des instructions sur la création du package d’installation pour MNP2000 sont fournies dans [un exemple d’installation](an-installation-example.md). Vous devez copier le contenu des dossiers suivants :

C : \\ exemple de \\MNP2000.msi

C : \\ exemple de \\ bloc-notes\\

C : \\ exemple de \\ binaire\\

C : \\ exemple d' \\ icône\\

Mettez à jour le contenu du dossier Notepad afin qu’il corresponde à la source décrite dans [planification d’une mise à niveau majeure](planning-a-major-upgrade.md). Supprimez tous les fichiers sources obsolètes, tels que Baseball.txt, et remplacez par les fichiers mis à jour, tels que Baseba01.txt. Ajoutez les nouveaux fichiers supplémentaires fournis par la mise à niveau, par exemple Opera01.txt.

Renommez MNP2000.msi MNP2001.msi. Dans les étapes suivantes, vous allez utiliser un éditeur de table pour modifier cette base de données dans le fichier. msi pour la mise à niveau. Les tables de base de données qui ne sont pas explicitement modifiées dans les sections suivantes sont identiques aux tables de la base de données du produit d’origine, MNP2000.msi.

[Continuer](updating-directory-structure-for-an-upgrade.md)

 

 



