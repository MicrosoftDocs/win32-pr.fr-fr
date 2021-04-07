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
# <a name="compiling-the-sample-application-using-visual-studio"></a><span data-ttu-id="a6f0f-110">Compilation de l’exemple d’application à l’aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a6f0f-110">Compiling the Sample Application Using Visual Studio</span></span>

<span data-ttu-id="a6f0f-111">Le kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media comprend une solution Visual Studio compatible avec Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="a6f0f-111">The Windows Media Device Manager SDK includes a Visual Studio solution that is compatible with Microsoft Visual Studio 2005.</span></span>

<span data-ttu-id="a6f0f-112">Avant de compiler l’exemple d’application, vous devez renommer le fichier d’en-tête shtypes. h pour empêcher les conflits avec un fichier portant le même nom que celui qui se trouve dans le kit de développement logiciel (SDK) Microsoft Platform.</span><span class="sxs-lookup"><span data-stu-id="a6f0f-112">Before you compile the sample application, you must rename the header file shtypes.h to prevent conflicts with a file of the same name that is found in the Microsoft Platform SDK.</span></span> <span data-ttu-id="a6f0f-113">Par exemple, vous pouvez renommer <*chemin d’installation du kit de développement logiciel* > \\ WMFSDK11 \\ inclure \\ shtypes. h pour <*chemin d’installation du kit de développement logiciel (SDK)* > \\ WMFSDK11 \\ include \\ shtypes. h. Backup.</span><span class="sxs-lookup"><span data-stu-id="a6f0f-113">For example, you could rename <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h to <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h.backup.</span></span>

<span data-ttu-id="a6f0f-114">Pour générer l’application, démarrez une instance de Visual Studio 2005, ouvrez le fichier solution, wmdmapp. sln, qui se trouve dans le dossier <*chemin d’installation du kit de développement logiciel (SDK)* > \\ WMFSDK11 \\ apps \\ wmdmapp et choisissez l’option **générer/générer la solution** .</span><span class="sxs-lookup"><span data-stu-id="a6f0f-114">To build the application, start an instance of Visual Studio 2005, open the solution file, wmdmapp.sln, which is found in the folder <*SDK installation path*>\\WMFSDK11\\apps\\wmdmapp and choose the **Build/Build Solution** option.</span></span> <span data-ttu-id="a6f0f-115">Cela permet de créer deux fichiers projet : le projet d’assistance, proghelp. vcproj, ainsi que l’application principale wmdmapp. vcproj.</span><span class="sxs-lookup"><span data-stu-id="a6f0f-115">This will create two project files: the helper project, proghelp.vcproj, as well as the main application wmdmapp.vcproj.</span></span> <span data-ttu-id="a6f0f-116">En outre, il crée la DLL d’assistance de progression et l’application principale (WMDMApp.exe).</span><span class="sxs-lookup"><span data-stu-id="a6f0f-116">In addition, it will create the progress helper DLL and the main application (WMDMApp.exe).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6f0f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6f0f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6f0f-118">**Exemple d’application de bureau**</span><span class="sxs-lookup"><span data-stu-id="a6f0f-118">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




