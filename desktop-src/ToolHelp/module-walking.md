---
title: Parcours du module
description: Un instantané qui inclut la liste des modules pour un processus spécifié contient des informations sur chaque module, fichier exécutable ou bibliothèque de liens dynamiques (DLL), utilisé par le processus spécifié.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- bibliothèques de liens dynamiques
- bibliothèques de liens dynamiques, énumération de dll
- énumérer
- énumération, dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101753"
---
# <a name="module-walking"></a><span data-ttu-id="d3aae-107">Parcours du module</span><span class="sxs-lookup"><span data-stu-id="d3aae-107">Module Walking</span></span>

<span data-ttu-id="d3aae-108">Un instantané qui inclut la liste des modules pour un processus spécifié contient des informations sur chaque module, fichier exécutable ou bibliothèque de liens dynamiques (DLL), utilisé par le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="d3aae-108">A snapshot that includes the module list for a specified process contains information about each module, executable file, or dynamic-link library (DLL), used by the specified process.</span></span> <span data-ttu-id="d3aae-109">Vous pouvez récupérer des informations pour le premier module de la liste à l’aide de la fonction [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) .</span><span class="sxs-lookup"><span data-stu-id="d3aae-109">You can retrieve information for the first module in the list by using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) function.</span></span> <span data-ttu-id="d3aae-110">Après avoir récupéré le premier module de la liste, vous pouvez récupérer des informations pour les modules suivants dans la liste à l’aide de la fonction [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) .</span><span class="sxs-lookup"><span data-stu-id="d3aae-110">After retrieving the first module in the list, you can retrieve information for subsequent modules in the list by using the [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) function.</span></span> <span data-ttu-id="d3aae-111">**Module32First** et **Module32Next** remplissent une structure [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) avec des informations sur le module.</span><span class="sxs-lookup"><span data-stu-id="d3aae-111">**Module32First** and **Module32Next** fill a [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) structure with information about the module.</span></span>

<span data-ttu-id="d3aae-112">Vous pouvez récupérer un code d’état d’erreur étendu pour [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) et [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="d3aae-112">You can retrieve an extended error status code for [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="d3aae-113">L’identificateur de module, qui est spécifié dans le membre **th32ModuleID** de [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), n’a qu’une signification dans Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d3aae-113">The module identifier, which is specified in the **th32ModuleID** member of [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), only has meaning in 16-bit Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d3aae-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3aae-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3aae-115">Parcours de la liste des modules</span><span class="sxs-lookup"><span data-stu-id="d3aae-115">Traversing the Module List</span></span>](traversing-the-module-list.md)
</dt> </dl>

 

 