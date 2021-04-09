---
description: Le mécanisme cible dirigée permet aux rédacteurs de remapper des fichiers au moment de la restauration.
ms.assetid: c0b4ab26-2bb6-4b0f-b837-01057983b49b
title: Utilisation des cibles dirigées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd2e15ec873b87030a2d01be69d2c3e5f95a193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033996"
---
# <a name="working-with-directed-targets"></a>Utilisation des cibles dirigées

Le mécanisme [*cible dirigée*](vssgloss-d.md) permet aux rédacteurs de remapper des fichiers au moment de la restauration. Cela permet aux rédacteurs d’effectuer les opérations suivantes :

-   Spécifiez les nouveaux emplacements cibles (analogues à [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)) du demandeur.
-   Récupérez de l’espace disque en restaurant uniquement les parties nécessaires d’un fichier sur le disque, en particulier lors de la sauvegarde d’un fichier à l’aide du mécanisme de [*fichier partiel*](vssgloss-p.md) .
-   Modifiez le format de fichier pour répondre aux besoins actuels.

Tout fichier à utiliser avec une opération cible dirigée doit avoir une [*cible de restauration*](vssgloss-r.md) de VSS \_ RT \_ dirigée.

Une fois qu’un demandeur peut prendre en charge une opération cible dirigée, un enregistreur (lors de la gestion de l’événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ) utilise [**IVssComponent :: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) pour l’instance de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant au composant qui gère le fichier (ou le composant qui définit le jeu de composants qui contient le fichier) pour définir la manière dont le fichier doit être remappé lors de la restauration.

Dans à l’aide de [**IVssComponent :: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget), les enregistreurs spécifient le nom de fichier et le chemin d’accès utilisés pour sauvegarder le fichier, le nom de fichier et le chemin d’accès de sa destination de restauration (ces valeurs peuvent être les mêmes que le nom et le chemin d’accès du fichier d’origine) et les plages de fichiers source et de destination.

Comme avec les opérations de fichiers partielles, les listes de plages sont des paires d’offsets dans le fichier à sauvegarder (en octets) et la longueur de la section à restaurer (en octets), le décalage et la longueur séparés par un signe deux-points, et chaque paire séparée par une virgule : *Offset1 ***:**_length1_*_,_* * Offset2 ***:**_length2_. Chaque valeur est un entier 64 bits au format hexadécimal ou décimal.

Si un enregistreur doit utiliser le mécanisme cible dirigé pour que le demandeur restaure un fichier vers un nouvel emplacement, il aurait appelé [**IVssComponent :: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) avec le nom de fichier et le chemin d’accès d’origine, ainsi que le nouveau nom de fichier et le chemin d’accès et spécifiez les plages de destination source avec un décalage de zéro et une longueur égale à celle de la taille de fichier entière

Par exemple, si un enregistreur doit avoir un fichier de 200 Ko, C : \\ WriterData \\ index. dat, restauré sous la forme c : \\ WriterData \\ OldIndex. dat, la chaîne de la plage source et de destination serait «**0:204880**».

Pour remapper un fichier de grande taille partiellement sauvegardé, le demandeur utilise la plage source utilisée pour sauvegarder le fichier et une plage de destination qui réduira la taille du fichier. Les informations de la plage source peuvent être obtenues à l’aide de [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) pour l’instance de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant au composant qui gère le fichier (ou le composant qui définit le jeu de composants qui contient le fichier).

Si le fichier partiellement sauvegardé était initialement un fichier volumineux dont l’en-tête, octets 64-512, contient un nombre d’enregistrements et d’autres informations fréquemment mises à jour, et dont les données les plus récentes doivent se trouver dans les 65536 derniers octets du fichier (octets 0x1239E8577A à 0x1239E7577A), un enregistreur peut spécifier une liste de plages sources comme chaîne "**64:448, 0x1239E8577A : 65536**."

Si l’auteur souhaite remapper le fichier restauré pour contenir uniquement l’en-tête et les données les plus récentes, la liste de plages peut être la chaîne «**0:488488:65536**».

Avant d’effectuer une opération de restauration, un demandeur doit vérifier si des fichiers nécessitent une prise en charge cible dirigée.

Pour ce faire, le demandeur itère d’abord sur les enregistreurs avec des composants stockés dans son document composants de sauvegarde à l’aide de [**IVssBackupComponents :: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) et [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L’interface [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) est ensuite utilisée pour retourner des instances de l’interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) , qui fournit les méthodes [**IVssWriterComponentsExt :: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) et [**IVssWriterComponentsExt :: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) qui permettent au demandeur d’obtenir des instances [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Cela permet à un demandeur d’obtenir des candidats ciblés à l’aide de [**IVssComponent :: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) et de [**IVssComponent :: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) pour l’instance de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant au composant qui gère le fichier (ou le composant qui définit le jeu de composants qui contient le fichier).

 

 
