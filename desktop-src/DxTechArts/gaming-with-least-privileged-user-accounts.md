---
title: Jeux avec Least-Privileged comptes d’utilisateur
description: Cet article explique comment les développeurs de jeux peuvent créer des jeux Microsoft Windows qui fonctionnent bien avec les comptes d’utilisateur dotés de privilèges minimum (également appelés comptes d’utilisateur limité).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c44d94345462fc02ec649c5674ed88c38c12ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463422"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Jeux avec Least-Privileged comptes d’utilisateur

Cet article explique comment les développeurs de jeux peuvent créer des jeux Microsoft Windows qui fonctionnent bien avec les comptes d’utilisateur dotés de privilèges minimum (également appelés comptes d’utilisateur limité).

-   [Introduction](#introduction)
-   [Accès aux fichiers pour les comptes d’utilisateurs Least-Privileged](#file-access-for-least-privileged-user-accounts)
    -   [Scénario 1 : fichiers qui ne doivent pas être affichés ou modifiés par les utilisateurs](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Scénario 2 : fichiers qui doivent être affichés ou modifiés par les utilisateurs](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Accès au registre pour les comptes d’utilisateurs Least-Privileged](#registry-access-for-least-privileged-user-accounts)
-   [Mise à jour corrective avec les comptes d’utilisateur Least-Privileged](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Introduction

Windows gère ses utilisateurs avec des comptes. Aujourd’hui, plus de 80% des utilisateurs de l’ordinateur chez eux partagent leur ordinateur avec d’autres membres de la famille. Lorsque plusieurs utilisateurs partagent un ordinateur Windows, plusieurs comptes d’utilisateur sont créés et chaque utilisateur se connecte avec un compte individuel pour accéder à l’ordinateur. Avec la sensibilisation accrue à la sécurité, de plus en plus de personnes exploitent leurs ordinateurs avec des comptes d’utilisateur dotés de privilèges minimum, également appelés comptes d’utilisateurs limités, qui n’ont pas un contrôle total sur le système. Les comptes d’administrateur ont généralement un accès illimité à chaque partie de l’ordinateur. Cela peut affecter le fonctionnement des jeux basés sur Windows.

Il existe des avantages supplémentaires pour les développeurs de jeux qui écrivent leurs jeux pour travailler avec des comptes d’utilisateur dotés de privilèges minimum. Dans Windows Vista et versions ultérieures, les comptes d’utilisateur dotés de privilèges minimum sont appliqués, ce qui signifie que chaque compte sur le système, à l’exception de l’administrateur local, est un compte d’utilisateur doté de privilèges minimum. Cela aura une incidence sur la façon dont les jeux qui ne suivent pas les instructions (applications héritées) s’exécutent sur Windows Vista et versions ultérieures. Par exemple, lorsqu’une application tente d’écrire dans un dossier ou une valeur de Registre pour laquelle elle n’a pas d’autorisation, l’écriture de fichier est redirigée vers un magasin de fichiers virtuel pour l’utilisateur. Ce magasin de fichiers virtuel réside dans un dossier pour lequel l’utilisateur dispose d’un accès en écriture. Ce comportement peut ne pas sembler catastrophique en cas d’échec de la tentative d’écriture. Toutefois, les applications qui créent des fichiers virtualisés peuvent dérouter les utilisateurs, car les fichiers ne seront pas écrits à l’emplacement attendu par les utilisateurs. Par exemple, les jeux qui écrivent des fichiers de score élevé dans le même dossier que le dossier exécutable écrira ces fichiers dans un dossier virtualisé à la place. Par conséquent, un utilisateur ne peut pas voir le score élevé atteint par un autre utilisateur, car chaque utilisateur dispose d’un magasin de fichiers virtualisé distinct.

Les jeux qui suivent les instructions de cet article s’exécutent avec des comptes d’utilisateur dotés de privilèges minimum et, par conséquent, assurent la compatibilité avec Windows Vista et les versions ultérieures.

## <a name="file-access-for-least-privileged-user-accounts"></a>Accès aux fichiers pour les comptes d’utilisateurs Least-Privileged

Windows prend en charge deux systèmes de fichiers : FAT32 et NTFS. FAT32 est un système de fichiers hérité pris en charge uniquement pour la compatibilité descendante. NTFS prend en charge des autorisations de fichiers plus puissantes et robustes. L’utilisation du système de fichiers NTFS s’étend au fur et à mesure que les détaillants expédient de nouveaux ordinateurs sur lesquels Windows est préinstallé sur un disque dur partitionné NTFS. Sur un système Windows XP NTFS, les utilisateurs disposant de comptes d’utilisateur dotés de privilèges minimum disposent uniquement d’un accès limité à plusieurs dossiers. Toutefois, ils disposent d’un accès complet sur un système Windows XP basé sur FAT32.

Le tableau suivant répertorie l’emplacement par défaut de ces dossiers et leurs autorisations.



| Chemin d’accès                                               | Contenu du dossier              | Lire | Write | Créer/Supprimer |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <Drive>: \\ Windows                            | Le système d’exploitation Windows | X    |       |               |
| <Drive>: \\ Program Files                      | Fichiers d’application exécutables | X    |       |               |
| <Drive>: \\ Documents and Settings \\ nom d’utilisateur\* | Fichiers de chaque utilisateur            | X    | X     | X             |
| <Drive>: \\ Documents and Settings \\ All Users  | Tous les fichiers utilisateur               | X    | X     | X             |



 

\* Username est le nom de connexion de l’utilisateur.

Dans un compte d’utilisateur doté de privilèges minimum, vous pouvez lire, écrire, créer et supprimer des fichiers dans l’un ou l’autre dossier : documents and Settings \\ username ou documents and Settings \\ All Users.

Cela signifie que vous ne devez pas placer les jeux dans des \\ fichiers programme, mais qu’ils doivent être placés dans un sous-dossier dans \\ Mes documents. En outre, vous ne devez pas placer les données d’application temporaires dans les \\ fichiers programme ou \\ Mes documents, mais vous devez les placer dans le dossier Application Data (CSIDL \_ local \_ AppData).

Plus précisément, il existe deux scénarios que chaque jeu doit gérer :

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Scénario 1 : fichiers qui ne doivent pas être affichés ou modifiés par les utilisateurs

Un exemple typique est le fichier de configuration, les fichiers temporaires et les fichiers de cache de jeu du jeu. Ces fichiers sont généralement conservés dans le dossier Application Data. Pour obtenir ce chemin d’accès au dossier, appelez la fonction [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) avec CSIDL \_ AppData ou CSIDL \_ local \_ AppData comme indiqué dans l’exemple de code suivant.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

// Local Application Data
SHGetFolderPath( hWnd, CSIDL_LOCAL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
// Roaming Application Data
SHGetFolderPath( hWnd, CSIDL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

La différence entre les dossiers de données d’application locaux et itinérants réside dans le fait que sur Windows 2000 et Windows XP, le contenu itinérant est copié depuis et vers le serveur au cours du processus d’ouverture/de fermeture de session, contrairement au contenu local. Pour la plupart des jeux, les données d’application locales sont suffisantes.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Scénario 2 : fichiers qui doivent être affichés ou modifiés par les utilisateurs

Un exemple typique est un fichier de jeu enregistré par un utilisateur. Stockez les fichiers dans le dossier des documents de l’utilisateur afin qu’ils soient facilement visibles pour l’utilisateur. Une application obtient le chemin d’accès au dossier de documents de l’utilisateur en appelant [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) avec CSIDL \_ Personal, comme le montre l’exemple de code suivant :

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

Parfois, un jeu peut avoir besoin de stocker des fichiers que tous les utilisateurs sont censés voir et utiliser. Par exemple, l’enregistrement de score élevé, où tous les utilisateurs écrivent dans le même fichier d’enregistrement afin que les scores élevés soient gérés à l’ensemble du système au lieu d’un score élevé distinct pour chaque utilisateur. Voici d’autres exemples : cartes téléchargées, missions et modifications de jeux. S’ils sont partagés, un seul utilisateur doit les télécharger au lieu de tous les utilisateurs. Dans ce scénario, utilisez le dossier document sous le dossier profil partagé, comme illustré dans le code suivant.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_COMMON_DOCUMENTS, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

## <a name="registry-access-for-least-privileged-user-accounts"></a>Accès au registre pour les comptes d’utilisateurs Least-Privileged

Il est courant pour les applications d’utiliser le Registre Windows pour stocker des informations. Comme pour l’accès aux fichiers, les comptes d’utilisateur administrateur et avec privilèges minimum n’ont pas la même autorisation pour le registre. Pour les comptes d’utilisateur dotés de privilèges minimum, l’intégralité du nœud de l' \_ ordinateur local HKEY \_ est en lecture seule. Par exemple, un jeu peut lire les informations de configuration par défaut, mais il ne peut pas écrire de nouvelles informations sur ce nœud. Par conséquent, les jeux qui s’exécutent en mode utilisateur avec le moins de privilèges qui doivent écrire dans le registre doivent utiliser le nœud de l' \_ utilisateur HKEY actuel \_ pour stocker des informations par utilisateur, comme illustré dans le code suivant.

``` syntax
#define APP_REGISTRY_KEY_PATH L"Software\\MyCompany\\MyApp"

LONG lRetVal;
HKEY hKey;

lRetVal = RegCreateKeyExW( HKEY_CURRENT_USER,
                           APP_REGISTRY_KEY_PATH,
                           0,
                           NULL,
                           REG_OPTION_NON_VOLATILE,
                           KEY_WRITE|KEY_READ,
                           NULL,
                           &hKey,
                           NULL );

if( ERROR_SUCCESS == lRetVal )
{
    // Store information in hKey
}
```

Il est important de noter que lors de l’installation, les informations du Registre doivent être écrites sur HKEY \_ local \_ machine, et non sur HKEY \_ Current \_ User. Cela est dû au fait que la personne qui exécute l’installation est généralement un administrateur et peut ne pas être la seule personne à utiliser le programme. Dans ce cas, l’écriture sur HKEY \_ Current \_ User rend les informations indisponibles pour les autres utilisateurs. Ce n’est généralement pas un problème, car les informations écrites dans le registre au cours de l’installation sont les paramètres de configuration et par défaut qui s’appliquent à chaque utilisateur du programme.

Lors de la désinstallation du jeu, un effort supplémentaire est nécessaire pour supprimer toutes les valeurs que le jeu a écrites dans le registre. Étant donné que le désinstallateur est exécuté par une personne, généralement l’administrateur, il suffit de supprimer les informations pertinentes dans HKEY \_ local \_ machine et HKEY \_ Current \_ User ne supprimera pas les valeurs des autres utilisateurs. Une façon de supprimer les informations par utilisateur dans le registre consiste à énumérer la racine de la \_ ruche de Registre HKEY Users. Chaque sous-clé sous HKEY \_ Users correspond à la ruche de l' \_ utilisateur actuel HKEY \_ pour un utilisateur particulier sur le système. En énumérant HKEY \_ Users et en supprimant les informations spécifiques aux jeux sous chaque sous-clé, le désinstaller peut s’assurer qu’aucune information n’est conservée.

## <a name="patching-with-least-privileged-user-accounts"></a>Mise à jour corrective avec les comptes d’utilisateur Least-Privileged

La mise à jour corrective d’un jeu implique la mise à jour des fichiers du jeu. Par conséquent, elle nécessite généralement un accès en écriture au dossier programme du jeu. La mise à jour corrective d’un jeu est un processus simple lorsqu’il est effectué par un administrateur, car il dispose d’un accès illimité au dossier du programme du jeu. À l’inverse, il a traditionnellement été difficile, voire impossible, pour un utilisateur doté de privilèges minimaux d’appliquer des correctifs à des jeux en raison de la restriction d’accès. À présent, [Windows Installer](/windows/desktop/Msi/windows-installer-portal) a été amélioré pour rendre possible un correctif de compte d’utilisateur doté de privilèges minimum. Pour tirer parti de cette fonctionnalité, les jeux sont encouragés à utiliser Windows Installer pour l’installation et la mise à jour corrective.

À compter de Windows Installer 3,0, les correctifs d’application peuvent être appliqués par les utilisateurs disposant de privilèges minimum lorsque certaines conditions sont remplies. Ces conditions sont les suivantes :

-   L’application a été installée à l’aide de Windows Installer 3,0.
-   L’application a été installée à l’origine par ordinateur.
-   L’application est installée à partir d’un support amovible, tel qu’un CD-ROM ou un disque vidéo numérique (DVD).
-   Les correctifs sont signés numériquement par un certificat identifié par le package d’installation d’origine (fichier. msi).
-   Les correctifs peuvent être validés par rapport à la signature numérique.
-   Le package d’installation d’origine n’a pas désactivé la mise à jour corrective des comptes d’utilisateur de moindre privilège.
-   L’administrateur système n’a pas désactivé la mise à jour corrective des comptes d’utilisateur avec des privilèges minimaux via la stratégie système.

En règle générale, un utilisateur doté de privilèges minimum ne peut pas modifier les fichiers programme d’un jeu. Toutefois, lorsque les conditions ci-dessus sont remplies et que la mise à jour corrective LUA est activée, Windows Installer pouvez mettre à jour les fichiers du jeu afin que l’utilisateur puisse obtenir la dernière version.

> [!Note]  
> Les informations contenues dans cet article concernent le produit logiciel en version préliminaire, qui peut être sensiblement modifié avant sa première version commerciale. En conséquence, les informations peuvent ne pas décrire ou refléter le produit logiciel lors de la première publication commercialisée. Cet article est fourni à titre d’information uniquement et Microsoft exclut toute garantie, expresse ou implicite, en ce qui concerne cet article ou les informations qu’il contient.

 

 

 