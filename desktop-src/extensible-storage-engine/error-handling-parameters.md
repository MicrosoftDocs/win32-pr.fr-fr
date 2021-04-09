---
description: En savoir plus sur les paramètres de gestion des erreurs
title: Paramètres de gestion des erreurs
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868734"
---
# <a name="error-handling-parameters"></a><span data-ttu-id="010d4-103">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="010d4-103">Error Handling Parameters</span></span>


<span data-ttu-id="010d4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="010d4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-parameters"></a><span data-ttu-id="010d4-105">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="010d4-105">Error Handling Parameters</span></span>

<span data-ttu-id="010d4-106">Cette rubrique contient des paramètres qui sont utilisés pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="010d4-106">This topic contains parameters that are used for error handling.</span></span>

<span data-ttu-id="010d4-107">*JET_paramErrorToString* 70</span><span class="sxs-lookup"><span data-stu-id="010d4-107">*JET_paramErrorToString* 70</span></span>  

<span data-ttu-id="010d4-108">Ce paramètre peut être utilisé pour convertir un [JET_ERR](./jet-err.md) en chaîne.</span><span class="sxs-lookup"><span data-stu-id="010d4-108">This parameter can be used to convert a [JET_ERR](./jet-err.md) into a string.</span></span> <span data-ttu-id="010d4-109">Cette opération s’effectue à l’aide d’un appel spécial à [JetGetSystemParameter](./jetgetsystemparameter-function.md) où la mémoire tampon de sortie entière contient la valeur [JET_ERR](./jet-err.md) à convertir (en tant que paramètre d’entrée) et la mémoire tampon de sortie de chaîne retourne la chaîne d’erreur correspondante.</span><span class="sxs-lookup"><span data-stu-id="010d4-109">This is done using a special call to [JetGetSystemParameter](./jetgetsystemparameter-function.md) where the integer output buffer contains the [JET_ERR](./jet-err.md) value to be converted (as an input parameter) and the string output buffer returns the matching error string.</span></span> <span data-ttu-id="010d4-110">La chaîne se présente comme suit : « JET_errSuccess, opération réussie ».</span><span class="sxs-lookup"><span data-stu-id="010d4-110">The string will look something like this: "JET_errSuccess,Successful Operation".</span></span> <span data-ttu-id="010d4-111">La chaîne est composée du nom symbolique de la chaîne, d’une virgule, puis d’une description textuelle simple de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="010d4-111">The string is composed of the symbolic name for the string, then a comma, and then a simple text description of the error.</span></span> <span data-ttu-id="010d4-112">La chaîne de description peut elle-même contenir des virgules.</span><span class="sxs-lookup"><span data-stu-id="010d4-112">The description string may itself contain commas.</span></span> <span data-ttu-id="010d4-113">Si l’erreur n’est pas reconnue, la chaîne sera « erreur inconnue, erreur inconnue ».</span><span class="sxs-lookup"><span data-stu-id="010d4-113">If the error is not recognized then the string will be "Unknown Error,Unknown Error".</span></span>

<span data-ttu-id="010d4-114">**Remarque**  Ce paramètre est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="010d4-114">**Note**  This parameter is read only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="010d4-115">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="010d4-115">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="010d4-116">Spécial</span><span class="sxs-lookup"><span data-stu-id="010d4-116">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-117">Tapez :</span><span class="sxs-lookup"><span data-stu-id="010d4-117">Type:</span></span></p></td>
<td><p><span data-ttu-id="010d4-118">Spécial</span><span class="sxs-lookup"><span data-stu-id="010d4-118">Special</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-119">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="010d4-119">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="010d4-120">Spécial</span><span class="sxs-lookup"><span data-stu-id="010d4-120">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-121">Étendue :</span><span class="sxs-lookup"><span data-stu-id="010d4-121">Scope:</span></span></p></td>
<td><p><span data-ttu-id="010d4-122">Global</span><span class="sxs-lookup"><span data-stu-id="010d4-122">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-123">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="010d4-123">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="010d4-124">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-125">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="010d4-125">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="010d4-126">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-127">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="010d4-127">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="010d4-128">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-129">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="010d4-129">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="010d4-130">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-131">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="010d4-131">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="010d4-132">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-133">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="010d4-133">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="010d4-134">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-135">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="010d4-135">Availability:</span></span></p></td>
<td><p><span data-ttu-id="010d4-136">Tous</span><span class="sxs-lookup"><span data-stu-id="010d4-136">All</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="010d4-137">*JET_paramExceptionAction*</span><span class="sxs-lookup"><span data-stu-id="010d4-137">*JET_paramExceptionAction*</span></span>  
<span data-ttu-id="010d4-138">98</span><span class="sxs-lookup"><span data-stu-id="010d4-138">98</span></span>  

<span data-ttu-id="010d4-139">Ce paramètre contrôle ce qui se produit lorsqu’une exception est levée par le moteur de base de données ou le code qui est appelé par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="010d4-139">This parameter controls what happens when an exception is thrown by the database engine or code that is called by the database engine.</span></span> <span data-ttu-id="010d4-140">Quand la valeur JET_ExceptionMsgBox, toute exception est levée dans le filtre d’exception non géré Windows.</span><span class="sxs-lookup"><span data-stu-id="010d4-140">When set to JET_ExceptionMsgBox, any exception will be thrown to the Windows unhandled exception filter.</span></span> <span data-ttu-id="010d4-141">L’exception est alors gérée en tant qu’échec de l’application.</span><span class="sxs-lookup"><span data-stu-id="010d4-141">This will result in the exception being handled as an application failure.</span></span> <span data-ttu-id="010d4-142">L’objectif est d’empêcher le code d’application d’essayer à tort d’intercepter et d’ignorer une exception générée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="010d4-142">The intent is to prevent application code from erroneously trying to catch and ignore an exception generated by the database engine.</span></span> <span data-ttu-id="010d4-143">Cela ne peut pas être autorisé, car une base de données endommagée peut se produire.</span><span class="sxs-lookup"><span data-stu-id="010d4-143">This cannot be allowed because database corruption could occur.</span></span> <span data-ttu-id="010d4-144">Si l’application souhaite gérer correctement ces exceptions, la protection peut être désactivée en définissant ce paramètre sur JET_ExceptionNone.</span><span class="sxs-lookup"><span data-stu-id="010d4-144">If the application wishes to properly handle these exceptions then the protection can be disabled by setting this parameter to JET_ExceptionNone.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="010d4-145">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="010d4-145">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="010d4-146">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="010d4-146">JET_ExceptionMsgBox</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-147">Tapez :</span><span class="sxs-lookup"><span data-stu-id="010d4-147">Type:</span></span></p></td>
<td><p><span data-ttu-id="010d4-148">Integer</span><span class="sxs-lookup"><span data-stu-id="010d4-148">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-149">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="010d4-149">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="010d4-150">JET_ExceptionMsgBox, JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="010d4-150">JET_ExceptionMsgBox, JET_ExceptionNone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-151">Étendue :</span><span class="sxs-lookup"><span data-stu-id="010d4-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="010d4-152">Global</span><span class="sxs-lookup"><span data-stu-id="010d4-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-153">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="010d4-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="010d4-154"><strong>Windows 2000, Windows XP et Windows Server 2003 :  </strong>  º</span><span class="sxs-lookup"><span data-stu-id="010d4-154"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="010d4-155"><strong>Windows Vista :</strong>  Oui</span><span class="sxs-lookup"><span data-stu-id="010d4-155"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-156">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="010d4-156">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="010d4-157"><strong>Windows 2000, Windows XP et Windows Server 2003 :  </strong>  º</span><span class="sxs-lookup"><span data-stu-id="010d4-157"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="010d4-158"><strong>Windows Vista :</strong>  Oui</span><span class="sxs-lookup"><span data-stu-id="010d4-158"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-159">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="010d4-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="010d4-160">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-160">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-161">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="010d4-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="010d4-162">Oui</span><span class="sxs-lookup"><span data-stu-id="010d4-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-163">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="010d4-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="010d4-164">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-165">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="010d4-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="010d4-166">Non</span><span class="sxs-lookup"><span data-stu-id="010d4-166">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-167">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="010d4-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="010d4-168">Tous</span><span class="sxs-lookup"><span data-stu-id="010d4-168">All</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a><span data-ttu-id="010d4-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="010d4-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="010d4-170"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="010d4-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="010d4-171">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="010d4-171">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="010d4-172"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="010d4-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="010d4-173">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="010d4-173">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="010d4-174"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="010d4-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="010d4-175">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="010d4-175">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a><span data-ttu-id="010d4-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="010d4-176">See Also</span></span>

[<span data-ttu-id="010d4-177">Constantes de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="010d4-177">Error Handling Constants</span></span>](./error-handling-constants.md)  
[<span data-ttu-id="010d4-178">Codes d’erreur du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="010d4-178">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="010d4-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="010d4-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="010d4-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="010d4-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="010d4-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="010d4-181">JetInit</span></span>](./jetinit-function.md)
