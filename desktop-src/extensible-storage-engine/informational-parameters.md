---
description: 'En savoir plus sur les paramètres suivants : informations'
title: Paramètres d’information
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753317"
---
# <a name="informational-parameters"></a><span data-ttu-id="a4975-103">Paramètres d’information</span><span class="sxs-lookup"><span data-stu-id="a4975-103">Informational Parameters</span></span>


<span data-ttu-id="a4975-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a4975-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="informational-parameters"></a><span data-ttu-id="a4975-105">Paramètres d’information</span><span class="sxs-lookup"><span data-stu-id="a4975-105">Informational Parameters</span></span>

<span data-ttu-id="a4975-106">Cette rubrique contient des paramètres utilisés pour exposer des informations sur le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="a4975-106">This topic contains parameters that are used to expose information about the database engine.</span></span>

<span data-ttu-id="a4975-107">*JET_paramKeyMost*</span><span class="sxs-lookup"><span data-stu-id="a4975-107">*JET_paramKeyMost*</span></span>  
<span data-ttu-id="a4975-108">134</span><span class="sxs-lookup"><span data-stu-id="a4975-108">134</span></span>  

<span data-ttu-id="a4975-109">Ce paramètre en lecture seule indique la longueur de clé d’index maximale autorisée qui peut être sélectionnée pour la taille de page de la base de données actuelle (telle que configurée par JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="a4975-109">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by JET_paramDatabasePageSize).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4975-110">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="a4975-110">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a4975-111">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="a4975-111">JET_cbKeyMost4KBytePage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-112">Tapez :</span><span class="sxs-lookup"><span data-stu-id="a4975-112">Type:</span></span></p></td>
<td><p><span data-ttu-id="a4975-113">Integer</span><span class="sxs-lookup"><span data-stu-id="a4975-113">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-114">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="a4975-114">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a4975-115">255 – 65535</span><span class="sxs-lookup"><span data-stu-id="a4975-115">255 – 65535</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-116">Étendue :</span><span class="sxs-lookup"><span data-stu-id="a4975-116">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a4975-117">Global</span><span class="sxs-lookup"><span data-stu-id="a4975-117">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-118">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a4975-118">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a4975-119">N/A</span><span class="sxs-lookup"><span data-stu-id="a4975-119">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-120">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a4975-120">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a4975-121">N/A</span><span class="sxs-lookup"><span data-stu-id="a4975-121">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-122">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="a4975-122">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a4975-123">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-123">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-124">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="a4975-124">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a4975-125">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-125">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-126">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="a4975-126">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a4975-127">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-127">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-128">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="a4975-128">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a4975-129">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-129">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-130">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="a4975-130">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a4975-131">À compter de Windows Server 2008 et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4975-131">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4975-132">*JET_paramMaxColtyp*</span><span class="sxs-lookup"><span data-stu-id="a4975-132">*JET_paramMaxColtyp*</span></span>  
<span data-ttu-id="a4975-133">131</span><span class="sxs-lookup"><span data-stu-id="a4975-133">131</span></span>  

<span data-ttu-id="a4975-134">Ce paramètre en lecture seule retourne la [JET_COLTYP](./jet-coltyp.md) maximale (JET_coltypMax) pour cette version du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="a4975-134">This read only parameter returns the maximum [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) for that version of the database engine.</span></span> <span data-ttu-id="a4975-135">Cette valeur peut être utilisée pour tester la prise en charge d’un [JET_COLTYP](./jet-coltyp.md)spécifique.</span><span class="sxs-lookup"><span data-stu-id="a4975-135">This value can be used to test for support of a specific [JET_COLTYP](./jet-coltyp.md).</span></span> <span data-ttu-id="a4975-136">Si un [JET_COLTYP](./jet-coltyp.md) donné est inférieur à la valeur de ce paramètre, il est pris en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="a4975-136">If a given [JET_COLTYP](./jet-coltyp.md) is less than the value of this parameter then it is supported by the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4975-137">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="a4975-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a4975-138">JET_coltypUnsignedShort + 1</span><span class="sxs-lookup"><span data-stu-id="a4975-138">JET_coltypUnsignedShort + 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-139">Tapez :</span><span class="sxs-lookup"><span data-stu-id="a4975-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="a4975-140">Integer</span><span class="sxs-lookup"><span data-stu-id="a4975-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-141">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="a4975-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a4975-142">0 – 255</span><span class="sxs-lookup"><span data-stu-id="a4975-142">0 – 255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-143">Étendue :</span><span class="sxs-lookup"><span data-stu-id="a4975-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="a4975-144">Global</span><span class="sxs-lookup"><span data-stu-id="a4975-144">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-145">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a4975-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="a4975-146">N/A</span><span class="sxs-lookup"><span data-stu-id="a4975-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-147">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a4975-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="a4975-148">N/A</span><span class="sxs-lookup"><span data-stu-id="a4975-148">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-149">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="a4975-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="a4975-150">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-151">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="a4975-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="a4975-152">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-153">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="a4975-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="a4975-154">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-155">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="a4975-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="a4975-156">Non</span><span class="sxs-lookup"><span data-stu-id="a4975-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-157">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="a4975-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="a4975-158">À compter de Windows Server 2008 et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4975-158">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4975-159">*JET_paramLVChunkSizeMost*</span><span class="sxs-lookup"><span data-stu-id="a4975-159">*JET_paramLVChunkSizeMost*</span></span>  
<span data-ttu-id="a4975-160">163</span><span class="sxs-lookup"><span data-stu-id="a4975-160">163</span></span>  

<span data-ttu-id="a4975-161">Paramètre en lecture seule qui retourne la taille de segment de valeur longue en fonction de la taille de page configurée.</span><span class="sxs-lookup"><span data-stu-id="a4975-161">Read only parameter that returns the long-value chunk size based on configured page size.</span></span> <span data-ttu-id="a4975-162">Si une valeur long doit être lue ou écrite avec plusieurs appels de colonne jet {set, Retrieve}, l’utilisation d’une mémoire tampon dont la taille est un multiple de la taille de segment est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="a4975-162">If a long-value is to be read or written with multiple Jet{Set,Retrieve}Column calls then using a buffer whose size is a multiple of the chunk size is more efficient.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4975-163">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="a4975-163">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="a4975-164">2 ko page = 1966 octets</span><span class="sxs-lookup"><span data-stu-id="a4975-164">2kb page = 1966 bytes</span></span><br />
<span data-ttu-id="a4975-165">4 ko page = 4014 octets</span><span class="sxs-lookup"><span data-stu-id="a4975-165">4kb page = 4014 bytes</span></span><br />
<span data-ttu-id="a4975-166">8 ko page = 8110 octets</span><span class="sxs-lookup"><span data-stu-id="a4975-166">8kb page = 8110 bytes</span></span><br />
<span data-ttu-id="a4975-167">16 ko page = 4050 octets</span><span class="sxs-lookup"><span data-stu-id="a4975-167">16kb page = 4050 bytes</span></span><br />
<span data-ttu-id="a4975-168">32KO page = 8150 octets</span><span class="sxs-lookup"><span data-stu-id="a4975-168">32kb page = 8150 bytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-169">Tapez :</span><span class="sxs-lookup"><span data-stu-id="a4975-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="a4975-170">Integer</span><span class="sxs-lookup"><span data-stu-id="a4975-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-171">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="a4975-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="a4975-172">0-10000</span><span class="sxs-lookup"><span data-stu-id="a4975-172">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-173">Étendue :</span><span class="sxs-lookup"><span data-stu-id="a4975-173">Scope:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-174">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="a4975-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-175">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="a4975-175">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-176">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="a4975-176">Affects Physical Layout:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-177">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="a4975-177">Affects Reliability:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-178">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="a4975-178">Affects Performance:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-179">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="a4975-179">Affects Resources:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-180">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="a4975-180">Availability:</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="a4975-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4975-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4975-182"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a4975-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a4975-183">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4975-183">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4975-184"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a4975-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a4975-185">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a4975-185">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4975-186"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a4975-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a4975-187">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a4975-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a4975-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4975-188">See Also</span></span>

[<span data-ttu-id="a4975-189">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="a4975-189">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a4975-190">JetInit</span><span class="sxs-lookup"><span data-stu-id="a4975-190">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="a4975-191">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="a4975-191">JET_COLTYP</span></span>](./jet-coltyp.md)
