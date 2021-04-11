---
title: Stockage des informations spécifiques à l’utilisateur
description: Les applications doivent stocker les informations spécifiques à l’utilisateur dans des emplacements spécifiques à l’utilisateur, séparément des informations globales qui s’appliquent à tous les utilisateurs.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c6236b7ba11a8b3149533e920b9b9413085d93
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031404"
---
# <a name="storing-user-specific-information"></a>Stockage des informations spécifiques à l’utilisateur

Dans un environnement Services Bureau à distance, les applications doivent stocker des informations spécifiques à l’utilisateur dans des emplacements spécifiques à l’utilisateur, indépendamment des informations globales qui s’appliquent à tous les utilisateurs. Cette règle s’applique aux informations stockées dans le registre, ainsi qu’aux informations stockées dans les fichiers. En général, ne partez pas du principe qu’un ordinateur est équivalent à un utilisateur.

Stockez les informations de Registre spécifiques à l’utilisateur sous la clé de Registre **HKEY \_ Current \_ User** . Services Bureau à distance charge la ruche de Registre personnel de l’utilisateur actuel dans **HKEY \_ Current \_ User** lorsque l’utilisateur ouvre une session. Bien sûr, Services Bureau à distance gère le registre pour s’assurer que chacun des clients connectés détecte la ruche utilisateur correcte sous **HKEY \_ Current \_ User**. Pour plus d’informations sur les clés de Registre, consultez [sécurité de la clé de Registre et droits d’accès](/windows/desktop/SysInfo/registry-key-security-and-access-rights) et [ruches du registre](/windows/desktop/SysInfo/registry-hives).

En revanche, tous les utilisateurs partagent la ruche de l' **\_ \_ ordinateur local HKEY** . Utilisez **HKEY \_ local \_ machine** pour stocker des informations spécifiques à l’ordinateur, et non des informations spécifiques à l’utilisateur.

Stockez les fichiers de préférences utilisateur ou d’autres fichiers spécifiques à l’utilisateur dans le répertoire racine de l’utilisateur ou dans un répertoire spécifié par l’utilisateur. Cette considération s’applique aux fichiers temporaires utilisés pour stocker des informations intermédiaires (telles que les données mises en cache) ou à transmettre des données à une autre application. Les fichiers temporaires spécifiques à l’utilisateur doivent également être stockés par utilisateur.

Vous pouvez utiliser la fonction [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) avec l' \_ indicateur personnel de CSIDL pour connaître l’emplacement du répertoire des fichiers personnels de l’utilisateur. Vous pouvez également utiliser la fonction [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) pour récupérer le chemin d’accès du répertoire Windows. Dans un environnement de Services Bureau à distance, il est garanti que le répertoire Windows est privé pour chaque utilisateur. Ne stockez pas les fichiers spécifiques à l’utilisateur dans le répertoire système, tel que WINDOWS ou le répertoire de programme, tel que Program Files.

Pour éviter les conflits entre les informations et les préférences des utilisateurs, les applications doivent stocker des informations temporaires par utilisateur dans des fichiers temporaires spécifiques à l’utilisateur. Les fichiers temporaires spécifiques à l’utilisateur empêchent également les échecs d’application causés par des conflits de verrouillage de fichiers. Pour spécifier le chemin d’accès pour le stockage des informations temporaires, utilisez la fonction [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) .

 

 