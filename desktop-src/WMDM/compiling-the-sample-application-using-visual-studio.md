---
title: Compilation de l’exemple d’application à l’aide de Visual Studio
description: Compilation de l’exemple d’application à l’aide de Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Gestionnaire de périphériques de média, exemples
- Gestionnaire de périphériques, exemples
- applications de bureau, exemples
- Windows Media Gestionnaire de périphériques, exemple d’application de bureau
- Gestionnaire de périphériques, exemple d’application de bureau
- exemples, applications de bureau
- exemples, compilation à l’aide de Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8b32cd5931a88bc41b8eee7171b6ab4ab18b629a8108007d68094180efaa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586250"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilation de l’exemple d’application à l’aide de Visual Studio

le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques comprend une solution Visual Studio compatible avec Microsoft Visual Studio 2005.

Avant de compiler l’exemple d’application, vous devez renommer le fichier d’en-tête shtypes. h pour empêcher les conflits avec un fichier portant le même nom que celui qui se trouve dans le kit de développement logiciel (SDK) Microsoft Platform. Par exemple, vous pouvez renommer <*chemin d’installation du kit de développement logiciel* > \\ WMFSDK11 \\ inclure \\ shtypes. h pour <*chemin d’installation du kit de développement logiciel (SDK)* > \\ WMFSDK11 \\ include \\ shtypes. h. Backup.

pour générer l’application, démarrez une instance de Visual Studio 2005, ouvrez le fichier solution wmdmapp. sln qui se trouve dans le dossier <*chemin d’installation du kit de développement logiciel (SDK)* > \\ WMFSDK11 \\ apps \\ wmdmapp et choisissez l’option **générer/générer la solution** . Cela permet de créer deux fichiers projet : le projet d’assistance, proghelp. vcproj, ainsi que l’application principale wmdmapp. vcproj. En outre, il crée la DLL d’assistance de progression et l’application principale (WMDMApp.exe).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple d’application de bureau**](sample-desktop-application.md)
</dt> </dl>

 

 




