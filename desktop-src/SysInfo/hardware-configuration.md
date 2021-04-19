---
description: Les fonctions de configuration matérielle récupèrent des informations telles que le processeur, le profil matériel et les informations de clavier.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Hardware Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521167"
---
# <a name="hardware-configuration"></a><span data-ttu-id="c59c9-103">Hardware Configuration</span><span class="sxs-lookup"><span data-stu-id="c59c9-103">Hardware Configuration</span></span>

<span data-ttu-id="c59c9-104">Les fonctions de configuration matérielle récupèrent des informations telles que le processeur, le profil matériel et les informations de clavier.</span><span class="sxs-lookup"><span data-stu-id="c59c9-104">The hardware configuration functions retrieve information such as processor, hardware profile, and keyboard information.</span></span>

<span data-ttu-id="c59c9-105">La fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) récupère les informations sur le processeur et la mémoire, telles que la taille de la page, l’identificateur OEM (Original Equipment Manufacturer), le nombre et le type de processeurs, la plage d’adresses d’application, etc.</span><span class="sxs-lookup"><span data-stu-id="c59c9-105">The [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function retrieves processor and memory information, such as the page size, original equipment manufacturer (OEM) identifier, number and type of processors, application address range, and so on.</span></span> <span data-ttu-id="c59c9-106">La fonction [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) récupère des informations sur les opérations à virgule flottante et les jeux d’instructions pris en charge par le processeur.</span><span class="sxs-lookup"><span data-stu-id="c59c9-106">The [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) function retrieves information about the floating-point operations and instruction sets supported by the processor.</span></span>

<span data-ttu-id="c59c9-107">La fonction [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) récupère des informations sur le profil matériel.</span><span class="sxs-lookup"><span data-stu-id="c59c9-107">The [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) function retrieves information about the hardware profile.</span></span> <span data-ttu-id="c59c9-108">Le profil matériel comprend des informations telles que l’état d’ancrage, l’identificateur global unique (GUID) et le nom d’affichage du profil.</span><span class="sxs-lookup"><span data-stu-id="c59c9-108">The hardware profile includes information such as the docking state, globally unique identifier (GUID), and display name for the profile.</span></span> <span data-ttu-id="c59c9-109">La fonction [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) récupère des informations telles que le type de clavier et le nombre de touches de fonction sur le clavier actuel.</span><span class="sxs-lookup"><span data-stu-id="c59c9-109">The [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) function retrieves such information as the type of keyboard and the number of function keys on the current keyboard.</span></span>

 

 
