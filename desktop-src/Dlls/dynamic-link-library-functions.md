---
description: Les fonctions suivantes sont utilisées dans la liaison dynamique.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Dynamic-Link les fonctions de la bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47ce37b6f91570ce9f3314fc329b5e85cde310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868258"
---
# <a name="dynamic-link-library-functions"></a>Dynamic-Link les fonctions de la bibliothèque

Les fonctions suivantes sont utilisées dans la liaison dynamique.



| Fonction                                                       | Description                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Ajoute un répertoire au chemin de recherche de DLL du processus.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Désactive les notifications d’attachement de thread et de détachement de thread pour la DLL spécifiée.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Point d’entrée facultatif dans une DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Décrémente le décompte de références de la DLL chargée. Lorsque le décompte de références atteint zéro, le module n’est pas mappé à partir de l’espace d’adressage du processus appelant. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Décrémente le décompte de références d’une DLL chargée, puis appelle [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) pour terminer le thread appelant.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Récupère la partie spécifique à l’application du chemin de recherche utilisé pour localiser les dll de l’application.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Récupère le chemin d’accès qualifié complet du fichier contenant le module spécifié.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Récupère le chemin d’accès qualifié complet du fichier contenant le module spécifié.                                                                               |
| [**Échec GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Récupère un handle de module pour le module spécifié.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Récupère un handle de module pour le module spécifié.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Récupère l’adresse d’une fonction ou d’une variable exportée à partir de la DLL spécifiée.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Mappe le module exécutable spécifié dans l’espace d’adressage du processus appelant.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Mappe le module exécutable spécifié dans l’espace d’adressage du processus appelant.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Mappe le module empaqueté spécifié et ses dépendances dans l’espace d’adressage du processus appelant. Seules les applications du Windows Store peuvent appeler cette fonction.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Supprime un répertoire qui a été ajouté au chemin de recherche de DLL du processus à l’aide de [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Spécifie un jeu de répertoires par défaut à rechercher lorsque le processus appelant charge une DLL.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Modifie le chemin de recherche utilisé pour localiser les dll de l’application.                                                                                              |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

Ces fonctions sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Windows.

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
