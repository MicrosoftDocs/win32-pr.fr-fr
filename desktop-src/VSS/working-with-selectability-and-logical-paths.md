---
description: La participation d’un enregistreur dans le cadre d’une opération de sauvegarde ou de restauration, et laquelle de ses données sont enregistrées, dépend des composants qui sont explicitement inclus dans le document des composants de sauvegarde d’un demandeur et de la relation entre ces composants et du chemin logique des autres composants dans le document de métadonnées du writer.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Utilisation de la sélectivité et des chemins logiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f008b086ea50a1695a76f8b7beecab473b767fb1e2835fd5686197bb1b583175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344252"
---
# <a name="working-with-selectability-and-logical-paths"></a>Utilisation de la sélectivité et des chemins logiques

La participation d’un enregistreur dans le cadre d’une opération de sauvegarde ou de restauration, et laquelle de ses données sont enregistrées, dépend des composants qui sont [*explicitement inclus*](vssgloss-e.md) dans le document des composants de sauvegarde d’un demandeur et de la relation entre ces composants et du chemin logique des autres composants dans le document de métadonnées du writer.

Les enregistreurs sans composants ajoutés au document du composant de sauvegarde d’un demandeur avant la génération d’un événement [*PrepareForBackup*](vssgloss-p.md) (dans le cas d’opérations de sauvegarde) ou d’un événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (dans le cas d’opérations de restauration) ne reçoivent aucun événement après ce point et ne participent pas à l’opération de sauvegarde ou de restauration.

Toutefois, la liberté d’un demandeur d’inclure ou d’exclure un composant donné dans une sauvegarde ou une restauration est régie par les éléments suivants :

-   Toute hiérarchie qui existe entre les composants gérés par un enregistreur et exprimée par des [ *chemins logiques*](vssgloss-l.md)
-   Si le composant est désigné comme étant [ *sélectionnable pour la sauvegarde*](vssgloss-s.md)
-   Indique s’il est désigné comme [ *sélectionnable pour la restauration*](vssgloss-s.md)
-   Indique s’il existe une dépendance explicite entre un composant donné dans un writer donné et d’autres composants dans d’autres enregistreurs

Vous trouverez plus d’informations sur ces problèmes dans les rubriques suivantes :

-   [Chemin logique des composants](logical-pathing-of-components.md)
-   [Utilisation de la sélectivité pour la sauvegarde](working-with-selectability-for-backup.md)
-   [Utilisation de la sélectivité pour la restauration et les sous-composants](working-with-selectability-for-restore-and-subcomponents.md)
-   [Sélection et utilisation des propriétés de composant](selectability-and-working-with-component-properties.md)
-   [Dépendances entre les composants gérés par différents Writers](dependencies-between-components-managed-by-different-writers.md)

 

 



