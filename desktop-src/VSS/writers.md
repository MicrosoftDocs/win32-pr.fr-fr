---
description: Les enregistreurs sont des applications ou des services qui stockent des informations persistantes dans des fichiers sur disque et qui fournissent les noms et les emplacements de ces fichiers aux demandeurs à l’aide de l’interface de cliché instantané.
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ca409e8dc6153a6b3e2b747dc23cc391055471
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191835"
---
# <a name="writers"></a>Writers

Les [*enregistreurs*](vssgloss-w.md) sont des applications ou des services qui stockent des informations persistantes dans des fichiers sur disque et qui fournissent les noms et les emplacements de ces fichiers aux demandeurs à l’aide de l’interface de cliché instantané.

Pendant les opérations de sauvegarde, les rédacteurs garantissent que leurs données sont inversées et stables, adaptées au cliché instantané et à la sauvegarde. Les enregistreurs collaborent avec les restaurations en déverrouillant les fichiers lorsque cela est possible et en indiquant d’autres emplacements si nécessaire.

Si aucun Writer n’est présent au cours d’une opération de sauvegarde VSS, vous pouvez toujours créer un cliché instantané. Dans ce cas, toutes les données du volume copié par cliché instantané seront dans l' [*État de cohérence*](vssgloss-c.md)en cas d’incident.

## <a name="writer-state"></a>État de l’enregistreur

Les Writers conservent leur état dans un objet de métadonnées XML, le [*document de métadonnées*](vssgloss-w.md)de l’enregistreur.

Les métadonnées de ce writer sont la seule structure de données qui contient le [*jeu de fichiers*](vssgloss-f.md)(chemin d’accès, spécification de fichier et indicateur de récurrence) des données à sauvegarder et à restaurer.

Le document de métadonnées de l’enregistreur organise les jeux de fichiers du writer en groupes ou [*composants*](vssgloss-c.md). La relation entre l’un de ces composants et les opérations de sauvegarde et de restauration sur les autres composants gérés par le writer est décrite dans le document de métadonnées de l’enregistreur par la sélectivité du composant [*pour la sauvegarde*](vssgloss-s.md), sa [*sélectivité pour la restauration*](vssgloss-s.md)et ses [*chemins logiques*](vssgloss-l.md). (Pour plus d’informations, consultez Configuration de l' [Organisation des composants](definition-of-components-by-writers.md) et [utilisation de la sélectivité et des chemins logiques](working-with-selectability-and-logical-paths.md).)

Ce document contient également des informations supplémentaires qui régissent la restauration des fichiers et d’autres problèmes.

Le demandeur a besoin des métadonnées de l’enregistreur, conjointement avec son propre document de composants de sauvegarde, pour traiter une sauvegarde ou une restauration.

Contrairement au document sur les composants de sauvegarde, le document de métadonnées de l’enregistreur doit être considéré comme une structure en lecture seule. Une fois qu’un enregistreur l’a créé, le document n’est pas modifié.

## <a name="writer-event-handling"></a>Gestion des événements du writer

Les opérations VSS d’un enregistreur sont lancées par le biais de la réception d’événements COM.

Quand aucun événement n’est présent, un enregistreur n’effectue pas d’opérations VSS (telles qu’une sauvegarde ou une restauration VSS). Au lieu de cela, il effectue son travail normal, tel que la réponse aux requêtes de base de données, la gestion des données utilisateur ou la fourniture d’autres services.

Pour garantir le bon fonctionnement de la gestion des erreurs pour plusieurs sessions parallèles de sauvegarde et de restauration, et pour garantir qu’une seule session de sauvegarde ou de restauration n’endommage pas une autre, vous devez effectuer les opérations suivantes :

-   Si le gestionnaire d’événements d’un writer (tel que [**CVssWriter :: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)) appelle la méthode [**CVssWriterEx2 :: GetSessionId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid), [**CVssWriter :: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)ou [**CVssWriterEx2 :: SetWriterFailureEx**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) , le gestionnaire d’événements doit appeler la méthode dans le même thread que celui qui a appelé le gestionnaire d’événements.
-   L’implémentation de votre writer d’un gestionnaire d’événements tel que [**OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) peut décharger le travail vers les threads de travail si vous le souhaitez, à condition que chaque thread de travail marshale tous les rapports d’erreurs nécessaires au thread du gestionnaire d’événements d’origine.

## <a name="handling-identify-events"></a>Gestion des événements d’identification

À l’exception de l’événement d’identification, le type et l’ordre des événements reçus par un writer dépend uniquement du type d’opérations VSS en cours.

L’événement d’identification nécessite que les enregistreurs fournissent les informations système relatives à leur configuration et aux fichiers qu’ils gèrent par le biais de leur [*document de métadonnées d’écriture*](vssgloss-w.md). Un événement d’identification est généré pour la prise en charge de presque toutes les opérations VSS, y compris les requêtes système, ainsi que les opérations de cliché instantané et de sauvegarde et de restauration. Par conséquent, toute implémentation du gestionnaire d’événements identify [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) doit pouvoir gérer un événement d’identification à tout moment, y compris au milieu du traitement d’une autre opération VSS, telle qu’une sauvegarde ou une restauration. Un événement d’identification ne doit jamais être considéré comme faisant partie du cycle de vie d’une opération VSS, même si sa génération peut être attendue et requise avant le début de cette opération.

Il est particulièrement important que les informations d’État relatives à une opération VSS ne soient pas modifiées dans [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), car la réception d’un événement non ordonné réinitialise ces informations.

## <a name="backup-and-restore-events"></a>Événements de sauvegarde et de restauration

Selon qu’elle participe à une sauvegarde ou une restauration, un enregistreur recevra entre deux et sept événements, en plus d’un événement d’identification initial.

La gestion de ces événements constitue (du point de vue d’un enregistreur) le cycle de vie d’une opération de sauvegarde ou de restauration.

Dans une opération de sauvegarde classique (consultez [vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md)), un enregistreur peut gérer les événements suivants (en plus d’un événement d’identification initial) :

-   PrepareForBackup
-   PrepareForSnapshot
-   Freeze
-   Libérer
-   PostSnapshot
-   BackupComplete
-   BackupShutdown

Dans une opération de restauration classique (consultez [vue d’ensemble du traitement d’une restauration sous VSS](overview-of-processing-a-restore-under-vss.md)), un enregistreur peut gérer les événements suivants :

-   Prérestauration
-   PostRestore

 

 



