---
description: Les enregistreurs peuvent affiner les performances de différents types de sauvegarde au niveau du jeu de fichiers en indiquant à l’aide d’un type de sauvegarde de spécification de fichier, indiqué par un masque de bits ou une opération de bits OR des membres de l' \_ \_ \_ énumération du type de sauvegarde spécification de fichier VSS \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Prise en charge des schémas au niveau du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413370"
---
# <a name="file-level-schema-support"></a>Prise en charge des schémas au niveau du fichier

Les enregistreurs peuvent affiner les performances de différents types de sauvegarde au niveau du [*jeu de fichiers*](vssgloss-f.md) en indiquant à l’aide d’un type de sauvegarde de spécification de fichier, indiqué par un masque de bits ou une opération de bits or des membres de l’énumération du type de sauvegarde spécification de [**\_ fichier \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) .

Pour les types de sauvegarde spécifiés, le writer indique les éléments suivants :

-   S’il est nécessaire de copier le cliché instantané du volume pour sauvegarder correctement un jeu de fichiers. Par exemple, si les fichiers d’un jeu de fichiers ne sont pas ouverts exclusivement par le writer et qu’il peut s’assurer qu’il est stable, aucun cliché instantané n’est nécessaire.
-   Si le demandeur doit effectuer la sauvegarde de telle sorte que, quelle que soit l’heure de la dernière modification ou d’autres problèmes, la version des fichiers du jeu de fichiers en cours à la sauvegarde sera restaurée. En général, cela signifie que le jeu de fichiers est copié dans le cadre de la sauvegarde.

Les valeurs du [**\_ type de \_ \_ sauvegarde spec \_ de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) qui indiquent l’exigence de cliché instantané sont :

-   \_FSBT VSS \_ tous les \_ instantanés \_ requis
-   \_ \_ instantané complet VSS \_ FSBT \_ requis
-   \_ \_ instantané différentiel FSBT \_ VSS \_ requis
-   \_instantané FSBT \_ incrémentiel VSS \_ \_ requis
-   \_instantané de \_ Journal FSBT VSS \_ \_ requis

Les valeurs du [**\_ type de \_ \_ sauvegarde spécification \_ de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) qui indiquent la nécessité de sauvegarder un fichier sont les suivantes :

-   \_sauvegarde VSS FSBT \_ toutes les \_ sauvegardes \_ requises
-   \_ \_ sauvegarde complète VSS \_ FSBT \_ requise
-   \_ \_ sauvegarde différentielle FSBT \_ VSS \_ requise
-   \_sauvegarde VSS FSBT \_ \_ \_ requise
-   \_sauvegarde du \_ Journal FSBT VSS \_ \_ requise

Par défaut, les jeux de fichiers sont marqués avec un type de sauvegarde de spécification de fichier VSS \_ FSBT \_ toutes les \_ sauvegardes \_ nécessaires \| VSS \_ FSBT \_ tous les \_ instantanés \_ requis, ce qui signifie qu’un cliché instantané est toujours requis pour gérer les fichiers du jeu de fichiers et que les fichiers doivent être copiés dans tous les types de sauvegardes.

 

 



