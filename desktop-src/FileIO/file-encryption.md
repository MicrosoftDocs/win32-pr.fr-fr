---
description: Le système de fichiers EFS (Encrypted File System) fournit une protection par chiffrement des fichiers individuels sur les volumes de système de fichiers NTFS à l’aide d’un système à clé publique.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Chiffrement de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dbbfa82024bea13eab9e672b482ea18bc1051cd6e86b97d2a405351e3b078b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107569"
---
# <a name="file-encryption"></a>Chiffrement de fichier

Le système de fichiers EFS (Encrypted File System) fournit un niveau supplémentaire de sécurité pour les fichiers et les répertoires. Il fournit une protection par chiffrement des fichiers individuels sur les volumes de système de fichiers NTFS à l’aide d’un système à clé publique.

en règle générale, le contrôle d’accès aux objets de fichiers et d’annuaire fournis par le modèle de sécurité Windows est suffisant pour protéger l’accès non autorisé aux informations sensibles. Toutefois, si un ordinateur portable qui contient des données sensibles est perdu ou volé, la protection de la sécurité de ces données risque d’être compromise. Le chiffrement des fichiers augmente la sécurité.

Pour déterminer si un système de fichiers prend en charge le chiffrement de fichier pour les fichiers et les répertoires, appelez la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et examinez l’indicateur de bit de **\_ \_ chiffrement de fichier FS** . Notez que les éléments suivants ne peuvent pas être chiffrés :

-   Fichiers compressés
-   Fichiers système
-   Répertoires système
-   Répertoires racine
-   Transactions

Les fichiers partiellement alloués peuvent être chiffrés.

TxF ne prend pas en charge la plupart des opérations sur les fichiers EFS (Encrypted File System). Les seules opérations prises en charge par TxF sont les opérations de lecture, telles que [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                               | Description                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestion des fichiers et des répertoires chiffrés](handling-encrypted-files-and-directories.md)<br/> | Un fichier marqué comme chiffré est chiffré par le système de fichiers NTFS à l’aide du pilote de chiffrement actuel.<br/>                                                          |
| [Fichiers chiffrés et clés utilisateur](encrypted-files-and-user-keys.md)<br/>                       | Répertorie les fonctions à utiliser pour créer une nouvelle clé, ajouter une clé à un fichier chiffré, interroger les clés d’un fichier chiffré et supprimer des clés d’un fichier chiffré.<br/> |
| [Sauvegarde et restauration de fichiers chiffrés](backup-and-restore-of-encrypted-files.md)<br/>       | Les fonctions de chiffrement brutes permettent de sauvegarder des fichiers chiffrés.<br/>                                                                                                |



 

Pour plus d’informations sur le chiffrement, consultez [Ajout d’utilisateurs à un fichier chiffré](adding-users-to-an-encrypted-file.md).

Pour plus d’informations sur le chiffrement, consultez [chiffrement](/windows/desktop/SecCrypto/cryptography-portal).

 

