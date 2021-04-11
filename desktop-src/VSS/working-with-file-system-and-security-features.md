---
description: Vous trouverez ci-dessous des conseils pour l’interopérabilité correcte avec divers systèmes de fichiers et fonctionnalités de sécurité qui ont été introduits dans Windows Vista et Windows Server 2008.
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: Utilisation du système de fichiers et des fonctionnalités de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12903599beb7ed153965f4b803ad8147fd32067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113155"
---
# <a name="working-with-file-system-and-security-features"></a>Utilisation du système de fichiers et des fonctionnalités de sécurité

Vous trouverez ci-dessous des conseils pour l’interopérabilité correcte avec divers systèmes de fichiers et fonctionnalités de sécurité qui ont été introduits dans Windows Vista et Windows Server 2008.

## <a name="interoperability-with-transactions"></a>Interopérabilité avec les transactions

Pour prendre en charge les transactions, VSS s’assure que le gestionnaire de transactions KTM (Kernel Transaction Manager) et le Distributed Transaction Coordinator (DTC) sont gelés avant la création de clichés instantanés de volume. Si le système ne parvient pas à geler ou à libérer KTM ou DTC, les erreurs de délai d’attente suivantes peuvent être retournées par la méthode [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) :

<dl> \_ \_ \_ \_ délai d’expiration de la transaction VSS E  
\_ \_ \_ \_ délai d’expiration de la transaction VSS E  
</dl>

Si le demandeur reçoit l’un de ces codes d’erreur, il doit retenter la création du cliché instantané.

Les opérations de Registre et de système de fichiers peuvent également être traitées. Dans le cas du Registre, l’enregistreur du Registre est chargé de garantir la cohérence transactionnelle. Dans le cas d’opérations du système de fichiers NTFS transactionnel (TxF), le fournisseur système est chargé de garantir la cohérence transactionnelle. Pour ce faire, vous devez monter le cliché instantané en lecture/écriture après qu’il a été créé pour permettre la récupération automatique. Lors de la phase de récupération automatique, KTM restaure toutes les transactions incomplètes.

## <a name="identifying-and-creating-hard-links"></a>Identification et création de liens physiques

Lors de la sauvegarde de fichiers, une application de sauvegarde doit identifier toutes les liaisons physiques vers chaque fichier afin d’éviter de sauvegarder le même fichier plusieurs fois. Deux nouvelles fonctions sont disponibles pour énumérer les liens physiques : [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) et [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew).

De même, lors de la restauration de fichiers, l’application de sauvegarde doit restaurer les liens physiques à l’aide de la fonction [**CreateHardLink**](/windows/win32/api/winbase/nf-winbase-createhardlinka) .

Les applications de sauvegarde doivent également déclarer le privilège de nom de sauvegarde de SE \_ \_ pendant la phase de sauvegarde et le nom de restauration de se \_ \_ pendant la phase de restauration.

## <a name="permissions-and-privileges-required-by-backup-applications"></a>Autorisations et privilèges requis par les applications de sauvegarde

Les applications de sauvegarde qui restaurent les fichiers système requièrent les privilèges suivants :

<dl> nom de la sauvegarde de SE \_ \_  
nom de la restauration de la SE \_ \_  
\_nom de sécurité de se \_  
SE \_ prendre le nom de la \_ propriété \_  
</dl>

Les applications de sauvegarde doivent également demander \_ des droits d’accès en écriture au propriétaire lors de la phase de restauration.

## <a name="windows-media-digital-rights-management"></a>Rights Management Windows Media Digital

Le client Windows Media Digital Rights Management (DRM) conserve un répertoire de fichiers d’État et de licence sensibles dans le répertoire% ProgramData% \\ Microsoft \\ Windows \\ DRM. Les fichiers de ce répertoire doivent être purgés en même temps que les fichiers temporaires et les fichiers cache. Pour vous assurer que le client Windows DRM reste dans un état cohérent, vous devez éviter de sauvegarder ou de restaurer ces fichiers. Ce répertoire est listé dans la clé de Registre FilesNotToBackup. Pour plus d’informations sur la clé FilesNotToBackup, consultez [génération d’un jeu de sauvegarde](generating-a-backup-set.md).

## <a name="user-account-control"></a>Contrôle de compte d'utilisateur

L’introduction du contrôle de compte d’utilisateur (UAC) dans Windows Vista signifie que, sauf indication contraire, les applications doivent s’exécuter sous un compte d’utilisateur standard. En outre, la fonctionnalité de virtualisation des fichiers et du Registre du contrôle de compte d’utilisateur modifie les emplacements où sont stockées les données utilisateur. Pour plus d’informations sur l’utilisation du contrôle de compte d’utilisateur et la virtualisation de fichier et de Registre, consultez les références suivantes :

<dl>

[Windows Vista et Windows Server 2008 Developer Story : exigences de développement d’applications Windows Vista pour le contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905330(v=msdn.10))  
[Exigences de développement d’applications Windows Vista pour la compatibilité du contrôle de compte d’utilisateur](/previous-versions/dotnet/articles/bb530410(v=msdn.10))  
[Mise à jour corrective du contrôle de compte d’utilisateur (UAC)](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a>Chiffrement de lecteur BitLocker

Chiffrement de lecteur BitLocker est une nouvelle fonctionnalité de Windows Vista Enterprise, Windows Vista Ultimate et Windows Server 2008 qui offre un démarrage sécurisé et un chiffrement de volume complet. La compréhension de cette fonctionnalité est importante pour les développeurs d’applications de sauvegarde qui effectuent des restaurations hors connexion où les données devront peut-être être restaurées sur un lecteur chiffré.

Pour restaurer des données sur un lecteur chiffré, procédez comme suit :

1.  Déverrouillez le lecteur.
2.  Désactivez Chiffrement de lecteur BitLocker.
3.  Effectuez la restauration.
4.  Démarrez dans le système d’exploitation restauré et activez Chiffrement de lecteur BitLocker.

Pour obtenir des informations détaillées sur Chiffrement de lecteur BitLocker, y compris un guide pas à pas, consultez [chiffrement de lecteur BitLocker](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) sur le site Web Microsoft TechNet Windows Vista. Pour plus d’informations sur le fournisseur WMI Chiffrement de lecteur BitLocker, consultez [chiffrement de lecteur BitLocker Provider](../secprov/bitlocker-drive-encryption-provider.md).

 

 
