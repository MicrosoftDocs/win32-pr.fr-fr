---
description: Les applications peuvent contrôler l’emplacement à partir duquel une DLL est chargée en spécifiant un chemin d’accès complet ou en utilisant un autre mécanisme tel qu’un manifeste. Si ces méthodes ne sont pas utilisées, le système recherche la DLL au moment du chargement, comme décrit dans cette rubrique.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Ordre de recherche de la bibliothèque Dynamic-Link
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 73c90e176983aa542ec524c2bfa32623821c2f21
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991836"
---
# <a name="dynamic-link-library-search-order"></a>Ordre de recherche de la bibliothèque Dynamic-Link

Un système peut contenir plusieurs versions de la même bibliothèque de liens dynamiques (DLL). Les applications peuvent contrôler l’emplacement à partir duquel une DLL est chargée en spécifiant un chemin d’accès complet ou en utilisant un autre mécanisme tel qu’un manifeste. Si ces méthodes ne sont pas utilisées, le système recherche la DLL au moment du chargement, comme décrit dans cette rubrique.

-   [Facteurs qui affectent la recherche](#factors-that-affect-searching)
-   [Ordre de recherche des applications UWP](#search-order-for-uwp-apps)
    -   [Ordre de recherche standard pour les applications UWP](#standard-search-order-for-uwp-apps)
    -   [Ordre de recherche alternatif pour les applications UWP](#alternate-search-order-for-uwp-apps)
-   [Ordre de recherche pour les applications de bureau](#search-order-for-desktop-applications)
    -   [Ordre de recherche standard pour les applications de bureau](#standard-search-order-for-desktop-applications)
    -   [Ordre de recherche alternatif pour les applications de bureau](#alternate-search-order-for-desktop-applications)
    -   [Ordre de recherche à l’aide des indicateurs de **\_ \_ recherche** de la bibliothèque de chargement](#search-order-using-load_library_search-flags)
-   [Rubriques connexes](#related-topics)

## <a name="factors-that-affect-searching"></a>Facteurs qui affectent la recherche

Les facteurs suivants déterminent si le système recherche une DLL :

-   Si une DLL portant le même nom de module est déjà chargée en mémoire, le système vérifie uniquement la redirection et un manifeste avant de résoudre la DLL chargée, quel que soit le répertoire dans lequel elle se trouve. Le système ne recherche pas la DLL.
-   si la dll se trouve dans la liste des dll connues pour la version de Windows sur laquelle l’application s’exécute, le système utilise sa copie de la dll connue (et les dll dépendantes de la dll connue, le cas échéant) au lieu de rechercher la dll. Pour obtenir la liste des dll connues sur le système actuel, consultez la clé de Registre suivante : **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.
-   Si une DLL a des dépendances, le système recherche les dll dépendantes comme si elles étaient chargées avec uniquement leurs noms de module. Cela est vrai même si la première DLL a été chargée en spécifiant un chemin d’accès complet.

## <a name="search-order-for-uwp-apps"></a>Ordre de recherche des applications UWP

quand une application UWP pour Windows 10 (ou une application de Store pour Windows 8. x) charge un module empaqueté en appelant la fonction [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) , la DLL doit se trouver dans le graphique de dépendance du package du processus. Pour plus d’informations, consultez **LoadPackagedLibrary**. Quand une application UWP charge un module par d’autres moyens et ne spécifie pas de chemin d’accès complet, le système recherche la DLL et ses dépendances au moment du chargement, comme décrit dans cette section.

Avant que le système ne recherche une DLL, il vérifie les éléments suivants :

-   Si une DLL portant le même nom de module est déjà chargée en mémoire, le système utilise la DLL chargée, quel que soit le répertoire dans lequel elle se trouve. Le système ne recherche pas la DLL.
-   si la dll se trouve dans la liste des dll connues pour la version de Windows sur laquelle l’application s’exécute, le système utilise sa copie de la dll connue (et les dll dépendantes de la dll connue, le cas échéant). Le système ne recherche pas la DLL. Pour obtenir la liste des dll connues sur le système actuel, consultez la clé de Registre suivante : **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.

Si le système doit rechercher un module ou ses dépendances, il utilise toujours l’ordre de recherche des applications UWP, même si une dépendance n’est pas un code d’application UWP.

### <a name="standard-search-order-for-uwp-apps"></a>Ordre de recherche standard pour les applications UWP

Si le module n’est pas déjà chargé ou dans la liste des dll connues, le système recherche les emplacements suivants dans cet ordre :

1.  Graphique de dépendance du package du processus. Il s’agit du package de l’application et de toutes les dépendances spécifiées comme `<PackageDependency>` dans la `<Dependencies>` section du manifeste du package de l’application. Les dépendances sont recherchées dans l’ordre dans lequel elles apparaissent dans le manifeste.
2.  Répertoire à partir duquel le processus appelant a été chargé.
3.  Répertoire système (% SystemRoot% \\ system32).

Si une DLL a des dépendances, le système recherche les dll dépendantes comme si elles étaient chargées avec uniquement leurs noms de module. Cela est vrai même si la première DLL a été chargée en spécifiant un chemin d’accès complet.

### <a name="alternate-search-order-for-uwp-apps"></a>Ordre de recherche alternatif pour les applications UWP

Si un module modifie l’ordre de recherche standard en appelant la fonction [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) avec le **\_ \_ \_ \_ chemin de recherche modifié**, le système recherche dans le répertoire que le module spécifié a été chargé à partir du répertoire du processus appelant. Le système recherche les emplacements suivants dans cet ordre :

1.  Graphique de dépendance du package du processus. Il s’agit du package de l’application et de toutes les dépendances spécifiées comme `<PackageDependency>` dans la `<Dependencies>` section du manifeste du package de l’application. Les dépendances sont recherchées dans l’ordre dans lequel elles apparaissent dans le manifeste.
2.  Répertoire à partir duquel le module spécifié a été chargé.
3.  Répertoire système (% SystemRoot% \\ system32).

## <a name="search-order-for-desktop-applications"></a>Ordre de recherche pour les applications de bureau

Les applications de bureau peuvent contrôler l’emplacement à partir duquel une DLL est chargée en spécifiant un chemin d’accès complet, à l’aide de la [redirection de dll](dynamic-link-library-redirection.md)ou à l’aide d’un [manifeste](/windows/desktop/SbsCs/manifests). Si aucune de ces méthodes n’est utilisée, le système recherche la DLL au moment du chargement, comme décrit dans cette section.

Avant que le système ne recherche une DLL, il vérifie les éléments suivants :

-   Si une DLL portant le même nom de module est déjà chargée en mémoire, le système utilise la DLL chargée, quel que soit le répertoire dans lequel elle se trouve. Le système ne recherche pas la DLL.
-   si la dll se trouve dans la liste des dll connues pour la version de Windows sur laquelle l’application s’exécute, le système utilise sa copie de la dll connue (et les dll dépendantes de la dll connue, le cas échéant). Le système ne recherche pas la DLL. Pour obtenir la liste des dll connues sur le système actuel, consultez la clé de Registre suivante : **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.

Si une DLL a des dépendances, le système recherche les dll dépendantes comme si elles étaient chargées avec uniquement leurs noms de module. Cela est vrai même si la première DLL a été chargée en spécifiant un chemin d’accès complet.

> [!IMPORTANT]
> Si une personne malveillante prend le contrôle de l’un des répertoires dans lesquels elle est recherchée, elle peut placer une copie malveillante de la DLL dans ce répertoire. Pour plus d’informations sur les méthodes permettant d’éviter de telles attaques, consultez [sécurité de la bibliothèque de liens dynamiques](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Ordre de recherche standard pour les applications de bureau

L’ordre de recherche des DLL standard utilisé par le système varie selon que le mode de recherche de DLL sécurisé est activé ou désactivé. Coffre Le mode de recherche DLL place le répertoire actuel de l’utilisateur plus tard dans l’ordre de recherche.

Coffre Le mode de recherche DLL est activé par défaut. Pour désactiver cette fonctionnalité, créez la valeur de Registre SafeDllSearchMode du **\_ Gestionnaire de \_ \\ \\ \\ \\ session** de la clé HKEY locale de l’ordinateur local \\  et affectez-lui la valeur 0. L’appel de la fonction [**SetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) désactive efficacement **SafeDllSearchMode** alors que le répertoire spécifié se trouve dans le chemin de recherche et modifie l’ordre de recherche comme décrit dans cette rubrique.

Si **SafeDllSearchMode** est activé, l’ordre de recherche est le suivant :

1.  Répertoire à partir duquel l’application a été chargée.
2.  Répertoire du système. Utilisez la fonction [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) pour récupérer le chemin d’accès à ce répertoire.
3.  Répertoire système 16 bits. Aucune fonction n’obtient le chemin d’accès de ce répertoire, mais elle est recherchée.
4.  répertoire Windows. Utilisez la fonction [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) pour récupérer le chemin d’accès à ce répertoire.
5.  Le répertoire actif.
6.  Répertoires répertoriés dans la variable d’environnement PATH. Notez que cela n’inclut pas le chemin d’accès par application spécifié par la clé de Registre **App Paths** . La clé **chemins d’accès** à l’application n’est pas utilisée lors du calcul du chemin de recherche de dll.

Si **SafeDllSearchMode** est désactivé, l’ordre de recherche est le suivant :

1.  Répertoire à partir duquel l’application a été chargée.
2.  Le répertoire actif.
3.  Répertoire du système. Utilisez la fonction [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) pour récupérer le chemin d’accès à ce répertoire.
4.  Répertoire système 16 bits. Aucune fonction n’obtient le chemin d’accès de ce répertoire, mais elle est recherchée.
5.  répertoire Windows. Utilisez la fonction [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) pour récupérer le chemin d’accès à ce répertoire.
6.  Répertoires répertoriés dans la variable d’environnement PATH. Notez que cela n’inclut pas le chemin d’accès par application spécifié par la clé de Registre **App Paths** . La clé **chemins d’accès** à l’application n’est pas utilisée lors du calcul du chemin de recherche de dll.

### <a name="alternate-search-order-for-desktop-applications"></a>Ordre de recherche alternatif pour les applications de bureau

L’ordre de recherche standard utilisé par le système peut être modifié en appelant la fonction [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) avec le **\_ \_ \_ \_ chemin de recherche modifié**. L’ordre de recherche standard peut également être modifié en appelant la fonction [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

> [!NOTE]
> L’ordre de recherche standard du processus est également affecté par l’appel de la fonction [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) dans le processus parent avant le démarrage du processus actuel.

Si vous spécifiez une autre stratégie de recherche, son comportement continue jusqu’à ce que tous les modules exécutables associés aient été localisés. Une fois que le système a démarré le traitement des routines d’initialisation de la DLL, le système revient à la stratégie de recherche standard.

La fonction [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) prend en charge un ordre de recherche alternatif si l’appel spécifie le **chargement avec un \_ \_ \_ \_ chemin de recherche modifié** et le paramètre *lpFileName* spécifie un chemin d’accès absolu.

Notez que la stratégie de recherche standard et la stratégie de recherche alternative spécifiée par [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) avec le **\_ \_ \_ \_ chemin de recherche modifié** diffèrent d’une seule façon : la recherche standard commence dans le répertoire de l’application appelante, et l’autre recherche commence dans le répertoire du module exécutable que **LoadLibraryEx** est en cours de chargement.

Si **SafeDllSearchMode** est activé, l’ordre de recherche alternatif est le suivant :

1.  Répertoire spécifié par *lpFileName*.
2.  Répertoire du système. Utilisez la fonction [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) pour récupérer le chemin d’accès à ce répertoire.
3.  Répertoire système 16 bits. Aucune fonction n’obtient le chemin d’accès de ce répertoire, mais elle est recherchée.
4.  répertoire Windows. Utilisez la fonction [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) pour récupérer le chemin d’accès à ce répertoire.
5.  Le répertoire actif.
6.  Répertoires répertoriés dans la variable d’environnement PATH. Notez que cela n’inclut pas le chemin d’accès par application spécifié par la clé de Registre **App Paths** . La clé **chemins d’accès** à l’application n’est pas utilisée lors du calcul du chemin de recherche de dll.

Si **SafeDllSearchMode** est désactivé, l’ordre de recherche alternatif est le suivant :

1.  Répertoire spécifié par *lpFileName*.
2.  Le répertoire actif.
3.  Répertoire du système. Utilisez la fonction [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) pour récupérer le chemin d’accès à ce répertoire.
4.  Répertoire système 16 bits. Aucune fonction n’obtient le chemin d’accès de ce répertoire, mais elle est recherchée.
5.  répertoire Windows. Utilisez la fonction [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) pour récupérer le chemin d’accès à ce répertoire.
6.  Répertoires répertoriés dans la variable d’environnement PATH. Notez que cela n’inclut pas le chemin d’accès par application spécifié par la clé de Registre **App Paths** . La clé **chemins d’accès** à l’application n’est pas utilisée lors du calcul du chemin de recherche de dll.

La fonction [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) prend en charge un ordre de recherche alternatif si le paramètre *lpPathName* spécifie un chemin d’accès. L’ordre de recherche alternatif est le suivant :

1.  Répertoire à partir duquel l’application a été chargée.
2.  Répertoire spécifié par le paramètre *lpPathName* de [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya).
3.  Répertoire du système. Utilisez la fonction [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) pour récupérer le chemin d’accès à ce répertoire. Le nom de ce répertoire est system32.
4.  Répertoire système 16 bits. Aucune fonction n’obtient le chemin d’accès de ce répertoire, mais elle est recherchée. Le nom de ce répertoire est System.
5.  répertoire Windows. Utilisez la fonction [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) pour récupérer le chemin d’accès à ce répertoire.
6.  Répertoires répertoriés dans la variable d’environnement PATH. Notez que cela n’inclut pas le chemin d’accès par application spécifié par la clé de Registre **App Paths** . La clé **chemins d’accès** à l’application n’est pas utilisée lors du calcul du chemin de recherche de dll.

Si le paramètre *lpPathName* est une chaîne vide, l’appel supprime le répertoire actif de l’ordre de recherche.

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) désactive efficacement le mode de recherche de dll sécurisée lorsque le répertoire spécifié se trouve dans le chemin de recherche. Pour restaurer le mode de recherche de DLL sécurisée en fonction de la valeur de Registre **SafeDllSearchMode** et restaurer le répertoire actif dans l’ordre de recherche, appelez **SetDllDirectory** avec *lpPathName* comme valeur null.

### <a name="search-order-using-load_library_search-flags"></a>Ordre de recherche à l’aide des indicateurs de **\_ \_ recherche** de la bibliothèque de chargement

Une application peut spécifier un ordre de recherche à l’aide d’un ou plusieurs indicateurs de **\_ \_ recherche** de la bibliothèque de chargement avec la fonction [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Une application peut également utiliser les indicateurs de **\_ \_ recherche** de la bibliothèque de chargement avec la fonction [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) pour établir un ordre de recherche de dll pour un processus. L’application peut spécifier des répertoires supplémentaires pour l’ordre de recherche des DLL du processus à l’aide des fonctions [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) ou [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

Les répertoires recherchés dépendent des indicateurs spécifiés avec [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Si plusieurs indicateurs sont utilisés, les répertoires correspondants sont recherchés dans l’ordre suivant :

1.  Répertoire qui contient la DLL (chargement de la dll de recherche de la **bibliothèque de chargement \_ \_ \_ \_ \_**). Ce répertoire est recherché uniquement pour les dépendances de la DLL à charger.
2.  Le répertoire de l’application (chargement de l’application de recherche dans la **\_ bibliothèque \_ \_ \_**).
3.  Les chemins d’accès ont été ajoutés explicitement avec la fonction [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) (**charger la \_ bibliothèque Rechercher les \_ \_ \_ répertoires utilisateur**) ou la fonction [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) . Si plusieurs chemins d’accès ont été ajoutés, l’ordre dans lequel les chemins d’accès sont recherchés n’est pas spécifié.
4.  Le répertoire système (**chargement de la \_ recherche de bibliothèque \_ \_ system32**).

Si l’application n’appelle pas [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) avec les indicateurs de **\_ \_ recherche** de la bibliothèque de chargement ou établit un ordre de recherche de dll pour le processus, le système recherche des dll à l’aide de l’ordre de recherche standard ou de l’ordre de recherche alternatif.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[Inscription de l’application](/windows/desktop/shell/app-registration)
</dt> <dt>

[Redirection de bibliothèque de liens dynamiques](dynamic-link-library-redirection.md)
</dt> <dt>

[Sécurité de la bibliothèque de liens dynamiques](dynamic-link-library-security.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
</dt> <dt>

[**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)
</dt> <dt>

[**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)
</dt> <dt>

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
</dt> <dt>

[Composants côte à côte](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 
