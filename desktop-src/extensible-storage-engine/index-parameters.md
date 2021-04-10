---
description: 'En savoir plus sur : paramètres d’index'
title: Paramètres d’index
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042788"
---
# <a name="index-parameters"></a><span data-ttu-id="bd848-103">Paramètres d’index</span><span class="sxs-lookup"><span data-stu-id="bd848-103">Index Parameters</span></span>


<span data-ttu-id="bd848-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bd848-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="index-parameters"></a><span data-ttu-id="bd848-105">Paramètres d’index</span><span class="sxs-lookup"><span data-stu-id="bd848-105">Index Parameters</span></span>

<span data-ttu-id="bd848-106">Cette rubrique contient des paramètres qui sont utilisés pour l’index.</span><span class="sxs-lookup"><span data-stu-id="bd848-106">This topic contains parameters that are used for the index.</span></span>

<span data-ttu-id="bd848-107">*JET_paramIndexTupleIncrement*</span><span class="sxs-lookup"><span data-stu-id="bd848-107">*JET_paramIndexTupleIncrement*</span></span>  
<span data-ttu-id="bd848-108">132</span><span class="sxs-lookup"><span data-stu-id="bd848-108">132</span></span>  

<span data-ttu-id="bd848-109">Ce paramètre spécifie la valeur par défaut pour l’incrément de décalage utilisé pour parcourir la valeur de la colonne source lors de la génération de chaque tuple.</span><span class="sxs-lookup"><span data-stu-id="bd848-109">This parameter specifies the default for the offset increment used to step through the source column value while generating each tuple.</span></span> <span data-ttu-id="bd848-110">Pour plus d’informations, consultez la structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bd848-110">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd848-111">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="bd848-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bd848-112">1</span><span class="sxs-lookup"><span data-stu-id="bd848-112">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="bd848-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="bd848-114">Integer</span><span class="sxs-lookup"><span data-stu-id="bd848-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-115">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="bd848-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bd848-116">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="bd848-116">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-117">Étendue :</span><span class="sxs-lookup"><span data-stu-id="bd848-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bd848-118">Instance</span><span class="sxs-lookup"><span data-stu-id="bd848-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-119">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-120">Oui</span><span class="sxs-lookup"><span data-stu-id="bd848-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-121">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-122">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-123">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="bd848-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bd848-124">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-125">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-126">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-127">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="bd848-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bd848-128">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-129">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="bd848-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bd848-130">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-131">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-132">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="bd848-132">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd848-133">*JET_paramIndexTupleStart*</span><span class="sxs-lookup"><span data-stu-id="bd848-133">*JET_paramIndexTupleStart*</span></span>  
<span data-ttu-id="bd848-134">133</span><span class="sxs-lookup"><span data-stu-id="bd848-134">133</span></span>  

<span data-ttu-id="bd848-135">Ce paramètre spécifie la valeur par défaut pour le décalage dans la valeur de colonne source au niveau de laquelle la génération de tuple démarrera.</span><span class="sxs-lookup"><span data-stu-id="bd848-135">This parameter specifies the default for the offset in the source column value at which tuple generation will start.</span></span> <span data-ttu-id="bd848-136">Pour plus d’informations, consultez la structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bd848-136">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd848-137">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="bd848-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bd848-138">0</span><span class="sxs-lookup"><span data-stu-id="bd848-138">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-139">Tapez :</span><span class="sxs-lookup"><span data-stu-id="bd848-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="bd848-140">Integer</span><span class="sxs-lookup"><span data-stu-id="bd848-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-141">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="bd848-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bd848-142">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="bd848-142">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-143">Étendue :</span><span class="sxs-lookup"><span data-stu-id="bd848-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bd848-144">Instance</span><span class="sxs-lookup"><span data-stu-id="bd848-144">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-145">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-146">Oui</span><span class="sxs-lookup"><span data-stu-id="bd848-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-147">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-148">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-148">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-149">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="bd848-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bd848-150">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-151">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-152">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-153">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="bd848-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bd848-154">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-155">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="bd848-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bd848-156">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-157">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-158">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="bd848-158">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd848-159">*JET_paramIndexTuplesLengthMax*</span><span class="sxs-lookup"><span data-stu-id="bd848-159">*JET_paramIndexTuplesLengthMax*</span></span>  
<span data-ttu-id="bd848-160">111</span><span class="sxs-lookup"><span data-stu-id="bd848-160">111</span></span>  

<span data-ttu-id="bd848-161">Ce paramètre spécifie la valeur par défaut de la longueur maximale du tuple dans un index de Tuple.</span><span class="sxs-lookup"><span data-stu-id="bd848-161">This parameter specifies the default for the maximum tuple length in a tuple index.</span></span> <span data-ttu-id="bd848-162">Pour plus d’informations, consultez la structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bd848-162">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<span data-ttu-id="bd848-163">**Windows Vista :**  Avant Windows Vista, l’affectation de la valeur zéro à ce paramètre permet de rétablir sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd848-163">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="bd848-164">Pour Windows Vista, ce n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bd848-164">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd848-165">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="bd848-165">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bd848-166">10</span><span class="sxs-lookup"><span data-stu-id="bd848-166">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-167">Tapez :</span><span class="sxs-lookup"><span data-stu-id="bd848-167">Type:</span></span></p></td>
<td><p><span data-ttu-id="bd848-168">Integer</span><span class="sxs-lookup"><span data-stu-id="bd848-168">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-169">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="bd848-169">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bd848-170"><strong>Windows 2000, Windows XP et Windows Server 2003 : </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="bd848-170"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="bd848-171"><strong>Windows Vista :</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="bd848-171"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-172">Étendue :</span><span class="sxs-lookup"><span data-stu-id="bd848-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bd848-173">Instance</span><span class="sxs-lookup"><span data-stu-id="bd848-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-174">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-175">Oui</span><span class="sxs-lookup"><span data-stu-id="bd848-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-176">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-177">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-178">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="bd848-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bd848-179">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-180">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-181">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-182">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="bd848-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bd848-183">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-183">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-184">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="bd848-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bd848-185">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-185">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-186">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-187">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="bd848-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd848-188">*JET_paramIndexTuplesLengthMin*</span><span class="sxs-lookup"><span data-stu-id="bd848-188">*JET_paramIndexTuplesLengthMin*</span></span>  
<span data-ttu-id="bd848-189">110</span><span class="sxs-lookup"><span data-stu-id="bd848-189">110</span></span>  

<span data-ttu-id="bd848-190">Ce paramètre spécifie la valeur par défaut pour la longueur minimale du tuple dans un index de Tuple.</span><span class="sxs-lookup"><span data-stu-id="bd848-190">This parameter specifies the default for the minimum tuple length in a tuple index.</span></span> <span data-ttu-id="bd848-191">Pour plus d’informations, consultez [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bd848-191">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="bd848-192">**Windows Vista :**  Avant Windows Vista, l’affectation de la valeur zéro à ce paramètre permet de rétablir sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd848-192">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="bd848-193">Pour Windows Vista, ce n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bd848-193">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd848-194">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="bd848-194">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bd848-195">3</span><span class="sxs-lookup"><span data-stu-id="bd848-195">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-196">Tapez :</span><span class="sxs-lookup"><span data-stu-id="bd848-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="bd848-197">Integer</span><span class="sxs-lookup"><span data-stu-id="bd848-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-198">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="bd848-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bd848-199"><strong>Windows 2000, Windows XP et Windows Server 2003 : </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="bd848-199"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="bd848-200"><strong>Windows Vista :</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="bd848-200"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-201">Étendue :</span><span class="sxs-lookup"><span data-stu-id="bd848-201">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bd848-202">Instance</span><span class="sxs-lookup"><span data-stu-id="bd848-202">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-203">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-203">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-204">Oui</span><span class="sxs-lookup"><span data-stu-id="bd848-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-205">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-205">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-206">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-206">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-207">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="bd848-207">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bd848-208">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-209">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-209">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-210">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-210">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-211">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="bd848-211">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bd848-212">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-212">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-213">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="bd848-213">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bd848-214">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-215">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-215">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-216">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="bd848-216">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd848-217">*JET_paramIndexTuplesToIndexMax*</span><span class="sxs-lookup"><span data-stu-id="bd848-217">*JET_paramIndexTuplesToIndexMax*</span></span>  
<span data-ttu-id="bd848-218">112</span><span class="sxs-lookup"><span data-stu-id="bd848-218">112</span></span>  

<span data-ttu-id="bd848-219">Ce paramètre spécifie la valeur par défaut pour la longueur maximale d’une chaîne source à décomposer en tuples pour un index de Tuple.</span><span class="sxs-lookup"><span data-stu-id="bd848-219">This parameter specifies the default for the maximum length of a source string to break into tuples for a tuple index.</span></span> <span data-ttu-id="bd848-220">Pour plus d’informations, consultez [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bd848-220">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="bd848-221">**Windows Vista :**  Avant Windows Vista, l’affectation de la valeur zéro à ce paramètre permet de rétablir sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd848-221">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="bd848-222">Pour Windows Vista, ce n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bd848-222">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd848-223">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="bd848-223">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bd848-224">32767</span><span class="sxs-lookup"><span data-stu-id="bd848-224">32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-225">Tapez :</span><span class="sxs-lookup"><span data-stu-id="bd848-225">Type:</span></span></p></td>
<td><p><span data-ttu-id="bd848-226">Integer</span><span class="sxs-lookup"><span data-stu-id="bd848-226">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-227">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="bd848-227">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bd848-228"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  0 – 32767</span><span class="sxs-lookup"><span data-stu-id="bd848-228"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 32767</span></span></p>
<p><span data-ttu-id="bd848-229"><strong>Windows Vista :</strong>  1 – 32767</span><span class="sxs-lookup"><span data-stu-id="bd848-229"><strong>Windows Vista:</strong>  1 – 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-230">Étendue :</span><span class="sxs-lookup"><span data-stu-id="bd848-230">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bd848-231">Instance</span><span class="sxs-lookup"><span data-stu-id="bd848-231">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-232">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-232">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-233">Oui</span><span class="sxs-lookup"><span data-stu-id="bd848-233">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-234">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-234">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-235">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-235">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-236">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="bd848-236">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bd848-237">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-237">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-238">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-238">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-239">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-239">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-240">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="bd848-240">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bd848-241">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-241">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-242">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="bd848-242">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bd848-243">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-243">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-244">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-244">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-245">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="bd848-245">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd848-246">*JET_paramUnicodeIndexDefault*</span><span class="sxs-lookup"><span data-stu-id="bd848-246">*JET_paramUnicodeIndexDefault*</span></span>  
<span data-ttu-id="bd848-247">72</span><span class="sxs-lookup"><span data-stu-id="bd848-247">72</span></span>  

<span data-ttu-id="bd848-248">Ce paramètre contrôle les paramètres Unicode par défaut utilisés par n’importe quel index sur une colonne de clé Unicode.</span><span class="sxs-lookup"><span data-stu-id="bd848-248">This parameter controls the default Unicode parameters used by any index over a Unicode key column.</span></span> <span data-ttu-id="bd848-249">Le type de ce paramètre est [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) et est passé en fait à l’aide d’un pointeur de mémoire tampon stocké dans le paramètre entier de [JetGetSystemParameter](./jetgetsystemparameter-function.md) et [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd848-249">The type of this parameter is [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and is actually passed using a buffer pointer stored in the integer parameter of [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="bd848-250">La taille de la mémoire tampon doit être égale à la taille de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) et doit être passée à [JetGetSystemParameter](./jetgetsystemparameter-function.md) à l’aide du paramètre de taille de mémoire tampon de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bd848-250">The size of the buffer must equal the size of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and must be passed to [JetGetSystemParameter](./jetgetsystemparameter-function.md) using the string buffer size parameter.</span></span> <span data-ttu-id="bd848-251">Cela est clairement incohérent, mais il s’agit du comportement de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="bd848-251">This is clearly inconsistent but that is the behavior of this parameter.</span></span>

<span data-ttu-id="bd848-252">La valeur par défaut de ce paramètre contient un LCID pour les paramètres régionaux anglais (États-Unis) et les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)suivants : LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="bd848-252">The default value of this parameter contains an LCID for the U.S. English locale and the following [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="bd848-253">**Windows 2000 :**  Le SORTID dans le LCID est ignoré.</span><span class="sxs-lookup"><span data-stu-id="bd848-253">**Windows 2000:**  The SORTID in the LCID is ignored.</span></span> <span data-ttu-id="bd848-254">Un SORTID de SORT_DEFAULT est toujours utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd848-254">A SORTID of SORT_DEFAULT is always used.</span></span>

<span data-ttu-id="bd848-255">**Windows 2000 :**  Les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) doivent contenir les indicateurs suivants : LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="bd848-255">**Windows 2000:**  The [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) flags must contain the following flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="bd848-256">En outre, les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)peuvent contenir les indicateurs suivants : NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="bd848-256">In addition, the [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags may contain the following flags: NORM_IGNORENONSPACE.</span></span>

<span data-ttu-id="bd848-257">**Remarque**  Si votre application souhaite stocker des données Unicode, il est vivement recommandé de ne pas compter sur les paramètres Unicode par défaut de vos index.</span><span class="sxs-lookup"><span data-stu-id="bd848-257">**Note**  If your application wishes to store Unicode data, then it is strongly recommended that you do not rely on the default Unicode parameters for your indexes.</span></span> <span data-ttu-id="bd848-258">L’utilisation de l’anglais des États-Unis est équivaut à l’utilisation des paramètres régionaux invariants et les indicateurs [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)par défaut sont connus pour interférer sérieusement avec certaines langues.</span><span class="sxs-lookup"><span data-stu-id="bd848-258">The use of U.S. English is tantamount to using the invariant locale and the default [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags are known to seriously interfere with some languages.</span></span> <span data-ttu-id="bd848-259">Vous devez toujours spécifier vos propres paramètres pour les paramètres Unicode à JetCreateIndex2 à l’aide de [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="bd848-259">You should always specify your own settings for the Unicode parameters to JetCreateIndex2 using [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd848-260">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="bd848-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bd848-261">Spécial</span><span class="sxs-lookup"><span data-stu-id="bd848-261">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-262">Tapez :</span><span class="sxs-lookup"><span data-stu-id="bd848-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="bd848-263">JET_UNICODEINDEX \* (JET_UNICODEINDEX)</span><span class="sxs-lookup"><span data-stu-id="bd848-263">JET_UNICODEINDEX\* (JET_UNICODEINDEX)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-264">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="bd848-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bd848-265">Spécial</span><span class="sxs-lookup"><span data-stu-id="bd848-265">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-266">Étendue :</span><span class="sxs-lookup"><span data-stu-id="bd848-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bd848-267">Instance</span><span class="sxs-lookup"><span data-stu-id="bd848-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-268">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-269">Oui</span><span class="sxs-lookup"><span data-stu-id="bd848-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-270">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="bd848-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bd848-271">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-272">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="bd848-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bd848-273">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-273">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-274">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-275">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-276">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="bd848-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bd848-277">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-278">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="bd848-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bd848-279">Non</span><span class="sxs-lookup"><span data-stu-id="bd848-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-280">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="bd848-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bd848-281">Tous</span><span class="sxs-lookup"><span data-stu-id="bd848-281">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="bd848-282">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd848-282">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd848-283"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bd848-283"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bd848-284">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="bd848-284">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd848-285"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="bd848-285"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bd848-286">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bd848-286">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd848-287"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="bd848-287"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bd848-288">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="bd848-288">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bd848-289">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd848-289">See Also</span></span>

[<span data-ttu-id="bd848-290">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="bd848-290">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="bd848-291">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="bd848-291">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="bd848-292">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="bd848-292">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="bd848-293">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="bd848-293">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="bd848-294">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bd848-294">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="bd848-295">JetInit</span><span class="sxs-lookup"><span data-stu-id="bd848-295">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="bd848-296">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bd848-296">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
