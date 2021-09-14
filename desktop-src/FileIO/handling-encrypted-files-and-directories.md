---
description: Un fichier marqué comme chiffré est chiffré par le système de fichiers NTFS à l’aide du pilote de chiffrement actuel.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Gestion des fichiers et des répertoires chiffrés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2718656a28eb678c10076e228e08a2a95cabd1fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009934"
---
# <a name="handling-encrypted-files-and-directories"></a>Gestion des fichiers et des répertoires chiffrés

Un programmeur ou un utilisateur peut marquer un répertoire ou un fichier comme étant chiffré. Un fichier marqué comme chiffré est chiffré par le système de fichiers NTFS à l’aide du pilote de chiffrement actuel. Si, à une date ultérieure, le fichier est marqué comme non chiffré, il est déchiffré et laissé dans un état de texte brut (non sécurisé).

Les répertoires ne sont pas chiffrés. Au lieu de cela, par défaut, dans un répertoire « chiffré », tous les nouveaux fichiers du répertoire sont chiffrés lors de la création. Un utilisateur doit modifier spécifiquement l’état d’un nouveau fichier à déchiffrer si l’utilisateur ne souhaite pas que le fichier soit chiffré. Un répertoire chiffré est visible. Pour rendre un répertoire inaccessible à d’autres utilisateurs, utilisez les méthodes standard de contrôle d’accès.

Les fonctions de chiffrement ne peuvent pas être utilisées avec l' [API Backup](/windows/desktop/Backup/backup).

Pour chiffrer un nouveau fichier, utilisez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l’indicateur de **fichier \_ attribute \_ Encrypted** . Pour chiffrer un fichier existant, utilisez la fonction [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) . Tous les flux de données dans le fichier sont chiffrés. Si le fichier est déjà chiffré, **EncryptFile** ne fait rien, mais retourne une valeur différente de zéro, ce qui indique une réussite. Si le fichier est compressé, **EncryptFile** décompresse le fichier avant de le chiffrer.

Pour déchiffrer un fichier chiffré, utilisez la fonction [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) . Si le fichier n’est pas chiffré, **DecryptFile** ne fait rien, mais retourne une valeur différente de zéro indiquant la réussite.

La fonction [**EncryptionDisable**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) désactive ou active le chiffrement du répertoire indiqué et des fichiers qu’il contient. Elle n’affecte pas le chiffrement des sous-répertoires situés sous le répertoire indiqué.

Pour récupérer l’état de chiffrement d’un fichier, utilisez la fonction [**FileEncryptionStatus**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) . Vous pouvez également appeler la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) et examiner l’indicateur de **fichier \_ attribute \_ Encrypted** dans la valeur de retour.

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) et [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) tentent de chiffrer le fichier de destination avec les clés utilisées dans le chiffrement du fichier source. Si cela ne peut pas être fait, les deux fonctions tentent de chiffrer le fichier de destination avec les clés par défaut. Si ces deux méthodes ne peuvent pas être effectuées, **CopyFile** et **CopyFileEx** échouent avec une erreur **\_ \_ échec du chiffrement** de l’erreur. Si vous souhaitez que **CopyFileEx** termine l’opération de copie même si le fichier de destination ne peut pas être chiffré, incluez l’indicateur de **\_ Destination fichier de copie autoriser le \_ \_ \_ déchiffrement** dans la valeur du paramètre *dwCopyFlags* dans votre appel à **CopyFileEx**.

 

 
