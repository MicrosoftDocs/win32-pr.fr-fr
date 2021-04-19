---
description: Pour installer des assemblys côte à côte en tant qu’assemblys privés, vous pouvez installer l’assembly en tant que composant d’un package d’installation.
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: Installation d’assemblys côte à côte en tant qu’assemblys privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516638"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a><span data-ttu-id="db67a-103">Installation d’assemblys côte à côte en tant qu’assemblys privés</span><span class="sxs-lookup"><span data-stu-id="db67a-103">Installing Side-by-side Assemblies as Private Assemblies</span></span>

<span data-ttu-id="db67a-104">Pour installer des [assemblys côte à côte](about-side-by-side-assemblies-.md) en tant qu' [assemblys privés](/windows/desktop/Msi/private-assemblies), vous pouvez installer l’assembly en tant que composant d’un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="db67a-104">To install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [private assemblies](/windows/desktop/Msi/private-assemblies), you can install the assembly as a component of an installer package.</span></span> <span data-ttu-id="db67a-105">Il peut s’agir du même package d’installation que celui utilisé pour installer ou mettre à jour votre application.</span><span class="sxs-lookup"><span data-stu-id="db67a-105">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="db67a-106">Windows Installer version 2,0 ou ultérieure est requis pour installer des assemblys.</span><span class="sxs-lookup"><span data-stu-id="db67a-106">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="db67a-107">Pour plus d’informations, consultez le kit de développement logiciel (SDK) [Windows Installer](../msi/windows-installer-portal.md) et les sections [installation des assemblys Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="db67a-107">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="db67a-108">Vous pouvez également utiliser le programme d’installation pour copier un assembly privé et un manifeste dans le même dossier que le fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="db67a-108">As an alternative, you can use the installer to copy a private assembly and manifest into the same folder as the application's executable file.</span></span>

 

 
