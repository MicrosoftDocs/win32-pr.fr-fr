---
description: Les administrateurs peuvent créer, supprimer et recréer des journaux de modifications.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Création, modification et suppression d’un journal des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d4cf9a597baa14fc929028eab262479da30797a2e423b779083f028927ce50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150865"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Création, modification et suppression d’un journal des modifications

Les administrateurs peuvent créer, supprimer et recréer des journaux de modification à votre consigne. Un administrateur doit supprimer un journal lorsque la valeur du numéro de séquence de mise à jour (USN) actuelle approche la valeur USN maximale possible, comme indiqué par le membre **MaxUsn** de la structure des [**\_ \_ données du journal USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) . Un administrateur peut également supprimer et recréer un journal des modifications pour libérer de l’espace disque. Pour effectuer cette opération et toutes les autres opérations de journal des modifications non programmées, vous devez disposer de privilèges d’administrateur système. Autrement dit, vous devez être membre du groupe administrateurs.

Pour créer ou modifier un journal des modifications sur un volume spécifié par programme, utilisez le code de contrôle [**FSCTL \_ créer un \_ \_ journal USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) .

Lorsque vous créez un nouveau journal des modifications ou en modifiez un, le système de fichiers NTFS définit des informations pour ce journal des modifications à partir des informations de la structure [**créer les \_ \_ \_ données du journal USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) , que [**FSCTL \_ crée le \_ \_ journal USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) comme entrée. **Créer \_ Les \_ \_ données du journal USN** possèdent les membres **MaximumSize** et **AllocationDelta**.

**MaximumSize** correspond à la taille maximale cible du journal des modifications, en octets. Le journal des modifications peut croître plus grand que cette valeur, mais au niveau des points de contrôle du système de fichiers NTFS, le système de fichiers NTFS examine le journal et le tronque lorsque sa taille dépasse la valeur de **MaximumSize** plus la valeur de **AllocationDelta**. (Au niveau des points de contrôle du système de fichiers NTFS, le système d’exploitation écrit des enregistrements dans le fichier journal du système de fichiers NTFS qui permet au système de fichiers NTFS de déterminer le traitement requis pour récupérer suite à une défaillance.)

**AllocationDelta** est le nombre d’octets ajoutés à la fin et supprimés du début du journal des modifications chaque fois que la mémoire est allouée ou désallouée. En d’autres termes, l’allocation et la désallocation ont lieu dans des unités de cette taille. Un entier multiple d’une taille de cluster est une valeur raisonnable pour ce membre.

Si un administrateur modifie un journal des modifications existant pour qu’il ait **une plus grande** valeur de taille maximale, par exemple si un volume est réindexé trop souvent, le journal des modifications reçoit simplement de nouvelles entrées jusqu’à ce qu’il dépasse la nouvelle taille maximale.

Pour supprimer un journal des modifications, utilisez le code de contrôle [**FSCTL \_ supprimer le \_ \_ journal USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) . Lorsque vous utilisez cette opération, elle parcourt tous les fichiers sur le volume et réinitialise l’USN de chaque fichier à zéro. L’opération supprime ensuite le journal des modifications existant. Cette opération persiste entre les redémarrages du système jusqu’à ce qu’elle se termine. Toute tentative de lecture, de création ou de modification du journal des modifications au cours de ce processus échoue avec le code **d’erreur erreur \_ \_ de suppression du journal \_ en \_ cours**.

Vous pouvez également utiliser le code de contrôle [**FSCTL \_ supprimer le \_ \_ journal USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) pour déterminer si une suppression lancée par un autre processus est en cours. Par exemple, votre application, lorsqu’elle est démarrée, peut déterminer si une suppression est en cours. Étant donné que les suppressions du journal sont conservées entre les redémarrages du système, les services et les applications démarrés au redémarrage du système doivent vérifier qu’une suppression est en cours.

Les journaux des modifications ne sont pas nécessairement créés au démarrage. Pour créer un journal des modifications, un administrateur peut le faire explicitement ou démarrer un autre service qui requiert un journal des modifications.

 

 
