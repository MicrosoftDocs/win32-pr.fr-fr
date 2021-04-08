---
title: /target, commutateur
description: Le commutateur/target permet au compilateur MIDL d’activer des optimisations disponibles uniquement sur les versions récentes de Windows. Le commutateur/target active automatiquement les commutateurs supplémentaires.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- MIDL du commutateur/target
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104042900"
---
# <a name="target-switch"></a><span data-ttu-id="856eb-105">/target, commutateur</span><span class="sxs-lookup"><span data-stu-id="856eb-105">/target switch</span></span>

<span data-ttu-id="856eb-106">Le commutateur **/target** permet au compilateur MIDL d’activer des optimisations disponibles uniquement sur les versions récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="856eb-106">The **/target** switch enables the MIDL compiler to enable optimizations available only on recent versions of Windows.</span></span> <span data-ttu-id="856eb-107">Le commutateur **/target** active automatiquement les commutateurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="856eb-107">The **/target** switch automatically activates additional switches.</span></span>

``` syntax
midl /target level
```

## <a name="switch-options"></a><span data-ttu-id="856eb-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="856eb-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="856eb-109">*level*</span><span class="sxs-lookup"><span data-stu-id="856eb-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="856eb-110">Spécifie le niveau cible, tel que NT50, NT51, NT60, NT61, NT62 ou NT100.</span><span class="sxs-lookup"><span data-stu-id="856eb-110">Specifies the target level, such as NT50, NT51, NT60, NT61, NT62, or NT100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="856eb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="856eb-111">Remarks</span></span>

<span data-ttu-id="856eb-112">Le commutateur **/target** active automatiquement les commutateurs supplémentaires, selon le système d’exploitation, comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="856eb-112">The **/target** switch automatically activates additional switches, based on the operating system, as specified in the following table:</span></span>



| <span data-ttu-id="856eb-113">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="856eb-113">Operating system</span></span> | <span data-ttu-id="856eb-114">niveau/target</span><span class="sxs-lookup"><span data-stu-id="856eb-114">/target level</span></span> | <span data-ttu-id="856eb-115">Commutateurs activés</span><span class="sxs-lookup"><span data-stu-id="856eb-115">Switches Activated</span></span>                     |
|------------------|---------------|----------------------------------------|
| <span data-ttu-id="856eb-116">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="856eb-116">Windows 2000</span></span>     | <span data-ttu-id="856eb-117">NT50</span><span class="sxs-lookup"><span data-stu-id="856eb-117">NT50</span></span>          | <span data-ttu-id="856eb-118">/Oicf/Error tout/Robust</span><span class="sxs-lookup"><span data-stu-id="856eb-118">/Oicf /error all /robust</span></span>               |
| <span data-ttu-id="856eb-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="856eb-119">Windows XP</span></span>       | <span data-ttu-id="856eb-120">NT51</span><span class="sxs-lookup"><span data-stu-id="856eb-120">NT51</span></span>          | <span data-ttu-id="856eb-121">/Oicf/Error All/Protocol All</span><span class="sxs-lookup"><span data-stu-id="856eb-121">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="856eb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="856eb-122">Windows Vista</span></span>    | <span data-ttu-id="856eb-123">NT60</span><span class="sxs-lookup"><span data-stu-id="856eb-123">NT60</span></span>          | <span data-ttu-id="856eb-124">/Oicf/Error All/Protocol All</span><span class="sxs-lookup"><span data-stu-id="856eb-124">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="856eb-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="856eb-125">Windows 7</span></span>        | <span data-ttu-id="856eb-126">NT61</span><span class="sxs-lookup"><span data-stu-id="856eb-126">NT61</span></span>          | <span data-ttu-id="856eb-127">/Oicf/Error All/Protocol All</span><span class="sxs-lookup"><span data-stu-id="856eb-127">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="856eb-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="856eb-128">Windows 8</span></span>        | <span data-ttu-id="856eb-129">NT62</span><span class="sxs-lookup"><span data-stu-id="856eb-129">NT62</span></span>          | <span data-ttu-id="856eb-130">/Oicf/Error All/Protocol All</span><span class="sxs-lookup"><span data-stu-id="856eb-130">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="856eb-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="856eb-131">Windows 10</span></span>       | <span data-ttu-id="856eb-132">NT100</span><span class="sxs-lookup"><span data-stu-id="856eb-132">NT100</span></span>         | <span data-ttu-id="856eb-133">/Oicf/Error All/Protocol All</span><span class="sxs-lookup"><span data-stu-id="856eb-133">/Oicf /error all /robust /protocol all</span></span> |
 

<span data-ttu-id="856eb-134">Pour s’assurer qu’un stub s’exécute sur le système spécifié par le commutateur **/target** , MIDL émet une erreur quand une fonctionnalité disponible uniquement sur une version plus récente de Windows est présente.</span><span class="sxs-lookup"><span data-stu-id="856eb-134">To ensure a stub runs on the system specified by the **/target** switch, MIDL issues an error when a feature available only on a more recent version of Windows is present.</span></span> <span data-ttu-id="856eb-135">Le tableau suivant spécifie le niveau minimal de **/target** requis pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="856eb-135">The following table specifies the minimum **/target** level required to enable the feature.</span></span> <span data-ttu-id="856eb-136">Les niveaux cibles plus élevés incluent toutes les fonctionnalités des niveaux cibles inférieurs.</span><span class="sxs-lookup"><span data-stu-id="856eb-136">Higher target levels include all features from lower target levels.</span></span>



| <span data-ttu-id="856eb-137">Niveau/Target minimal requis</span><span class="sxs-lookup"><span data-stu-id="856eb-137">Minimum required /target level</span></span> | <span data-ttu-id="856eb-138">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="856eb-138">Features</span></span>                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="856eb-139">NT50</span><span class="sxs-lookup"><span data-stu-id="856eb-139">NT50</span></span>                           | <span data-ttu-id="856eb-140">/Robust</span><span class="sxs-lookup"><span data-stu-id="856eb-140">/robust</span></span><br/> <span data-ttu-id="856eb-141">\[message\]</span><span class="sxs-lookup"><span data-stu-id="856eb-141">\[message\]</span></span><br/> <span data-ttu-id="856eb-142">\[async\]</span><span class="sxs-lookup"><span data-stu-id="856eb-142">\[async\]</span></span><br/> <span data-ttu-id="856eb-143">\[\_UUID asynchrone\]</span><span class="sxs-lookup"><span data-stu-id="856eb-143">\[async\_uuid\]</span></span><br/> <span data-ttu-id="856eb-144">\[notifier \] en mode/Oicf</span><span class="sxs-lookup"><span data-stu-id="856eb-144">\[notify\] in /Oicf mode</span></span><br/> <span data-ttu-id="856eb-145">\[encoder \] ou \[ décoder \] en mode/Oicf</span><span class="sxs-lookup"><span data-stu-id="856eb-145">\[encode\] or \[decode\] in /Oicf mode</span></span><br/>                   |
| <span data-ttu-id="856eb-146">NT51</span><span class="sxs-lookup"><span data-stu-id="856eb-146">NT51</span></span>                           | <span data-ttu-id="856eb-147">prise en charge de/Protocol 64 bits</span><span class="sxs-lookup"><span data-stu-id="856eb-147">/protocol 64-bit support</span></span><br/> <span data-ttu-id="856eb-148">\[\_Ignorer partiellement\]</span><span class="sxs-lookup"><span data-stu-id="856eb-148">\[partial\_ignore\]</span></span><br/> <span data-ttu-id="856eb-149">\[forcer l' \_ allocation\]</span><span class="sxs-lookup"><span data-stu-id="856eb-149">\[force\_allocate\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="856eb-150">NT60</span><span class="sxs-lookup"><span data-stu-id="856eb-150">NT60</span></span>                           | <span data-ttu-id="856eb-151">Marshaling de structure complexe forcé</span><span class="sxs-lookup"><span data-stu-id="856eb-151">Forced complex structure marshalling</span></span><br/> <span data-ttu-id="856eb-152">Handles de contexte dans un tableau ou une structure</span><span class="sxs-lookup"><span data-stu-id="856eb-152">Context handles in an array or structure</span></span><br/> <span data-ttu-id="856eb-153">\[\]prise en charge des chaînes non dimensionnées par plage</span><span class="sxs-lookup"><span data-stu-id="856eb-153">\[range\] support for unsized strings</span></span><br/> <span data-ttu-id="856eb-154">\[\_handle de \_ contexte \_ strict de type\]</span><span class="sxs-lookup"><span data-stu-id="856eb-154">\[type\_strict\_context\_handle\]</span></span><br/> |
| <span data-ttu-id="856eb-155">NT61</span><span class="sxs-lookup"><span data-stu-id="856eb-155">NT61</span></span>                           | <span data-ttu-id="856eb-156">Les appels directs du stub COM pour les interfaces avec moins de 32 méthodes requièrent la liaison des stubs COM avec **OLE32.DLL**.</span><span class="sxs-lookup"><span data-stu-id="856eb-156">Direct COM stub calls for interfaces with less than 32 methods requires linking COM stubs with **OLE32.DLL**.</span></span><br/>                                                                          |
| <span data-ttu-id="856eb-157">NT62</span><span class="sxs-lookup"><span data-stu-id="856eb-157">NT62</span></span>                           | <span data-ttu-id="856eb-158">Support ARM</span><span class="sxs-lookup"><span data-stu-id="856eb-158">ARM support</span></span><br/> <span data-ttu-id="856eb-159">Prise en charge de WinRT</span><span class="sxs-lookup"><span data-stu-id="856eb-159">WinRT support</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="856eb-160">NT100</span><span class="sxs-lookup"><span data-stu-id="856eb-160">NT100</span></span>                          | <span data-ttu-id="856eb-161">\[\]support system_handle</span><span class="sxs-lookup"><span data-stu-id="856eb-161">\[system_handle\] support</span></span><br /> |


 

## <a name="examples"></a><span data-ttu-id="856eb-162">Exemples</span><span class="sxs-lookup"><span data-stu-id="856eb-162">Examples</span></span>

<span data-ttu-id="856eb-163">**MIDL/Target NT50**</span><span class="sxs-lookup"><span data-stu-id="856eb-163">**midl /target NT50**</span></span>

## <a name="see-also"></a><span data-ttu-id="856eb-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="856eb-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856eb-165">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="856eb-165">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="856eb-166">**/osf**</span><span class="sxs-lookup"><span data-stu-id="856eb-166">**/osf**</span></span>](-osf.md)
</dt> </dl>
