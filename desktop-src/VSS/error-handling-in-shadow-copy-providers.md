---
description: 'VSS permet l’existence de nombreux clichés instantanés à la fois, mais il n’autorise qu’une seule création de jeu de clichés instantanés en cours entre l’appel à IVssBackupComponents :: StartSnapshotSet et le retour de l’appel à IVssBackupComponents ::D oSnapshotSet.'
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Gestion des erreurs dans les fournisseurs de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0963df4c9c81c2cd9f96e7c1828243f3910a1df34d5ef94a714f17c57b404b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032679"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Gestion des erreurs dans les fournisseurs de clichés instantanés

VSS permet l’existence de nombreux clichés instantanés à la fois, mais il n’autorise qu’une seule création de jeu de clichés instantanés en cours entre l’appel à [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) et le retour de l’appel à [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).

## <a name="no-partial-commit"></a>Aucune validation partielle

Si un fournisseur échoue sur un volume ou un numéro d’unité logique du jeu de clichés instantanés, la création du jeu de clichés instantanés entier échoue. C'est la procédure normale. Cette conception simplifie les problèmes de comportement associés à la sémantique de défaillance partielle et conserve un point dans le temps cohérent pour tous les clichés instantanés de l’ensemble.

## <a name="reporting-fault-conditions"></a>Signalement des conditions d’erreur

Si une erreur de fournisseur ou une condition d’erreur se produit, le fournisseur doit consigner une erreur dans le journal des événements de l’application. Cela comprend, sans s’y limiter, les erreurs spécifiques au fournisseur lors de la création ou de l’importation d’un jeu de clichés instantanés, ou l’échec d’allocation de ressources pour le cliché instantané de copie sur écriture après la création. Cette journalisation ne doit pas avoir lieu au moment où les volumes dans le jeu de clichés instantanés sont dans un état figé.

## <a name="valid-provider-return-values"></a>Valeurs de retour de fournisseur valides

Le tableau suivant répertorie les codes de retour valides pour les méthodes de fournisseur et leurs significations.



| Valeur                                                                                                                                                                              | Description                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>\_OK<br/>                                                                                                                     | La méthode a réussi.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>\_OUTOFMEMORY E<br/>                                                                                          | Le fournisseur ne dispose pas de suffisamment de mémoire ou d’autres ressources système.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | L’une des valeurs de paramètre n’est pas valide.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>\_ACCESSDENIED E<br/>                                                                                       | Un client non privilégié a tenté d’appeler le fournisseur.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>\_ \_ état incorrect de VSS E \_<br/>                                                                                  | Aucun fournisseur ne prend en charge l’opération demandée ou l’opération ne peut pas être effectuée sur l’objet, car l’objet n’est pas dans l’état correct.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>\_objet VSS \_ E \_ \_ introuvable<br/>                                                            | Un paramètre fait référence à un objet qui est introuvable (par exemple, un ID de cliché instantané, un ID de jeu de clichés instantanés ou un volume).<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>VSS \_ E \_ stockage insuffisant \_<br/>                                                 | Le fournisseur ne peut pas effectuer l’opération, car l’espace disque est insuffisant.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>\_volume E \_ VSS \_ non \_ pris en charge<br/>                                                | Aucun fournisseur sur cet ordinateur ne prend en charge l’opération demandée sur le volume.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>\_volume E \_ VSS \_ non \_ pris en charge \_ par le \_ fournisseur<br/>          | Le fournisseur ne prend pas en charge le volume.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>\_ \_ \_ nombre maximal \_ de \_ captures instantanées de \_ VSS E atteint<br/> | Le fournisseur a atteint le nombre maximal de clichés instantanés qu’il peut prendre en charge.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>\_veto du \_ fournisseur VSS E \_<br/>                                                                      | Le fournisseur a rencontré une erreur d’exécution interne qui n’est pas mappée à une autre valeur de retour. Le fournisseur doit également écrire un événement dans le journal des événements de l’application pour fournir à l’utilisateur des informations sur la façon de résoudre ce problème.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E \_ ne peut pas \_ rétablir le \_ dépatinage<br/>                                                | La signature MBR ou l’ID GPT d’un ou plusieurs disques n’a pas pu être défini sur la valeur demandée. Pour plus d’informations, consultez le journal des événements d’application.<br/>                                                                                            |



 

Le fournisseur ne doit pas tenter de retourner d’autres codes d’erreur.

Si le fournisseur retourne un code d’erreur qui n’est pas attendu (par exemple, a la **\_ valeur false**, **e \_ Fail**, **e \_ inattendue** ou **e \_ Abort**), VSS écrit un événement dans le journal des événements en mentionnant le fournisseur et la méthode qui a échoué, et convertit l’erreur en **\_ erreur VSS E \_ inattendue du \_ fournisseur \_** avant de retourner au demandeur. Cela n’est pas effectué pour les retours de [**IVssProviderCreateSnapshotSet :: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) ou [**IVssProviderNotifications :: OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 




