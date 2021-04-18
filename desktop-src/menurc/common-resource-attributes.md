---
title: Attributs de ressources communes
description: Les instructions de définition de ressources prises en charge sur Windows 16 bits incluent une option de chargement qui spécifie les caractéristiques de chargement et de mémoire de la ressource.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512452"
---
# <a name="common-resource-attributes"></a><span data-ttu-id="67c0c-103">Attributs de ressources communes</span><span class="sxs-lookup"><span data-stu-id="67c0c-103">Common Resource Attributes</span></span>

<span data-ttu-id="67c0c-104">Les instructions de définition de ressources prises en charge sur Windows 16 bits incluent une option de *chargement* qui spécifie les caractéristiques de chargement et de mémoire de la ressource.</span><span class="sxs-lookup"><span data-stu-id="67c0c-104">The resource-definition statements supported on 16-bit Windows include a *load-mem* option that specifies the loading and memory characteristics of the resource.</span></span> <span data-ttu-id="67c0c-105">Ces attributs sont autorisés dans les scripts de ressources à des fins de compatibilité descendante, mais ils sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="67c0c-105">These attributes are permitted in resource scripts for backward compatibility, but they are ignored.</span></span> <span data-ttu-id="67c0c-106">Les ressources Windows sont chargées lorsque le module correspondant est chargé, et sont libérées quand le module est déchargé.</span><span class="sxs-lookup"><span data-stu-id="67c0c-106">Windows resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

## <a name="load-attributes"></a><span data-ttu-id="67c0c-107">Charger les attributs</span><span class="sxs-lookup"><span data-stu-id="67c0c-107">Load Attributes</span></span>

<span data-ttu-id="67c0c-108">Les attributs de chargement spécifient le moment où la ressource doit être chargée.</span><span class="sxs-lookup"><span data-stu-id="67c0c-108">The load attributes specify when the resource is to be loaded.</span></span> <span data-ttu-id="67c0c-109">Le paramètre de charge doit être l’un des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="67c0c-109">The load parameter must be one of the following attributes.</span></span>



| <span data-ttu-id="67c0c-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="67c0c-110">Attribute</span></span>      | <span data-ttu-id="67c0c-111">Description</span><span class="sxs-lookup"><span data-stu-id="67c0c-111">Description</span></span>                                                                  |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="67c0c-112">**PRÉ**</span><span class="sxs-lookup"><span data-stu-id="67c0c-112">**PRELOAD**</span></span>    | <span data-ttu-id="67c0c-113">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-113">Ignored.</span></span> <span data-ttu-id="67c0c-114">Dans Windows 16 bits, la ressource est chargée avec le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="67c0c-114">In 16-bit Windows, the resource is loaded with the executable file.</span></span> |
| <span data-ttu-id="67c0c-115">**LOADONCALL**</span><span class="sxs-lookup"><span data-stu-id="67c0c-115">**LOADONCALL**</span></span> | <span data-ttu-id="67c0c-116">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-116">Ignored.</span></span> <span data-ttu-id="67c0c-117">Dans Windows 16 bits, la ressource est chargée quand elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="67c0c-117">In 16-bit Windows, the resource is loaded when called.</span></span>              |



 

## <a name="memory-attributes"></a><span data-ttu-id="67c0c-118">Attributs de mémoire</span><span class="sxs-lookup"><span data-stu-id="67c0c-118">Memory Attributes</span></span>

<span data-ttu-id="67c0c-119">Les attributs de mémoire spécifient si la ressource est fixe ou mobile, si elle peut être supprimée et si elle est pure.</span><span class="sxs-lookup"><span data-stu-id="67c0c-119">The memory attributes specify whether the resource is fixed or movable, whether it is discardable, and whether it is pure.</span></span> <span data-ttu-id="67c0c-120">Le paramètre de mémoire peut être un ou plusieurs des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="67c0c-120">The memory parameter can be one or more of the following attributes.</span></span>



| <span data-ttu-id="67c0c-121">Attribut</span><span class="sxs-lookup"><span data-stu-id="67c0c-121">Attribute</span></span>       | <span data-ttu-id="67c0c-122">Description</span><span class="sxs-lookup"><span data-stu-id="67c0c-122">Description</span></span>                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c0c-123">**FIXED**</span><span class="sxs-lookup"><span data-stu-id="67c0c-123">**FIXED**</span></span>       | <span data-ttu-id="67c0c-124">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-124">Ignored.</span></span> <span data-ttu-id="67c0c-125">Dans Windows 16 bits, la ressource reste à un emplacement de mémoire fixe.</span><span class="sxs-lookup"><span data-stu-id="67c0c-125">In 16-bit Windows, the resource remains at a fixed memory location.</span></span>                                                              |
| <span data-ttu-id="67c0c-126">**PLACÉ**</span><span class="sxs-lookup"><span data-stu-id="67c0c-126">**MOVEABLE**</span></span>    | <span data-ttu-id="67c0c-127">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-127">Ignored.</span></span> <span data-ttu-id="67c0c-128">Dans Windows 16 bits, la ressource peut être déplacée si nécessaire pour compacter la mémoire.</span><span class="sxs-lookup"><span data-stu-id="67c0c-128">In 16-bit Windows, the resource can be moved if necessary to compact memory.</span></span>                                                     |
| <span data-ttu-id="67c0c-129">**POUVANT être éliminée**</span><span class="sxs-lookup"><span data-stu-id="67c0c-129">**DISCARDABLE**</span></span> | <span data-ttu-id="67c0c-130">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-130">Ignored.</span></span> <span data-ttu-id="67c0c-131">Dans Windows 16 bits, la ressource peut être ignorée si vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="67c0c-131">In 16-bit Windows, the resource can be discarded if no longer needed.</span></span>                                                            |
| <span data-ttu-id="67c0c-132">**FCP**</span><span class="sxs-lookup"><span data-stu-id="67c0c-132">**PURE**</span></span>        | <span data-ttu-id="67c0c-133">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-133">Ignored.</span></span> <span data-ttu-id="67c0c-134">Accepté pour la compatibilité avec les scripts de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="67c0c-134">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="67c0c-135">**IMPURES**</span><span class="sxs-lookup"><span data-stu-id="67c0c-135">**IMPURE**</span></span>      | <span data-ttu-id="67c0c-136">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-136">Ignored.</span></span> <span data-ttu-id="67c0c-137">Accepté pour la compatibilité avec les scripts de ressources existants.</span><span class="sxs-lookup"><span data-stu-id="67c0c-137">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="67c0c-138">**PARTAGÉ**</span><span class="sxs-lookup"><span data-stu-id="67c0c-138">**SHARED**</span></span>      | <span data-ttu-id="67c0c-139">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-139">Ignored.</span></span> <span data-ttu-id="67c0c-140">Dans Windows 16 bits, SHAREd est ignoré pour les modules normaux.</span><span class="sxs-lookup"><span data-stu-id="67c0c-140">In 16-bit Windows, SHARED is ignored for regular modules.</span></span> <span data-ttu-id="67c0c-141">Pour une ressource d’un module ROM Windows, la mémoire est partagée.</span><span class="sxs-lookup"><span data-stu-id="67c0c-141">For a resource from a ROM Windows module, the memory is shared.</span></span>        |
| <span data-ttu-id="67c0c-142">**NON partagée**</span><span class="sxs-lookup"><span data-stu-id="67c0c-142">**NONSHARED**</span></span>   | <span data-ttu-id="67c0c-143">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="67c0c-143">Ignored.</span></span> <span data-ttu-id="67c0c-144">Dans Windows 16 bits, non partagé est ignoré pour les modules normaux.</span><span class="sxs-lookup"><span data-stu-id="67c0c-144">In 16-bit Windows, NONSHARED is ignored for regular modules.</span></span> <span data-ttu-id="67c0c-145">Pour une ressource d’un module ROM Windows, la mémoire n’est pas partagée.</span><span class="sxs-lookup"><span data-stu-id="67c0c-145">For a resource from a ROM Windows module, the memory is not shared.</span></span> |



 

 

 




