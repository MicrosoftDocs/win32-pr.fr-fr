---
title: Compilation de l’exemple d’application à l’aide de Visual Studio
description: Compilation de l’exemple d’application à l’aide de Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Gestionnaire de périphériques Windows Media, exemples
- Gestionnaire de périphériques, exemples
- applications de bureau, exemples
- Windows Media Gestionnaire de périphériques, exemple d’application de bureau
- Gestionnaire de périphériques, exemple d’application de bureau
- exemples, applications de bureau
- exemples, compilation à l’aide de Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028980"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilation de l’exemple d’application à l’aide de Visual Studio

Le kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media comprend une solution Visual Studio compatible avec Microsoft Visual Studio 2005.

Avant de compiler l’exemple d’application, vous devez renommer le fichier d’en-tête shtypes. h pour empêcher les conflits avec un fichier portant le même nom que celui qui se trouve dans le kit de développement logiciel (SDK) Microsoft Platform. Par exemple, vous pouvez renommer <*chemin d’installation du kit de développement logiciel* > \\ WMFSDK11 \\ inclure \\ shtypes. h pour <*chemin d’installation du kit de développement logiciel (SDK)* > \\ WMFSDK11 \\ include \\ shtypes. h. Backup.

Pour générer l’application, démarrez une instance de Visual Studio 2005, ouvrez le fichier solution, wmdmapp. sln, qui se trouve dans le dossier <*chemin d’installation du kit de développement logiciel (SDK)* > \\ WMFSDK11 \\ apps \\ wmdmapp et choisissez l’option **générer/générer la solution** . Cela permet de créer deux fichiers projet : le projet d’assistance, proghelp. vcproj, ainsi que l’application principale wmdmapp. vcproj. En outre, il crée la DLL d’assistance de progression et l’application principale (WMDMApp.exe).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple d’application de bureau**](sample-desktop-application.md)
</dt> </dl>

 

 




