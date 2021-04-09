---
title: Restauration d’un serveur Active Directory
description: Les serveurs Active Directory doivent être restaurés hors connexion.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Restauration de Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273d02fd50d6b3bd68a055a6a783566e4ebddcf7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842026"
---
# <a name="restoring-an-active-directory-server"></a>Restauration d’un serveur Active Directory

Les serveurs Active Directory doivent être restaurés hors connexion. Le système doit être redémarré en mode de restauration des services d’annuaire. Dans ce mode, le système d’exploitation s’exécute sans Active Directory Domain Services et toute la validation de l’utilisateur s’effectue par le biais du gestionnaire de comptes de sécurité (SAM) dans le registre. Pour restaurer Active Directory Domain Services, utilisez les informations d’identification d’un administrateur local sur le contrôleur de domaine qui est restauré.

L’appelant des fonctions de restauration doit avoir le privilège d’accès au **\_ \_ nom** de la restauration. Utilisez la fonction [**DsSetAuthIdentity**](dssetauthidentity.md) pour définir le contexte de sécurité sous lequel les fonctions de sauvegarde et de restauration d’annuaire sont appelées.

Sachez que lorsque vous restaurez des Active Directory Domain Services, vous devez également restaurer les autres composants d’État du système.

**Pour restaurer Active Directory Domain Services**

1.  Appelez la fonction [**DsIsNTDSOnline**](dsisntdsonline.md) pour déterminer si Active Directory Domain Services sont en cours d’exécution.
2.  Si Active Directory Domain Services ne sont pas en cours d’exécution, la fonction [**DsRestorePrepare**](dsrestoreprepare.md) est appelée pour initialiser l’opération de restauration et obtenir un handle de contexte de sauvegarde. Si Active Directory Domain Services sont en cours d’exécution, il ne peut pas être restauré et l’application de restauration doit faire échouer l’opération de restauration. La fonction **DsRestorePrepare** nécessite l’obtention du jeton d’expiration à partir de la fonction [**DsBackupPrepare**](dsbackupprepare.md) pendant l’opération de sauvegarde.
3.  Appelez la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) pour déterminer les répertoires dans lesquels les fichiers doivent être restaurés. Si cette fonction échoue, restaurez les données dans le répertoire source de sauvegarde d’origine ; Il s’agit du répertoire à partir duquel les données ont été sauvegardées.
4.  Appelez la fonction [**DsRestoreRegister**](dsrestoreregister.md) pour préparer le serveur de Active Directory pour l’opération de restauration et verrouiller les répertoires de restauration.
5.  Utilisez les fonctions Win32 standard pour restaurer les fichiers. Tout d’abord, supprimez tous les fichiers du répertoire de destination. Copiez ensuite les fichiers de sauvegarde dans le répertoire de destination.
6.  Appelez la fonction [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) pour indiquer que la restauration est terminée.
7.  Appelez la fonction [**DsRestoreEnd**](dsrestoreend.md) pour libérer toutes les ressources associées au contexte.

Après une restauration en mode de restauration des services d’annuaire, le contrôleur de domaine doit être redémarré en mode normal. Au démarrage du service d’annuaire, le contrôleur de domaine effectue la vérification de cohérence normale et le répertoire restauré est alors en ligne.

N’oubliez pas que la restauration d’un serveur Active Directory est toujours une opération en deux parties. Tout d’abord, restaurez la base de données jusqu’au moment où la sauvegarde a été effectuée. Ensuite, répliquez le répertoire dans lequel le DSA nouvellement restauré réplique les mises à jour après la sauvegarde à partir d’autres DSA dans le domaine et la forêt d’entreprise.

Un ordinateur s’exécutant sur Windows 2000 ou Windows Server 2003, qui contient un réplica du service d’annuaire, est un contrôleur de domaine.

La fonction [**DsRestoreRegister**](dsrestoreregister.md) ajoute des données au registre qui doivent survivre au processus de restauration du Registre pour que la restauration fonctionne correctement. Pour vous assurer que ces données de Registre sont conservées, restaurez Active Directory Domain Services avec les fonctions **DsRestore \*** avant de redémarrer l’ordinateur après l’appel de la fonction [**RegReplaceKey**](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) . Ce processus fonctionne parce que **RegReplaceKey** ne remplace pas la ruche du Registre tant que l’ordinateur n’est pas redémarré et que les données de Registre ajoutées par la fonction **DsRestoreRegister** n’ont pas été spécifiquement remplacées lors d’une opération de restauration du Registre.

 

 