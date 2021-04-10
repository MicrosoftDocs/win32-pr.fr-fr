---
description: Windows Installer s’exécute en tant que service sur les ordinateurs utilisant Windows 32 bits ou 64 bits.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: À propos des Windows Installer sur les systèmes d’exploitation 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "104211113"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a><span data-ttu-id="3efff-103">À propos des Windows Installer sur les systèmes d’exploitation 64 bits</span><span class="sxs-lookup"><span data-stu-id="3efff-103">About Windows Installer on 64-Bit Operating Systems</span></span>

<span data-ttu-id="3efff-104">Windows Installer s’exécute en tant que service sur les ordinateurs utilisant Windows 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-104">Windows Installer runs as a service on computers using 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="3efff-105">Les versions du programme d’installation antérieures à la version 2,0 peuvent installer et gérer des packages Windows Installer 32 bits uniquement sur les systèmes d’exploitation 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-105">Versions of the installer earlier than version 2.0 can install and manage 32-bit Windows Installer Packages only on 32-bit operating systems.</span></span> <span data-ttu-id="3efff-106">Notez que vous ne pouvez pas publier ou installer une application 64 bits sur un système d’exploitation 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-106">Note that you cannot advertise or install a 64-bit application on a 32-bit operating system.</span></span>

<span data-ttu-id="3efff-107">Un package de Windows Installer doit être spécifié en tant que package 32 bits ou 64 bits ; elle ne peut pas être spécifiée comme neutre.</span><span class="sxs-lookup"><span data-stu-id="3efff-107">A Windows Installer package must be specified as either a 32-bit or a 64-bit package; it cannot be specified as neutral.</span></span> <span data-ttu-id="3efff-108">Sur un ordinateur qui utilise un système d’exploitation 64 bits, le service Windows Installer est hébergé dans un processus 64 bits qui installe les packages 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-108">On a computer using a 64-bit operating system, the Windows Installer service is hosted in a 64-bit process that installs both 32-bit and 64-bit packages.</span></span> <span data-ttu-id="3efff-109">Windows Installer installe trois types de packages Windows Installer sur un ordinateur exécutant un système d’exploitation 64 bits :</span><span class="sxs-lookup"><span data-stu-id="3efff-109">Windows Installer installs three types of Windows installer packages on a computer running a 64-bit operating system:</span></span>

-   <span data-ttu-id="3efff-110">Packages 32 bits qui contiennent uniquement des composants 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-110">32-bit packages that contain only 32-bit components.</span></span>
-   <span data-ttu-id="3efff-111">Packages 64 bits contenant des composants 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-111">64-bit packages containing some 32-bit components.</span></span>
-   <span data-ttu-id="3efff-112">Packages 64 bits contenant uniquement des composants de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-112">64-bit packages containing only 64-bit components.</span></span>

<span data-ttu-id="3efff-113">Les sections suivantes décrivent les deux types de Windows Installer packages et les nouvelles propriétés de programme d’installation fournies par Windows Installer pour les packages 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3efff-113">The follow sections describe the two types of Windows Installer packages and the new installer properties provided by Windows Installer for 64-bit packages.</span></span>

[<span data-ttu-id="3efff-114">Packages de Windows Installer 32 bits</span><span class="sxs-lookup"><span data-stu-id="3efff-114">32-bit Windows Installer Packages</span></span>](32-bit-windows-installer-packages.md)

[<span data-ttu-id="3efff-115">Packages de Windows Installer 64 bits</span><span class="sxs-lookup"><span data-stu-id="3efff-115">64-bit Windows Installer Packages</span></span>](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a><span data-ttu-id="3efff-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3efff-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3efff-117">Utilisation de packages Windows Installers 64 bits</span><span class="sxs-lookup"><span data-stu-id="3efff-117">Using 64-Bit Windows Installer Packages</span></span>](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



