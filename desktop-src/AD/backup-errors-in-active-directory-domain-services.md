---
title: Erreurs de sauvegarde dans Active Directory Domain Services
description: Cette rubrique répertorie les valeurs de retour d’erreur de sauvegarde pour les fonctions dans Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Erreurs de sauvegarde Active Directory
- Erreurs de sauvegarde du service domaine Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5038b1d3a7a1f24c2e3b8dbf137aa2722073650b878e1d6a1dfdec8cac399a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024136"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Erreurs de sauvegarde dans Active Directory Domain Services

Cette rubrique répertorie les valeurs de retour d’erreur de sauvegarde pour les fonctions dans Active Directory Domain Services.



| Valeur                                      | Description                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | La fonction n’est pas implémentée.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | Ce paramètre n'est pas valide.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | Une erreur interne s’est produite.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | Le descripteur n’est pas valide.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | Le processus de restauration est en cours.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | Le fichier spécifié est ouvert.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | Les destinataires ne sont pas valides. <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | Impossible de sauvegarder. Une connexion au serveur de sauvegarde spécifié n’a pas été détectée ou le service que vous tentez de sauvegarder n’est pas en cours d’exécution.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Une table de restauration existe pour le composant spécifié. Un mappage de restauration peut être spécifié lors d’une restauration complète.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | une autre application a modifié la base de données de Service d’annuaire Windows NT/Windows 2000 spécifiée de telle sorte que toutes les sauvegardes suivantes échouent. Pour résoudre ce problème, effectuez une sauvegarde complète.<br/> |
| **hrLogFileNotFound**<br/>           | impossible d’effectuer une sauvegarde incrémentielle car un fichier journal de base de données du Service d’annuaire Windows NT/Windows 2000 requis est introuvable.<br/>                                        |
| **hrCircularLogging**<br/>           | le Windows composant de Service d’annuaire NT/Windows 2000 spécifié est configuré pour utiliser des journaux de base de données circulaires. Elle ne peut pas être sauvegardée de façon incrémentielle. Effectuez une sauvegarde complète.<br/>       |
| **hrNoFullRestore**<br/>             | Les bases de données n’ont pas été restaurées sur cet ordinateur. Vous ne pouvez pas restaurer une sauvegarde incrémentielle tant qu’une sauvegarde complète n’a pas été restaurée.<br/>                                            |
| **hrCommunicationError**<br/>        | Une erreur de communication s’est produite lors de la tentative d’exécution d’une sauvegarde locale.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | Vous devez effectuer une sauvegarde complète avant de pouvoir effectuer une sauvegarde incrémentielle.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | Le jeton d’expiration est manquant. Impossible de restaurer sans les données d’expiration.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | Le jeton d’expiration est dans un format non reconnaissable.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | Le contenu DS de la sauvegarde est obsolète. Restaurez avec une copie récente.<br/>                                                                                                            |



 

## <a name="see-also"></a>Voir aussi

[Réussite](success.md), [erreurs système dans Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), [Erreurs du gestionnaire de répertoires](directory-manager-errors.md), erreurs de [journalisation et de récupération dans les fonctions de Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), [valeurs de retour pour les fonctions dans Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





