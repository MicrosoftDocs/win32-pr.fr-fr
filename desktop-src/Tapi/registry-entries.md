---
description: Les terminaux enfichables sont classés en superclasses de terminaux.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entrées de Registre (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531425"
---
# <a name="registry-entries-telephony-api"></a><span data-ttu-id="bc0a1-103">Entrées de Registre (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="bc0a1-103">Registry Entries (Telephony API)</span></span>

<span data-ttu-id="bc0a1-104">Les terminaux enfichables sont classés en superclasses de terminaux.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-104">The pluggable terminals are classified into Terminal Superclasses.</span></span> <span data-ttu-id="bc0a1-105">Chaque superclasse de terminal a une entrée dans le Registre sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="bc0a1-105">Each Terminal Superclass has an entry in the registry under the following key:</span></span>

<span data-ttu-id="bc0a1-106">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telephony** \\ **TerminalManager**</span><span class="sxs-lookup"><span data-stu-id="bc0a1-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Telephony**\\**TerminalManager**</span></span>

<span data-ttu-id="bc0a1-107">Sous la clé de superclasse terminal sont des entrées pour chaque terminal enfichable au sein de la superclasse terminal.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-107">Below the Terminal Superclass key are entries for each pluggable terminal within the Terminal Superclass.</span></span>

<span data-ttu-id="bc0a1-108">L’entrée de chaque superclasse de terminal est identifiée par un CLSID de superclasse terminal.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-108">The entry for each Terminal Superclass is identified by a Terminal Superclass CLSID.</span></span> <span data-ttu-id="bc0a1-109">Il s’agit d’un identificateur unique pour une classe de terminal.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-109">This is a unique identifier for a terminal class.</span></span> <span data-ttu-id="bc0a1-110">La classe terminal possède un attribut facultatif : Name, qui est un nom convivial pour la classe terminal.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-110">The terminal class has an optional attribute: name, which is a friendly name for the terminal class.</span></span> <span data-ttu-id="bc0a1-111">Chaque terminal enfichable est identifié par une classe de terminal CLSID ; autrement dit, un GUID.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-111">Each pluggable terminal is identified by a CLSID Terminal class; that is, a GUID.</span></span> <span data-ttu-id="bc0a1-112">Les attributs du terminal enfichable sont stockés dans des valeurs de clés de terminal enfichables.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-112">The attributes for pluggable terminal are stored into pluggable terminal key values.</span></span> <span data-ttu-id="bc0a1-113">Les attributs d’un terminal enfichable sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-113">The attributes for a pluggable terminal are the following.</span></span>



| <span data-ttu-id="bc0a1-114">Classe de terminal</span><span class="sxs-lookup"><span data-stu-id="bc0a1-114">Terminal class</span></span> | <span data-ttu-id="bc0a1-115">Nom de clé</span><span class="sxs-lookup"><span data-stu-id="bc0a1-115">Key name</span></span> | <span data-ttu-id="bc0a1-116">Identificateur public</span><span class="sxs-lookup"><span data-stu-id="bc0a1-116">Public identifier</span></span>                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bc0a1-117">Nom</span><span class="sxs-lookup"><span data-stu-id="bc0a1-117">Name</span></span>           | <span data-ttu-id="bc0a1-118">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="bc0a1-118">REG\_SZ</span></span>  | <span data-ttu-id="bc0a1-119">Nom convivial du terminal</span><span class="sxs-lookup"><span data-stu-id="bc0a1-119">Terminal friendly name</span></span>                                                            |
| <span data-ttu-id="bc0a1-120">Company</span><span class="sxs-lookup"><span data-stu-id="bc0a1-120">Company</span></span>        | <span data-ttu-id="bc0a1-121">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="bc0a1-121">REG\_SZ</span></span>  | <span data-ttu-id="bc0a1-122">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="bc0a1-122">Company name</span></span>                                                                      |
| <span data-ttu-id="bc0a1-123">Version</span><span class="sxs-lookup"><span data-stu-id="bc0a1-123">Version</span></span>        | <span data-ttu-id="bc0a1-124">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="bc0a1-124">REG\_SZ</span></span>  | <span data-ttu-id="bc0a1-125">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="bc0a1-125">Version information</span></span>                                                               |
| <span data-ttu-id="bc0a1-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc0a1-126">CLSID</span></span>          | <span data-ttu-id="bc0a1-127">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="bc0a1-127">REG\_SZ</span></span>  | <span data-ttu-id="bc0a1-128">CLSID de terminal (utilisé dans la méthode [**COCREATEINSTANCE**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com)</span><span class="sxs-lookup"><span data-stu-id="bc0a1-128">Terminal CLSID (used in COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method)</span></span> |
| <span data-ttu-id="bc0a1-129">Directions</span><span class="sxs-lookup"><span data-stu-id="bc0a1-129">Directions</span></span>     | <span data-ttu-id="bc0a1-130">DWORD</span><span class="sxs-lookup"><span data-stu-id="bc0a1-130">DWORD</span></span>    | <span data-ttu-id="bc0a1-131">Direction du terminal</span><span class="sxs-lookup"><span data-stu-id="bc0a1-131">Terminal direction</span></span>                                                                |
| <span data-ttu-id="bc0a1-132">MediaTypes</span><span class="sxs-lookup"><span data-stu-id="bc0a1-132">MediaTypes</span></span>     | <span data-ttu-id="bc0a1-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="bc0a1-133">DWORD</span></span>    | <span data-ttu-id="bc0a1-134">Types de média terminal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc0a1-134">Terminal media types supported</span></span>                                                    |



 

<span data-ttu-id="bc0a1-135">Pour une classe de terminal, les attributs sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-135">For a terminal class the attributes are the following.</span></span>



| <span data-ttu-id="bc0a1-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc0a1-136">CLSID</span></span> | <span data-ttu-id="bc0a1-137">Nom de clé</span><span class="sxs-lookup"><span data-stu-id="bc0a1-137">Key name</span></span> | <span data-ttu-id="bc0a1-138">Identificateur public</span><span class="sxs-lookup"><span data-stu-id="bc0a1-138">Public identifier</span></span>            |
|-------|----------|------------------------------|
| <span data-ttu-id="bc0a1-139">Nom</span><span class="sxs-lookup"><span data-stu-id="bc0a1-139">Name</span></span>  | <span data-ttu-id="bc0a1-140">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="bc0a1-140">REG\_SZ</span></span>  | <span data-ttu-id="bc0a1-141">Nom convivial de la classe terminal</span><span class="sxs-lookup"><span data-stu-id="bc0a1-141">Terminal class friendly name</span></span> |



 

 

 
