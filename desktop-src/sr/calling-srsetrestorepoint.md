---
title: Appel de SRSetRestorePoint
description: Une application peut créer un point de restauration avant de provoquer une modification importante du système, telle qu’une mise à jour de l’installation, de la désinstallation ou de la fonctionnalité.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ee2fc64fc74dd9ceeff4856a6a63effe0667ff2bd837d7dc8ae521172a1c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592209"
---
# <a name="calling-srsetrestorepoint"></a>Appel de SRSetRestorePoint

Une application peut créer un point de restauration avant de provoquer une modification importante du système, telle qu’une mise à jour de l’installation, de la désinstallation ou de la fonctionnalité.

Les programmes d’installation doivent créer un point de restauration juste avant l’installation en appelant la fonction [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) avec le membre **dwEventType** de la structure [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) définie sur commencer la \_ \_ modification système. Pour signaler à la restauration du système que l’installation est terminée, appelez **SRSetRestorePoint** avec **DWEVENTTYPE** défini sur terminer la \_ modification du système \_ .

Si l’utilisateur annule l’installation de l’application, le programme d’installation peut supprimer le point de restauration créé au début de l’installation. La suppression du point de restauration est facultative et peut empêcher l’utilisateur d’effectuer une récupération à partir de modifications non intentionnelles apportées par le programme d’installation au cours de l’annulation. Si le programme d’installation doit supprimer un point de restauration, il peut appeler la fonction [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) ou appeler [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) avec **dwRestorePointType** défini sur opération annulée \_ , **DWEVENTTYPE** définir \_ sur \_ la modification du système de fin et **LlSequenceNumber** défini sur la valeur retournée par l’appel initial à **SRSetRestorePoint**.

* * Windows 8 : * *

Une nouvelle clé de registre permet aux développeurs d’applications de modifier la fréquence de création du point de restauration.

Les applications doivent créer cette clé pour l’utiliser, car elle n’est pas préexistante dans le système. Les éléments suivants s’appliquent par défaut si la clé n’existe pas. si une application appelle la fonction **SRSetRestorePoint** pour créer un point de restauration, Windows ignore la création de ce nouveau point de restauration si des points de restauration ont été créés au cours des dernières 24 heures. La restauration du système définit le membre **IISequenceNumber** de la structure [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) sur le numéro de séquence du point de restauration créé précédemment dans la journée et définit la valeur du membre **nStatus** sur **erreur \_ réussite**. La fonction **SRSetRestorePoint** retourne la **valeur true**.

les développeurs peuvent écrire des applications qui créent la valeur **DWORD** **SystemRestorePointCreationFrequency** sous la clé de registre **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. La valeur de cette clé de Registre peut modifier la fréquence de création du point de restauration. La valeur de cette clé de Registre peut modifier la fréquence de création du point de restauration.

Si l’application appelle **SRSetRestorePoint** pour créer un point de restauration et que la valeur de la clé de Registre est 0, la restauration du système n’ignore pas la création du nouveau point de restauration.

Si l’application appelle **SRSetRestorePoint** pour créer un point de restauration et que la valeur de la clé de Registre est l’entier N, la restauration du système ignore la création d’un nouveau point de restauration si des points de restauration ont été créés au cours des N minutes précédentes.

* * Windows 8 : * *

la restauration du système s’exécutant sur Windows 8 surveille les fichiers du volume de démarrage qui sont pertinents pour la restauration du système uniquement. les captures instantanées du volume de démarrage créé par la restauration du système exécutée sur Windows 8 peuvent être supprimées si l’instantané est ensuite exposé par une version antérieure de Windows. Notez que bien qu’il n’existe qu’un seul volume système, il existe un volume de démarrage pour chaque système d’exploitation dans un système à démarrage multiple.

les développeurs peuvent écrire des applications qui créent la valeur **DWORD** **ScopeSnapshots** sous la clé de registre **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. Si la valeur de cette clé de Registre est égale à 0, la restauration du système crée des instantanés du volume de démarrage de la même façon que dans les versions antérieures de Windows. si cette valeur est supprimée, la restauration du système exécutée sur Windows 8 reprend la création de captures instantanées qui surveillent les fichiers du volume de démarrage qui sont pertinents pour la restauration du système uniquement.

Pour obtenir un exemple, consultez Utilisation de la [restauration du système](using-system-restore.md).

 

 




