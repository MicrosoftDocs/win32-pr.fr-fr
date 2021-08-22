---
description: quand une application charge dynamiquement une bibliothèque de liens dynamiques sans spécifier de nom de chemin d’accès qualifié complet, Windows tente de localiser la DLL en recherchant un ensemble bien défini de répertoires dans un ordre particulier, comme décrit dans Dynamic-Link ordre de recherche de la bibliothèque. Si un attaquant gagne le contrôle de l’un des répertoires du chemin de recherche de DLL, il peut placer une copie malveillante de la DLL dans ce répertoire. C’est ce qu’on appelle parfois une attaque de préchargement de DLL ou une attaque de plantation binaire.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Sécurité de la bibliothèque de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582122debce68ade593c007e431e62a91a7fa07f395f148b7eaa05cac13bc56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290399"
---
# <a name="dynamic-link-library-security"></a>Sécurité de la bibliothèque de Dynamic-Link

quand une application charge dynamiquement une bibliothèque de liens dynamiques sans spécifier de nom de chemin complet, Windows tente de localiser la DLL en recherchant un ensemble bien défini de répertoires dans un ordre particulier, comme décrit dans l’ordre de recherche de la [bibliothèque de liens dynamiques](dynamic-link-library-search-order.md). Si un attaquant gagne le contrôle de l’un des répertoires du chemin de recherche de DLL, il peut placer une copie malveillante de la DLL dans ce répertoire. C’est ce qu’on appelle parfois une attaque de *préchargement de dll* ou une *attaque de plantation binaire*. Si le système ne trouve pas de copie légitime de la DLL avant de rechercher le répertoire compromis, il charge la DLL malveillante. Si l’application s’exécute avec des privilèges d’administrateur, l’attaquant peut parvenir à une élévation de privilèges locale.

Supposons, par exemple, qu’une application soit conçue pour charger une DLL à partir du répertoire actuel de l’utilisateur et échouer correctement si la DLL est introuvable. L’application appelle [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) uniquement avec le nom de la dll, ce qui amène le système à rechercher la dll. En supposant que le mode de recherche de DLL sécurisé est activé et que l’application n’utilise pas d’autre ordre de recherche, le système recherche les répertoires dans l’ordre suivant :

1.  Répertoire à partir duquel l’application a été chargée.
2.  Répertoire du système.
3.  Répertoire système 16 bits.
4.  répertoire Windows.
5.  Le répertoire actif.
6.  Répertoires répertoriés dans la variable d’environnement PATH.

En poursuivant l’exemple, une personne malveillante ayant connaissance de l’application prend le contrôle du répertoire actuel et place une copie malveillante de la DLL dans ce répertoire. Lorsque l’application émet l’appel **LoadLibrary** , le système recherche la dll, recherche la copie malveillante de la dll dans le répertoire actif et la charge. La copie malveillante de la DLL s’exécute ensuite dans l’application et obtient les privilèges de l’utilisateur.

Les développeurs peuvent aider à protéger leurs applications contre les attaques de préchargement de DLL en suivant ces instructions :

-   Dans la mesure du possible, spécifiez un chemin d’accès complet lorsque vous utilisez les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)ou [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) .
-   Utilisez les \_ indicateurs de \_ recherche de la bibliothèque de chargement avec la fonction [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , ou utilisez ces indicateurs avec la fonction [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) pour établir un ordre de recherche de dll pour un processus, puis utilisez les fonctions [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) ou [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) pour modifier la liste. Pour plus d’informations, consultez ordre de recherche de la [bibliothèque de liens dynamiques](dynamic-link-library-search-order.md).

    **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Ces indicateurs et fonctions sont disponibles sur les systèmes sur lesquels [KB2533623](https://support.microsoft.com/kb/2533623) est installé.

-   Sur les systèmes sur lesquels [KB2533623](https://support.microsoft.com/kb/2533623) est installé, utilisez les indicateurs de recherche de la \_ bibliothèque \_ de chargement avec la fonction [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , ou utilisez ces indicateurs avec la fonction [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) pour établir un ordre de recherche de dll pour un processus, puis utilisez les fonctions [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) ou [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) pour modifier la liste. Pour plus d’informations, consultez ordre de recherche de la [bibliothèque de liens dynamiques](dynamic-link-library-search-order.md).
-   Envisagez d’utiliser la [redirection de dll](dynamic-link-library-redirection.md) ou un [manifeste](/windows/desktop/SbsCs/manifests) pour vous assurer que votre application utilise la dll correcte.
-   Lorsque vous utilisez l’ordre de recherche standard, assurez-vous que le mode de recherche de DLL sécurisé est activé. cela place le répertoire actuel de l’utilisateur plus tard dans l’ordre de recherche, ce qui augmente le risque que Windows trouve une copie légitime de la DLL avant une copie malveillante. Coffre le mode de recherche DLL est activé par défaut à partir de Windows XP avec Service Pack 2 (SP2) et est contrôlé par la valeur de registre SafeDllSearchMode du **\_ gestionnaire de \_ \\ \\ \\ \\ sessions HKEY LOCAL MACHINE System** \\  . Pour plus d’informations, consultez ordre de recherche de la [bibliothèque de liens dynamiques](dynamic-link-library-search-order.md).
-   Envisagez de supprimer le répertoire actif du chemin de recherche standard en appelant [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) avec une chaîne vide (""). Cela doit être fait une fois au début de l’initialisation du processus, et non avant et après les appels à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Sachez que **SetDllDirectory** affecte l’ensemble du processus et que plusieurs threads appelant **SetDllDirectory** avec des valeurs différentes peuvent entraîner un comportement indéfini. Si votre application charge des dll tierces, testez-les soigneusement pour identifier les incompatibilités.
-   N’utilisez pas la fonction [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) pour récupérer un chemin d’accès à une dll pour un appel [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ultérieur, sauf si le mode de recherche de processus sécurisé est activé. Lorsque le mode de recherche de processus sécurisé n’est pas activé, la fonction **SearchPath** utilise un ordre de recherche différent de **LoadLibrary** et est susceptible d’effectuer une recherche dans le répertoire actuel de l’utilisateur pour la DLL spécifiée. Pour activer le mode de recherche de processus sécurisé pour la fonction **SearchPath** , utilisez la fonction [**SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) avec le chemin de recherche de base \_ \_ \_ Enable \_ Safe \_ searchmode. Cela déplace le répertoire actif à la fin de la liste de recherche de la **SearchPath** pendant la durée de vie du processus. Notez que le répertoire actif n’est pas supprimé du chemin de recherche. par conséquent, si le système ne trouve pas de copie légitime de la DLL avant qu’il n’atteigne le répertoire actif, l’application est toujours vulnérable. Comme avec [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya), l’appel de **SetSearchPathMode** doit être effectué tôt dans l’initialisation du processus et affecte l’ensemble du processus. Si votre application charge des dll tierces, testez-les soigneusement pour identifier les incompatibilités.
-   N’effectuez pas d’hypothèses sur la version du système d’exploitation en fonction d’un appel [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) qui recherche une dll. Si l’application s’exécute dans un environnement où la DLL est légitimement absente mais où une copie malveillante de la DLL se trouve dans le chemin de recherche, la copie malveillante de la DLL peut être chargée. Utilisez plutôt les techniques recommandées décrites dans [obtention de la version du système](/windows/desktop/SysInfo/getting-the-system-version).

L’outil process Monitor peut être utilisé pour identifier les opérations de chargement de DLL susceptibles d’être vulnérables. L’outil process Monitor peut être téléchargé à partir de <https://technet.microsoft.com/sysinternals/bb896645.aspx> .

La procédure suivante décrit comment utiliser process Monitor pour examiner les opérations de chargement des DLL dans votre application.

**Pour utiliser process Monitor afin d’examiner les opérations de chargement des DLL dans votre application**

1.  Démarrez le moniteur de processus.
2.  Dans Process Monitor, incluez les filtres suivants :
    -   L’opération est CreateFile
    -   L’opération est LoadImage
    -   Le chemin d’accès contient .cpl
    -   Le chemin d’accès contient .dll
    -   Le chemin d’accès contient. drv
    -   Le chemin d’accès contient .exe
    -   Le chemin d’accès contient. ocx
    -   Le chemin contient. SCR
    -   Le chemin d’accès contient .sys
3.  Excluez les filtres suivants :
    -   Le nom du processus est procmon.exe
    -   Le nom du processus est Procmon64.exe
    -   Le nom du processus est System
    -   L’opération commence avec IRP \_ MJ\_
    -   L’opération commence par FASTIO\_
    -   Résultat réussi
    -   Le chemin d’accès se termine par pagefile.sys
4.  Essayez de démarrer votre application avec le répertoire actif défini sur un répertoire spécifique. Par exemple, double-cliquez sur un fichier avec une extension dont le gestionnaire de fichiers est assigné à votre application.
5.  Vérifiez la sortie de process Monitor pour les chemins d’accès suspects, tels qu’un appel au répertoire actif pour charger une DLL. Ce type d’appel peut indiquer une vulnérabilité dans votre application.

 

 
