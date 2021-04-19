---
description: La procédure suivante décrit comment installer des assemblys côte à côte en tant qu’assemblys partagés.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installation d’assemblys côte à côte en tant qu’assemblys partagés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484641"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a><span data-ttu-id="f03ea-103">Installation d’assemblys côte à côte en tant qu’assemblys partagés</span><span class="sxs-lookup"><span data-stu-id="f03ea-103">Installing Side-by-side Assemblies as Shared Assemblies</span></span>

<span data-ttu-id="f03ea-104">La procédure suivante décrit comment installer des [assemblys côte à côte](about-side-by-side-assemblies-.md) en tant qu' [assemblys partagés](/windows/desktop/Msi/shared-assemblies).</span><span class="sxs-lookup"><span data-stu-id="f03ea-104">The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](/windows/desktop/Msi/shared-assemblies).</span></span>

<span data-ttu-id="f03ea-105">**Pour installer un assembly côte à côte en tant qu’assembly partagé**</span><span class="sxs-lookup"><span data-stu-id="f03ea-105">**To install a side-by-side assembly as a shared assembly**</span></span>

1.  <span data-ttu-id="f03ea-106">Signez et créez un catalogue pour les fichiers de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="f03ea-106">Sign and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="f03ea-107">Les fichiers doivent être signés pour être installés en tant qu’assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="f03ea-107">Files must be signed to install them as side-by-side assemblies.</span></span> <span data-ttu-id="f03ea-108">Pour plus d’informations, consultez [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="f03ea-108">For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

2.  <span data-ttu-id="f03ea-109">Vous devez installer des assemblys côte à côte partagés en tant que composants d’un package de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f03ea-109">You should install shared side-by-side assemblies as components of a Windows Installer package.</span></span> <span data-ttu-id="f03ea-110">Il peut s’agir du même package d’installation que celui utilisé pour installer ou mettre à jour votre application.</span><span class="sxs-lookup"><span data-stu-id="f03ea-110">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="f03ea-111">Si l’assembly partagé est fourni dans le cadre de plusieurs applications, vous devez fournir un module de fusion qui peut être incorporé dans les packages d’installation de ces applications et créer un catalogue pour les fichiers de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="f03ea-111">If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="f03ea-112">Windows Installer version 2,0 ou ultérieure est requis pour installer des assemblys.</span><span class="sxs-lookup"><span data-stu-id="f03ea-112">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="f03ea-113">Pour plus d’informations, consultez le kit de développement logiciel (SDK) [Windows Installer](../msi/windows-installer-portal.md) et les sections [installation des assemblys Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="f03ea-113">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

 

 
