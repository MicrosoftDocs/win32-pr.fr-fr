---
description: Les options de restauration permettent aux demandeurs de communiquer des options de restauration personnalisées aux enregistreurs.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Définition des options de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529153"
---
# <a name="setting-vss-restore-options"></a>Définition des options de restauration VSS

Les options de restauration permettent aux demandeurs de communiquer des options de restauration personnalisées aux enregistreurs.

## <a name="restore-options"></a>Options de restauration

La standardisation du format des options de restauration permet aux rédacteurs et aux demandeurs de gérer les demandes personnalisées courantes. Les options de restauration sont définies par le demandeur en appelant la méthode [**IVssBackupComponents :: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) jusqu’à une fois par composant sélectionné pour la sauvegarde avant d’appeler la méthode [**IVssBackupComponents ::P Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) . La chaîne transmise dans le paramètre *wszRestoreOptions* à la méthode **SetRestoreOptions** peut contenir plusieurs valeurs, comme décrit ci-dessous.

## <a name="format"></a>Format

Le format des options de restauration est une ou plusieurs paires nom/valeur séparées par des virgules, et le nom est éventuellement préfixé avec le nom du sous-composant auquel il s’applique. Les noms des composants et des options ne respectent pas la casse. Le respect de la casse des valeurs est déterminé par le writer. Par exemple :

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

Dans cet exemple, « option1 » s’applique uniquement au sous-composant « child1 » et à ses descendants, « option2 » s’applique à tous les composants et à leurs descendants, et « option3 » s’applique uniquement aux sous-composants « enfant2 \\ Grandchild3 » et à ses descendants.

La méthode [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) peut uniquement être appelée sur des composants sélectionnables pour la sauvegarde, alors que les nœuds descendants ne peuvent pas être sélectionnables pour la sauvegarde, ils peuvent être sélectionnables pour la restauration.

## <a name="common-restore-options"></a>Options de restauration courantes

Ces options de restauration courantes ont été définies pour améliorer l’interopérabilité entre les enregistreurs et les demandeurs.

-   Manière

    L’option « authoritative » prend en charge plusieurs valeurs « Item », mais une seule valeur « All ».

    Ce composant entier fait autorité.

    ``` syntax
    "Authoritative"="All"
    ```

    Seul l’élément spécifié fait autorité. Le format de l’élément nommé est défini par le writer. Les désignations courantes sont « \* » pour indiquer tous les fichiers, « ... » pour indiquer tous les fichiers et sous-répertoires du composant spécifié.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Restaurer par progression

    Après la restauration d’une base de données, les rédacteurs restaurent généralement les journaux pour mettre à jour la base de données. En cas de restaurations incrémentielles ou différentielles, le demandeur utilise la méthode [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) pour contrôler partiellement le comportement de gestion des journaux : cette option de restauration permet un contrôle plus granulaire.

    Ne pas restaurer les journaux.

    ``` syntax
    "Roll Forward"="None"
    ```

    Parcourez tous les journaux.

    ``` syntax
    "Roll Forward"="All"
    ```

    Restaure les journaux jusqu’au point spécifié. Le format du point spécifié est défini par le writer.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Nouveau nom du composant

    Un enregistreur peut vouloir restaurer un nouveau nom d’un composant. Par exemple, la restauration d’une base de données avec un nom différent pour restaurer un élément individuel ; Si vous restaurez le même nom, toutes les données nous recommandons que les rédacteurs acceptent un chemin logique et un nom de composant valides comme valeur. Ce sera souvent utilisé avec une [*cible dirigée*](vssgloss-d.md).

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



