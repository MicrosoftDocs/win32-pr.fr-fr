---
description: Cette section décrit les fonctions d’assistance que vous pouvez utiliser pour développer des analyses personnalisées.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Fonctions de surveillance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862854"
---
# <a name="monitor-functions"></a><span data-ttu-id="a73bc-103">Fonctions de surveillance</span><span class="sxs-lookup"><span data-stu-id="a73bc-103">Monitor Functions</span></span>

<span data-ttu-id="a73bc-104">Cette section décrit les fonctions d’assistance que vous pouvez utiliser pour développer des analyses personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a73bc-104">This section describes the helper functions you can use to develop custom monitors.</span></span>



| <span data-ttu-id="a73bc-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="a73bc-105">Function</span></span>                                       | <span data-ttu-id="a73bc-106">Description</span><span class="sxs-lookup"><span data-stu-id="a73bc-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a73bc-107">DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="a73bc-107">DllGetMonitorObject</span></span>](dllgetmonitorobject.md) | <span data-ttu-id="a73bc-108">Crée une instance de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a73bc-108">Creates an instance of the monitor.</span></span>                                                                                                                              |
| [<span data-ttu-id="a73bc-109">HTMLValueToUnicode</span><span class="sxs-lookup"><span data-stu-id="a73bc-109">HTMLValueToUnicode</span></span>](htmlvaluetounicode.md)   | <span data-ttu-id="a73bc-110">Convertit une \_ chaîne de version html FP UTF8 en Unicode.</span><span class="sxs-lookup"><span data-stu-id="a73bc-110">Converts an HTML CP\_UTF8 version string to Unicode.</span></span>                                                                                                             |
| [<span data-ttu-id="a73bc-111">LoadDWORD</span><span class="sxs-lookup"><span data-stu-id="a73bc-111">LoadDWORD</span></span>](loaddword.md)                     | <span data-ttu-id="a73bc-112">Charge un **DWORD** à partir d’une chaîne de configuration html.</span><span class="sxs-lookup"><span data-stu-id="a73bc-112">Loads a **DWORD** from an HTML configuration string.</span></span>                                                                                                             |
| [<span data-ttu-id="a73bc-113">LoadIPAddresses</span><span class="sxs-lookup"><span data-stu-id="a73bc-113">LoadIPAddresses</span></span>](loadipaddresses.md)         | <span data-ttu-id="a73bc-114">Charge une liste d’adresses IP à partir d’une chaîne de configuration TEXTAREA HTML.</span><span class="sxs-lookup"><span data-stu-id="a73bc-114">Loads an IP address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="a73bc-115">LoadIPXAddresses</span><span class="sxs-lookup"><span data-stu-id="a73bc-115">LoadIPXAddresses</span></span>](loadipxaddresses.md)       | <span data-ttu-id="a73bc-116">Charge une liste d’adresses IPX à partir d’une chaîne de configuration TEXTAREA HTML.</span><span class="sxs-lookup"><span data-stu-id="a73bc-116">Loads an IPX address list from an HTML TEXTAREA configuration string.</span></span>                                                                                            |
| [<span data-ttu-id="a73bc-117">LoadMACAddresses</span><span class="sxs-lookup"><span data-stu-id="a73bc-117">LoadMACAddresses</span></span>](loadmacaddresses.md)       | <span data-ttu-id="a73bc-118">Charge une liste d’adresses MAC à partir d’une chaîne de configuration TEXTAREA HTML.</span><span class="sxs-lookup"><span data-stu-id="a73bc-118">Loads a MAC address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="a73bc-119">LoadStringAddr</span><span class="sxs-lookup"><span data-stu-id="a73bc-119">LoadStringAddr</span></span>](loadstringaddr.md)           | <span data-ttu-id="a73bc-120">Transforme une chaîne (telle que « 157.54.32.45 ») en une adresse **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a73bc-120">Transforms a string (such as "157.54.32.45") to a **DWORD** address.</span></span>                                                                                             |
| [<span data-ttu-id="a73bc-121">LoadTCHAR</span><span class="sxs-lookup"><span data-stu-id="a73bc-121">LoadTCHAR</span></span>](loadtchar.md)                     | <span data-ttu-id="a73bc-122">Recherche un nom de variable demandé dans la chaîne de configuration et alloue suffisamment d’espace (à l’aide de **HeapAllocMemory**) pour le stocker, le copier et le retourner.</span><span class="sxs-lookup"><span data-stu-id="a73bc-122">Searches for a requested variable name in the configuration string, and allocates sufficient space (by using **HeapAllocMemory**) to store, copy, and return it.</span></span> |
| [<span data-ttu-id="a73bc-123">OnLoadingDLL</span><span class="sxs-lookup"><span data-stu-id="a73bc-123">OnLoadingDLL</span></span>](onloadingdll.md)               | <span data-ttu-id="a73bc-124">Indique que le chargement de la DLL a commencé.</span><span class="sxs-lookup"><span data-stu-id="a73bc-124">Indicates that the DLL has begun to load.</span></span> <span data-ttu-id="a73bc-125">Le MCSVC appelle cette fonction lors du premier chargement de la DLL du moniteur.</span><span class="sxs-lookup"><span data-stu-id="a73bc-125">The MCSVC calls this function when it first loads the monitor DLL.</span></span>                                                     |



 

 

 



