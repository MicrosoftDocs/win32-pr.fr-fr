---
description: Les composants sont définis par les writers et instanciés dans leur document de métadonnées d’écriture en réponse à un événement d’identification au démarrage d’une opération de sauvegarde (consultez vue d’ensemble de l’initialisation de la sauvegarde) lorsque le document de métadonnées de l’enregistreur est rempli.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Définition des composants par les rédacteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5383e9bc87620f23bb2a3ab067c1913a323782
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413387"
---
# <a name="definition-of-components-by-writers"></a>Définition des composants par les rédacteurs

Les composants sont définis par les writers et instanciés dans leur document de métadonnées d’écriture en réponse à un [*événement d’identification*](vssgloss-i.md) au démarrage d’une opération de sauvegarde (consultez [vue d’ensemble de l’initialisation de la sauvegarde](overview-of-backup-initialization.md)) lorsque le document de métadonnées de l’enregistreur est rempli.

Quand vous créez un composant dans son document de métadonnées d’écriture à l’aide de [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) et de [**IVssCreateWriterMetadata :: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), un enregistreur doit spécifier les éléments suivants :

-   Indique si le composant peut être [ *sélectionné pour la sauvegarde*](vssgloss-s.md)
-   Un type de composant
-   Nom de composant (qui doit être unique non seulement dans une [*instance de writer*](vssgloss-w.md) donnée, mais dans toutes les instances d’écriture)
-   Si les métadonnées spécifiques au writer sont associées au composant
-   Si l’enregistreur requiert une notification après une sauvegarde réussie

Les enregistreurs peuvent éventuellement spécifier :

-   [*Chemin logique*](vssgloss-l.md) d’un composant (qui doit être unique non seulement dans une instance de writer donnée, mais dans toutes les instances d’écriture)
-   Description d’un composant (ou légende)
-   Icône à utiliser avec les interfaces graphiques pour indiquer le composant

Il n’est pas nécessaire qu’un composant contienne réellement des fichiers. Ce type de composant vide ou « factice » peut être utile pour organiser les composants. Ce type de composant peut être utilisé pour définir un [*jeu de composants*](vssgloss-c.md) et un composant d’enregistreur (consultez [chemin logique des composants](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Configuration de l’Organisation des composants

La définition de la [*sélectivité*](vssgloss-s.md) d’un composant (sa [*sélectivité pour la sauvegarde*](vssgloss-s.md)et [*sa sélectivité pour la restauration*](/windows)) et de ses [*chemins logiques*](vssgloss-l.md) permet à un enregistreur d’imposer ou de rendre facultatif l’inclusion de certains composants dans une opération de sauvegarde ou de restauration, et de regrouper des composants en [*ensembles*](vssgloss-c.md) de composants avec un composant sélectionnable agissant comme point d’entrée pour l’ensemble du groupe.

L’appartenance à ces regroupements détermine les composants qui seront utilisés pendant les opérations de sauvegarde et de restauration. À l’aide de « sélectionnable » pour signifier qu’il est sélectionnable pour l’opération de sauvegarde et sélectionnable pour la restauration pour l’opération de restauration, les développeurs doivent comprendre ce qui suit :

-   Si des composants gérés par un writer donné sont sauvegardés, un demandeur doit [*inclure explicitement*](vssgloss-e.md) tous les [*composants*](vssgloss-c.md) non sélectionnables sans les ancêtres sélectionnables dans leur [*chemin logique*](vssgloss-l.md) vers le document des composants de sauvegarde et les sauvegarder et les restaurer en tant que groupe.
-   Un demandeur a la possibilité d’ajouter explicitement des composants sélectionnables au document des composants de sauvegarde pendant les opérations de sauvegarde et de restauration ; une fois ajouté, le composant doit être sauvegardé ou restauré.
-   Si un composant peut être sélectionné, le composant et tous ses sous- [*composants*](vssgloss-s.md) (tels que définis par les chemins logiques) forment un jeu de composants, qui peut être traité comme une unité unique qui peut éventuellement participer à des opérations de sauvegarde et de restauration.
-   Un demandeur n’ajoute jamais explicitement un composant non sélectionnable avec des ancêtres sélectionnables, un sous-composant d’un jeu de composants, à son document de composants de sauvegarde pendant les opérations de sauvegarde et de restauration. Ces composants doivent être [*inclus implicitement*](/windows) si leur ancêtre sélectionnable est explicitement ajouté, auquel cas ils doivent être sauvegardés ou restaurés (voir [utilisation de composants par le demandeur](use-of-components-by-the-requestor.md)).
-   Un composant sélectionnable avec un ancêtre sélectionnable est toujours un sous- [*composant*](vssgloss-s.md) (un membre d’un jeu de composants) et peut être inclus implicitement si son ancêtre sélectionnable est explicitement inclus dans l’opération. Dans ce cas, ses informations ne sont pas ajoutées au document sur les composants de sauvegarde. Si son ancêtre sélectionnable n’est pas inclus dans l’opération, le composant peut être explicitement sélectionné pour être inclus dans l’opération, auquel cas ses informations sont incluses dans le document sur les composants de sauvegarde.
-   Un sous-composant inclus implicitement dans une sauvegarde peut être inclus explicitement dans une opération de restauration, indépendamment de l’état d’un ancêtre sélectionnable, s’il peut être sélectionné pour la restauration. Tout élément sélectionnable pour le sous-composant Restore inclus lors d’une opération de restauration doit avoir ses informations ajoutées au document des composants de sauvegarde.
-   Un enregistreur qui n’avait aucun composant explicitement ajouté au document des composants de sauvegarde avant la génération de [*PrepareForBackup*](vssgloss-p.md) et les événements de [*prérestauration*](vssgloss-p.md) ne recevront pas d’événements VSS supplémentaires.

Pour plus d’informations, consultez [utilisation de la sélectivité et des chemins d’accès logiques](working-with-selectability-and-logical-paths.md).

## <a name="adding-files-to-a-component"></a>Ajout de fichiers à un composant

Un composant contient des informations de fichier sous la forme d’un [*jeu de fichiers*](vssgloss-f.md) qui contient :

-   Répertoire racine des fichiers dans le composant.
-   Spécification de fichier pour les fichiers dans le composant.
-   Indicateur qui spécifie si la spécification du composant est récursive.

Selon le type de composant, qui peut être une base de données ou un groupe de fichiers, et (dans le cas des composants de base de données) si les fichiers à charger sont des fichiers de données ou des fichiers journaux, un enregistreur appelle [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) pour ajouter un jeu de fichiers.

Lorsque vous utilisez ces fonctions, vous devez spécifier les fichiers à ajouter au jeu de fichiers comme suit :

-   *wszPath*: chemin d’accès au répertoire qui contient les fichiers à ajouter au jeu de fichiers. Si le paramètre *bRecursive* est défini sur **true**, le paramètre *wszPath* spécifie une hiérarchie de répertoires à traverser de manière récursive, et tous les répertoires doivent être recréés, y compris les répertoires vides.
-   *wszFilespec*: cette chaîne spécifie les fichiers de chaque répertoire à ajouter au jeu de fichiers.

Par exemple, supposons que la structure de répertoires suivante existe :

<dl> C : \\ Directory1 \\File1.txt  
C : \\ Directory1 \\File2.txt  
C : \\ Directory1 \\ Directory2 \\File1.txt  
C : \\ Directory1 \\ Directory2 \\File2.txt  
C : \\ Directory1 \\ Directory3\\  
</dl>

Si le writer spécifie « C : \\ Directory1 » pour *wszPath*, « fichier1. \* » pour *wszFilespec* et **true** pour *bRecursive*, le demandeur doit inclure les fichiers suivants :

<dl> C : \\ Directory1 \\File1.txt  
C : \\ Directory1 \\ Directory2 \\File1.txt  
</dl>

Si, à la place, le writer spécifie « C : \\ Directory1 » pour *wszPath*, « \* » pour *wszFilespec* et **true** pour *bRecursive*, le demandeur doit inclure les fichiers suivants :

<dl> C : \\ Directory1 \\File1.txt  
C : \\ Directory1 \\File2.txt  
C : \\ Directory1 \\ Directory2 \\File1.txt  
C : \\ Directory1 \\ Directory2 \\File2.txt  
</dl>

Si le writer spécifie « C : \\ Directory1 » pour *wszPath*, « \* » pour *WszFilespec* et **false** pour *bRecursive*, le demandeur doit inclure les fichiers suivants :

<dl> C : \\ Directory1 \\File1.txt  
C : \\ Directory1 \\File2.txt  
</dl>

Dans tous les exemples précédents, chaque fois que le writer spécifie **true** pour *bRecursive*, le répertoire vide C : \\ Directory1 \\ Directory3 \\ doit être recréé.

Pour un jeu de fichiers ajouté à un composant de groupe de fichiers, dans les cas où les fichiers qui se trouvent actuellement sur le disque ne sont pas dans ce que le rédacteur considère comme l’emplacement approprié ou par défaut, un enregistreur a la possibilité d’ajouter un autre chemin d’accès. Dans ce cas, la définition du chemin d’accès du jeu de fichiers contient l’emplacement normal des fichiers et de l’emplacement où les fichiers doivent être restaurés, tandis que l’autre chemin d’accès contient l’emplacement actuel des fichiers à sauvegarder.

Tous les fichiers du jeu de fichiers doivent exister au moment de la sauvegarde. Les demandeurs doivent supposer que tous les fichiers répertoriés dans le jeu de fichiers sont requis pour la sauvegarde et échoueront à la sauvegarde si des fichiers sont manquants. Notez que lorsque « \* » est spécifié pour le paramètre *wszFilespec* , il peut correspondre à zéro ou plusieurs fichiers.

Notez que les attributs du document de métadonnées de l’enregistreur sont des mappages d’emplacements alternatifs, des fichiers explicitement inclus et exclus, et que les méthodes de restauration sont définies au niveau du writer, et non au niveau du composant. (Pour plus d’informations, consultez [utilisation du document de métadonnées de l’enregistreur](working-with-the-writer-metadata-document.md).)

## <a name="component-definition-for-backup-and-restore-operations"></a>Définition de composant pour les opérations de sauvegarde et de restauration

Les opérations de restauration et de sauvegarde génèrent nécessairement un [*événement d’identification*](vssgloss-i.md), et pour les sauvegardes et les restaurations, elles sont gérées par la même méthode [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

Pendant les opérations de sauvegarde, les demandeurs utilisent les informations retournées par les méthodes [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) d’un writer pour déterminer quels Writers sont présents sur le système, puis pour déterminer ceux de leurs fichiers à sauvegarder.

Pendant les opérations de restauration, les informations retournées par l’événement [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) d’un writer sont utilisées uniquement pour établir l’identité et l’état des enregistreurs actuellement présents sur le système. les informations de spécification de fichier générées au cours d’une restauration ne sont pas utilisées. Au lieu de cela, les documents de métadonnées d’écriture stockés au moment de la sauvegarde sont utilisés pour obtenir ces données.

Une fois générés au cours d’une opération de sauvegarde, les informations du composant d’écriture, ainsi que le reste des informations de l’enregistreur, sont enregistrées pour être récupérées afin de prendre en charge les opérations de restauration. Il incombe généralement au demandeur de stocker ces informations.

 

 
