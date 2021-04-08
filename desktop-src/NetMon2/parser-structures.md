---
description: Cette section décrit les structures que vous pouvez utiliser pour développer des analyseurs. Ces structures sont utilisées par les fonctions que vous pouvez utiliser pour développer des analyseurs et des fonctions que vous pouvez utiliser pour développer des analyseurs ou des experts.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Structures de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953249"
---
# <a name="parser-structures"></a><span data-ttu-id="aad53-104">Structures de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="aad53-104">Parser Structures</span></span>

<span data-ttu-id="aad53-105">Cette section décrit les structures que vous pouvez utiliser pour développer des analyseurs.</span><span class="sxs-lookup"><span data-stu-id="aad53-105">This section describes structures you can use to develop parsers.</span></span> <span data-ttu-id="aad53-106">Ces structures sont utilisées par les fonctions que vous pouvez utiliser pour développer des analyseurs et des fonctions que vous pouvez utiliser pour développer des analyseurs ou des experts.</span><span class="sxs-lookup"><span data-stu-id="aad53-106">These structures are used by functions you can use to develop parsers and functions you can use to develop either parsers or experts.</span></span>



| <span data-ttu-id="aad53-107">Structure</span><span class="sxs-lookup"><span data-stu-id="aad53-107">Structure</span></span>                                 | <span data-ttu-id="aad53-108">Description</span><span class="sxs-lookup"><span data-stu-id="aad53-108">Description</span></span>                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aad53-109">MACFRAME</span><span class="sxs-lookup"><span data-stu-id="aad53-109">MACFRAME</span></span>](macframe.md)                  | <span data-ttu-id="aad53-110">Définit les protocoles initiaux les plus couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="aad53-110">Defines the most commonly used initial protocols.</span></span>                                                                               |
| [<span data-ttu-id="aad53-111">ENTRYPOINTS</span><span class="sxs-lookup"><span data-stu-id="aad53-111">ENTRYPOINTS</span></span>](entrypoints.md)            | <span data-ttu-id="aad53-112">Spécifie des pointeurs vers les points d’entrée de la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="aad53-112">Specifies pointers to the entry points for the Parser DLL.</span></span>                                                                      |
| [<span data-ttu-id="aad53-113">\_FOLLOWENTRY PF</span><span class="sxs-lookup"><span data-stu-id="aad53-113">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)     | <span data-ttu-id="aad53-114">Spécifie le protocole qui suit le protocole en cours.</span><span class="sxs-lookup"><span data-stu-id="aad53-114">Specifies the protocol that follows the current protocol.</span></span>                                                                       |
| [<span data-ttu-id="aad53-115">\_FOLLOWSET PF</span><span class="sxs-lookup"><span data-stu-id="aad53-115">PF\_FOLLOWSET</span></span>](pf-followset.md)         | <span data-ttu-id="aad53-116">Spécifie l’ensemble des protocoles qui suivent le protocole en cours.</span><span class="sxs-lookup"><span data-stu-id="aad53-116">Specifies the set of protocols that follows the current protocol.</span></span>                                                               |
| [<span data-ttu-id="aad53-117">\_HANDOFFENTRY PF</span><span class="sxs-lookup"><span data-stu-id="aad53-117">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)   | <span data-ttu-id="aad53-118">Spécifie le protocole qui transmet au protocole en cours ou le protocole que le protocole en cours transmet.</span><span class="sxs-lookup"><span data-stu-id="aad53-118">Specifies either the protocol that hands off to the current protocol or the protocol that the current protocol hands off to.</span></span>    |
| [<span data-ttu-id="aad53-119">\_HANDOFFSET PF</span><span class="sxs-lookup"><span data-stu-id="aad53-119">PF\_HANDOFFSET</span></span>](pf-handoffset.md)       | <span data-ttu-id="aad53-120">Spécifie le jeu de protocoles qui transmet au protocole en cours ou l’ensemble de protocoles vers lequel le protocole en cours est mis.</span><span class="sxs-lookup"><span data-stu-id="aad53-120">Specifies the set of protocols that hand off to the current protocol or the set of protocols the current protocol hands off to.</span></span> |
| [<span data-ttu-id="aad53-121">\_PARSERDLLINFO PF</span><span class="sxs-lookup"><span data-stu-id="aad53-121">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md) | <span data-ttu-id="aad53-122">Spécifie le nombre d’analyseurs dans la DLL de l’analyseur et les informations sur chaque analyseur.</span><span class="sxs-lookup"><span data-stu-id="aad53-122">Specifies the number of parsers in the parser DLL and information about each parser.</span></span>                                            |
| [<span data-ttu-id="aad53-123">\_PARSERINFO PF</span><span class="sxs-lookup"><span data-stu-id="aad53-123">PF\_PARSERINFO</span></span>](pf-parserinfo.md)       | <span data-ttu-id="aad53-124">Spécifie les informations relatives à un analyseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="aad53-124">Specifies information about a specific parser.</span></span>                                                                                  |
| [<span data-ttu-id="aad53-125">\_bit étiqueté</span><span class="sxs-lookup"><span data-stu-id="aad53-125">LABELED\_BIT</span></span>](labeled-bit.md)           | <span data-ttu-id="aad53-126">Spécifie des handles, des champs de bits ou des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="aad53-126">Specifies handles, BIT fields, or flags.</span></span>                                                                                        |
| [<span data-ttu-id="aad53-127">\_octet étiqueté</span><span class="sxs-lookup"><span data-stu-id="aad53-127">LABELED\_BYTE</span></span>](labeled-byte.md)         | <span data-ttu-id="aad53-128">Spécifie une paire d’étiquettes d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="aad53-128">Specifies a **BYTE** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="aad53-129">\_DWORD étiqueté</span><span class="sxs-lookup"><span data-stu-id="aad53-129">LABELED\_DWORD</span></span>](labeled-dword.md)       | <span data-ttu-id="aad53-130">Spécifie une paire d’étiquettes **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="aad53-130">Specifies a **DWORD** label pair.</span></span>                                                                                               |
| [<span data-ttu-id="aad53-131">\_mot étiqueté</span><span class="sxs-lookup"><span data-stu-id="aad53-131">LABELED\_WORD</span></span>](labeled-word.md)         | <span data-ttu-id="aad53-132">Spécifie une paire d’étiquettes **Word** .</span><span class="sxs-lookup"><span data-stu-id="aad53-132">Specifies a **WORD** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="aad53-133">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="aad53-133">PROPERTYINFO</span></span>](propertyinfo.md)          | <span data-ttu-id="aad53-134">Spécifie les propriétés dont l’analyseur de protocole a besoin pour décrire les frames.</span><span class="sxs-lookup"><span data-stu-id="aad53-134">Specifies the properties that the protocol parser requires to describe frames.</span></span>                                                  |
| [<span data-ttu-id="aad53-135">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="aad53-135">PROPERTYINST</span></span>](propertyinst.md)          | <span data-ttu-id="aad53-136">Spécifie une instance d’une propriété dans un frame.</span><span class="sxs-lookup"><span data-stu-id="aad53-136">Specifies an instance of a property in a frame.</span></span>                                                                                 |
| [<span data-ttu-id="aad53-137">PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="aad53-137">PROPERTYINSTEX</span></span>](propertyinstex.md)      | <span data-ttu-id="aad53-138">Spécifie une instance de propriété étendue et de forme libre.</span><span class="sxs-lookup"><span data-stu-id="aad53-138">Specifies a free-form, extended property instance.</span></span>                                                                              |
| [<span data-ttu-id="aad53-139">PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="aad53-139">PROTOCOLINFO</span></span>](protocolinfo.md)          | <span data-ttu-id="aad53-140">Spécifie un protocole.</span><span class="sxs-lookup"><span data-stu-id="aad53-140">Specifies a protocol.</span></span>                                                                                                           |
| [<span data-ttu-id="aad53-141">RANGE</span><span class="sxs-lookup"><span data-stu-id="aad53-141">RANGE</span></span>](range.md)                        | <span data-ttu-id="aad53-142">Spécifie une plage pour un nombre.</span><span class="sxs-lookup"><span data-stu-id="aad53-142">Specifies a range for a number.</span></span>                                                                                                 |
| [<span data-ttu-id="aad53-143">SET</span><span class="sxs-lookup"><span data-stu-id="aad53-143">SET</span></span>](set.md)                            | <span data-ttu-id="aad53-144">Spécifie une table de valeurs pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="aad53-144">Specifies a table of values for a property.</span></span>                                                                                     |



 

<span data-ttu-id="aad53-145">Pour plus d’informations sur les fonctions utilisées pour développer des dll d’analyseur, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="aad53-145">For information about functions used to develop parser DLLs, see the following topics.</span></span>



| <span data-ttu-id="aad53-146">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="aad53-146">For information about</span></span>                                         | <span data-ttu-id="aad53-147">Consultez</span><span class="sxs-lookup"><span data-stu-id="aad53-147">See</span></span>                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="aad53-148">Fonctions exportées par les dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="aad53-148">Functions that the parser DLLs export.</span></span>                        | [<span data-ttu-id="aad53-149">Fonctions d’exportation de DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="aad53-149">Parser DLL Export Functions</span></span>](parser-dll-export-functions.md)               |
| <span data-ttu-id="aad53-150">Fonctions que vous pouvez utiliser pour développer des dll d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="aad53-150">Functions that you can use to develop parser DLLs.</span></span>            | [<span data-ttu-id="aad53-151">Fonctions de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="aad53-151">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="aad53-152">Fonctions que vous pouvez utiliser pour développer des dll de l’analyseur et des experts.</span><span class="sxs-lookup"><span data-stu-id="aad53-152">Functions that you can use to develop parser and expert DLLs.</span></span> | [<span data-ttu-id="aad53-153">Fonctions courantes des experts et de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="aad53-153">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



