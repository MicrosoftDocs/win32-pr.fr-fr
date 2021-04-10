---
title: Installation d’applications sur des systèmes 64 bits
description: L’Windows Installer 64 bits peut installer en toute transparence des applications MSI 32 bits sur Windows 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- installation d’application 64 bits (programmation Windows)
- installation de la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101905"
---
# <a name="application-installation-on-64-bit-systems"></a><span data-ttu-id="e3d57-105">Installation d’applications sur des systèmes 64 bits</span><span class="sxs-lookup"><span data-stu-id="e3d57-105">Application Installation on 64-bit Systems</span></span>

<span data-ttu-id="e3d57-106">L' [Windows Installer 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) peut installer en toute transparence des applications MSI 32 bits sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e3d57-106">The [64-bit Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span> <span data-ttu-id="e3d57-107">Pour les applications plus anciennes qui utilisent un stub 16 bits pour lancer un moteur d’installation 32 bits, Windows 64 bits reconnaît des programmes d’installation 16 bits spécifiques et remplace une version de 32 bits par un port.</span><span class="sxs-lookup"><span data-stu-id="e3d57-107">For older applications that use a 16-bit stub to launch a 32-bit installation engine, 64-bit Windows recognizes specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span>

<span data-ttu-id="e3d57-108">les applications DOS, Windows ou OS/2 16 bits utilisent souvent un stub 16 bits pour vérifier le type de machine, puis lancent un moteur d’installation 32 bits pour effectuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="e3d57-108">16-bit DOS, Windows, or OS/2 applications often use a 16-bit stub to check the machine type, then launch a 32-bit installation engine to actually perform the installation.</span></span> <span data-ttu-id="e3d57-109">Pour permettre l’installation d’applications qui utilisent cette technique, Windows 64 bits remplace les versions 32 bits des programmes d’installation 16 bits suivants :</span><span class="sxs-lookup"><span data-stu-id="e3d57-109">To enable installation of applications that use this technique, 64-bit Windows substitutes 32-bit versions for the following 16-bit installer programs:</span></span>

* <span data-ttu-id="e3d57-110">Programme d’installation de Microsoft pour Windows 1,2</span><span class="sxs-lookup"><span data-stu-id="e3d57-110">Microsoft Setup for Windows 1.2</span></span>  
* <span data-ttu-id="e3d57-111">Programme d’installation de Microsoft pour Windows 2,6</span><span class="sxs-lookup"><span data-stu-id="e3d57-111">Microsoft Setup for Windows 2.6</span></span>  
* <span data-ttu-id="e3d57-112">Programme d’installation de Microsoft pour Windows 3,0</span><span class="sxs-lookup"><span data-stu-id="e3d57-112">Microsoft Setup for Windows 3.0</span></span>  
* <span data-ttu-id="e3d57-113">Programme d’installation de Microsoft pour Windows 3,01</span><span class="sxs-lookup"><span data-stu-id="e3d57-113">Microsoft Setup for Windows 3.01</span></span>  
* <span data-ttu-id="e3d57-114">InstallShield 5. x</span><span class="sxs-lookup"><span data-stu-id="e3d57-114">InstallShield 5.x</span></span>  

<span data-ttu-id="e3d57-115">La liste des substitutions est stockée dans le Registre sous la clé suivante : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.</span><span class="sxs-lookup"><span data-stu-id="e3d57-115">The list of substitutions is stored in the registry under the following key: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64**.</span></span>

> [!Note]  
> <span data-ttu-id="e3d57-116">Ce mécanisme est fourni uniquement pour la compatibilité avec les applications 32 bits qui utilisent les programmes Microsoft installer 16 bits indiqués dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e3d57-116">This mechanism is provided only for compatibility with 32-bit applications that use the 16-bit Microsoft installer programs listed in this topic.</span></span> <span data-ttu-id="e3d57-117">L’ajout de programmes d’installation tiers n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e3d57-117">Addition of third-party installer programs is not supported.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3d57-118">Ce mécanisme n’est pas inclus sur Windows 10 sur ARM.</span><span class="sxs-lookup"><span data-stu-id="e3d57-118">This mechanism is not included on Windows 10 on ARM.</span></span>

 

 

 