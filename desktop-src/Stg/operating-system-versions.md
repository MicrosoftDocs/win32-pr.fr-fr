---
title: Versions de système d’exploitation
description: Ce type de données DWORD doit contenir le type de système d’exploitation dans le mot de poids fort et le numéro de version du système d’exploitation dans le mot de poids faible. Les valeurs possibles pour le système d’exploitation sont répertoriées dans le tableau suivant.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Versions de système d’exploitation stockage structuré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509662"
---
# <a name="operating-system-versions"></a><span data-ttu-id="b2ef0-105">Versions de système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b2ef0-105">Operating System Versions</span></span>

<span data-ttu-id="b2ef0-106">Ce type de données **DWORD** doit contenir le type de système d’exploitation dans le mot de poids fort et le numéro de version du système d’exploitation dans le mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-106">This **DWORD** data type should hold the operating system type in the high-order word and the version number of the operating system in the low-order word.</span></span> <span data-ttu-id="b2ef0-107">Les valeurs possibles pour le système d’exploitation sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-107">Possible values for the operating system are listed in the following table.</span></span>



| <span data-ttu-id="b2ef0-108">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b2ef0-108">Operating system</span></span>       | <span data-ttu-id="b2ef0-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2ef0-109">Value</span></span>  |
|------------------------|--------|
| <span data-ttu-id="b2ef0-110">32 bits Windows (Win32)</span><span class="sxs-lookup"><span data-stu-id="b2ef0-110">32-Bit Windows (Win32)</span></span> | <span data-ttu-id="b2ef0-111">0x0002</span><span class="sxs-lookup"><span data-stu-id="b2ef0-111">0x0002</span></span> |
| <span data-ttu-id="b2ef0-112">Macintosh</span><span class="sxs-lookup"><span data-stu-id="b2ef0-112">Macintosh</span></span>              | <span data-ttu-id="b2ef0-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="b2ef0-113">0x0001</span></span> |
| <span data-ttu-id="b2ef0-114">Windows 16 bits (Win16)</span><span class="sxs-lookup"><span data-stu-id="b2ef0-114">16-Bit Windows (Win16)</span></span> | <span data-ttu-id="b2ef0-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="b2ef0-115">0x0000</span></span> |



 

<span data-ttu-id="b2ef0-116">Pour les systèmes d’exploitation Microsoft Windows, la version du système d’exploitation est le mot de poids faible retourné par la fonction [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) .</span><span class="sxs-lookup"><span data-stu-id="b2ef0-116">For Microsoft Windows operating systems, the operating system version is the low-order word returned by the [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) function.</span></span> <span data-ttu-id="b2ef0-117">Pour Microsoft Windows, l’exemple de code suivant définit correctement la version du système d’exploitation d’origine.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-117">For Microsoft Windows, the following example code correctly sets the version of the originating operating system.</span></span>

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 