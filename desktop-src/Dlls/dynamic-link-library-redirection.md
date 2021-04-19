---
description: Les applications peuvent dépendre d’une version spécifique d’une DLL partagée et commencer à échouer si une autre application est installée avec une version plus récente ou plus ancienne de la même DLL.
ms.assetid: 3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8
title: Redirection de la bibliothèque de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d566231058cca13c10a067a3c2e20078073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534391"
---
# <a name="dynamic-link-library-redirection"></a>Redirection de la bibliothèque de Dynamic-Link

Les applications peuvent dépendre d’une version spécifique d’une DLL partagée et commencer à échouer si une autre application est installée avec une version plus récente ou plus ancienne de la même DLL. Il existe deux façons de s’assurer que votre application utilise la DLL correcte : la redirection de DLL et les composants côte à côte. Les développeurs et les administrateurs doivent utiliser la redirection de DLL pour les applications existantes, car elles ne nécessitent aucune modification de l’application. Si vous créez une nouvelle application ou que vous mettez à jour une application et souhaitez isoler votre application des problèmes potentiels, créez un [composant côte à côte](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Pour activer la redirection de DLL au niveau de l’ordinateur, vous devez créer une nouvelle clé de registre. Créez une nouvelle clé DWORD appelée **DevOverrideEnable** dans **HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution** , puis définissez-la sur 1. Après cela, vous devez redémarrer votre ordinateur pour voir les effets.

Pour utiliser la redirection de DLL, créez un *fichier de redirection* pour votre application. Le fichier de redirection doit être nommé comme suit : *app \_ Name*. local. Par exemple, si le nom de l’application est Editor.exe, le fichier de redirection doit être nommé Editor.exe. local. Vous devez installer le fichier. local dans le répertoire de l’application. Vous devez également installer les dll dans le répertoire de l’application.

Le contenu d’un fichier de redirection est ignoré, mais sa présence fait que Windows vérifie d’abord le répertoire de l’application chaque fois qu’il charge une DLL, quel que soit le chemin d’accès spécifié pour [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Si la DLL est introuvable dans le répertoire de l’application, ces fonctions utilisent leur ordre de recherche habituel. Par exemple, si l’application c : \\ myapp \\myapp.exe appelle **LoadLibrary** à l’aide du chemin d’accès suivant :

c : \\ Program Files \\ système de fichiers communs \\ \\mydll.dll

Et, si c : \\ myapp \\myapp.exe. local et c : \\ MyApp \\mydll.dll existent, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) charge c : \\ MyApp \\mydll.dll. Sinon, **LoadLibrary** charge le \\ système de fichiers communs c : Program Files \\ \\ \\mydll.dll.

Sinon, si un répertoire nommé c : \\ myapp \\myapp.exe. local existe et contient mydll.dll, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) charge c : \\ MyApp \\myapp.exe. local \\mydll.dll.

Si l’application a un manifeste, tous les fichiers. local sont ignorés.

Si vous utilisez la redirection de DLL et que l’application n’a pas accès à tous les lecteurs et répertoires dans l’ordre de recherche, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) arrête la recherche dès que l’accès est refusé. (Si vous n’utilisez pas la redirection de DLL, **LoadLibrary** ignore les répertoires auxquels il ne peut pas accéder, puis poursuit la recherche.)

Il est recommandé d’installer des dll d’application dans le même répertoire que celui qui contient l’application, même si vous n’utilisez pas la redirection de DLL. Cela permet de s’assurer que l’installation de l’application ne remplace pas d’autres copies de la DLL et provoque l’échec d’autres applications. En outre, si vous suivez cette bonne pratique, les autres applications ne remplacent pas votre copie de la DLL et provoquent l’échec de votre application.

 

 
