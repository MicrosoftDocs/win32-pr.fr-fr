---
description: 'En savoir plus sur : codes d’erreur du moteur de stockage extensible'
title: Codes d’erreur du moteur de stockage extensible
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541966"
---
# <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="6847b-103">Codes d’erreur du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="6847b-103">Extensible Storage Engine Error Codes</span></span>


<span data-ttu-id="6847b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6847b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="6847b-105">Codes d’erreur du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="6847b-105">Extensible Storage Engine Error Codes</span></span>

<span data-ttu-id="6847b-106">Les codes d’erreur (indicateurs) suivants sont utilisés par les fonctions de l’API du moteur de stockage extensible.</span><span class="sxs-lookup"><span data-stu-id="6847b-106">The following error codes (flags) are used by functions in the Extensible Storage Engine API.</span></span>

<span data-ttu-id="6847b-107">Une [JET_ERR](./jet-err.md) valeur de zéro doit être interprétée comme une réussite.</span><span class="sxs-lookup"><span data-stu-id="6847b-107">A [JET_ERR](./jet-err.md) value of zero should be interpreted as success.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6847b-108">Succès</span><span class="sxs-lookup"><span data-stu-id="6847b-108">Success</span></span></p></th>
<th><p><span data-ttu-id="6847b-109">Description</span><span class="sxs-lookup"><span data-stu-id="6847b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6847b-110">JET_errSuccess 0</span><span class="sxs-lookup"><span data-stu-id="6847b-110">JET_errSuccess 0</span></span></p></td>
<td><p><span data-ttu-id="6847b-111">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="6847b-111">The function succeeded.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6847b-112">Une valeur [JET_ERR](./jet-err.md) supérieure à zéro doit être interprétée comme un avertissement.</span><span class="sxs-lookup"><span data-stu-id="6847b-112">A [JET_ERR](./jet-err.md) value that is greater than zero should be interpreted as a warning.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6847b-113">Avertissements</span><span class="sxs-lookup"><span data-stu-id="6847b-113">Warnings</span></span></p></th>
<th><p><span data-ttu-id="6847b-114">Description</span><span class="sxs-lookup"><span data-stu-id="6847b-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6847b-115">JET_wrnRemainingVersions</span><span class="sxs-lookup"><span data-stu-id="6847b-115">JET_wrnRemainingVersions</span></span><br />
<span data-ttu-id="6847b-116">321</span><span class="sxs-lookup"><span data-stu-id="6847b-116">321</span></span></p></td>
<td><p><span data-ttu-id="6847b-117">La Banque des versions est toujours active.</span><span class="sxs-lookup"><span data-stu-id="6847b-117">The version store is still active.</span></span> <span data-ttu-id="6847b-118">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-118">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-119">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="6847b-119">JET_wrnUniqueKey</span></span><br />
<span data-ttu-id="6847b-120">345</span><span class="sxs-lookup"><span data-stu-id="6847b-120">345</span></span></p></td>
<td><p><span data-ttu-id="6847b-121">Une recherche sur un index non unique a produit une clé unique.</span><span class="sxs-lookup"><span data-stu-id="6847b-121">A seek on a non-unique index yielded a unique key.</span></span> <span data-ttu-id="6847b-122">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-122">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-123">JET_wrnSeparateLongValue</span><span class="sxs-lookup"><span data-stu-id="6847b-123">JET_wrnSeparateLongValue</span></span><br />
<span data-ttu-id="6847b-124">406</span><span class="sxs-lookup"><span data-stu-id="6847b-124">406</span></span></p></td>
<td><p><span data-ttu-id="6847b-125">Une colonne de base de données est une valeur long séparée.</span><span class="sxs-lookup"><span data-stu-id="6847b-125">A database column is a separated long value.</span></span> <span data-ttu-id="6847b-126">Cette erreur est retournée par le gestionnaire d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6847b-126">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-127">JET_wrnExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="6847b-127">JET_wrnExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="6847b-128">558</span><span class="sxs-lookup"><span data-stu-id="6847b-128">558</span></span></p></td>
<td><p><span data-ttu-id="6847b-129">La signature du fichier journal existant est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-129">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-130">JET_wrnExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="6847b-130">JET_wrnExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="6847b-131">559</span><span class="sxs-lookup"><span data-stu-id="6847b-131">559</span></span></p></td>
<td><p><span data-ttu-id="6847b-132">Le fichier journal existant n’est pas contigu.</span><span class="sxs-lookup"><span data-stu-id="6847b-132">The existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-133">JET_wrnSkipThisRecord</span><span class="sxs-lookup"><span data-stu-id="6847b-133">JET_wrnSkipThisRecord</span></span><br />
<span data-ttu-id="6847b-134">564</span><span class="sxs-lookup"><span data-stu-id="6847b-134">564</span></span></p></td>
<td><p><span data-ttu-id="6847b-135">Cette erreur est réservée à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="6847b-135">This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-136">JET_wrnTargetInstanceRunning</span><span class="sxs-lookup"><span data-stu-id="6847b-136">JET_wrnTargetInstanceRunning</span></span><br />
<span data-ttu-id="6847b-137">578</span><span class="sxs-lookup"><span data-stu-id="6847b-137">578</span></span></p></td>
<td><p><span data-ttu-id="6847b-138">Le TargetInstance spécifié pour la restauration est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6847b-138">The TargetInstance specified for the restore is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-139">JET_wrnDatabaseRepaired</span><span class="sxs-lookup"><span data-stu-id="6847b-139">JET_wrnDatabaseRepaired</span></span><br />
<span data-ttu-id="6847b-140">595</span><span class="sxs-lookup"><span data-stu-id="6847b-140">595</span></span></p></td>
<td><p><span data-ttu-id="6847b-141">La base de données endommagée a été réparée.</span><span class="sxs-lookup"><span data-stu-id="6847b-141">The database corruption has been repaired.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-142">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="6847b-142">JET_wrnColumnNull</span></span><br />
<span data-ttu-id="6847b-143">1004</span><span class="sxs-lookup"><span data-stu-id="6847b-143">1004</span></span></p></td>
<td><p><span data-ttu-id="6847b-144">La colonne a une valeur <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="6847b-144">The column has a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-145">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="6847b-145">JET_wrnBufferTruncated</span></span><br />
<span data-ttu-id="6847b-146">1006</span><span class="sxs-lookup"><span data-stu-id="6847b-146">1006</span></span></p></td>
<td><p><span data-ttu-id="6847b-147">La mémoire tampon est insuffisante pour les données.</span><span class="sxs-lookup"><span data-stu-id="6847b-147">The buffer is too small for the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-148">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="6847b-148">JET_wrnDatabaseAttached</span></span><br />
<span data-ttu-id="6847b-149">1007</span><span class="sxs-lookup"><span data-stu-id="6847b-149">1007</span></span></p></td>
<td><p><span data-ttu-id="6847b-150">La base de données est déjà attachée.</span><span class="sxs-lookup"><span data-stu-id="6847b-150">The database is already attached.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-151">JET_wrnSortOverflow</span><span class="sxs-lookup"><span data-stu-id="6847b-151">JET_wrnSortOverflow</span></span><br />
<span data-ttu-id="6847b-152">1009</span><span class="sxs-lookup"><span data-stu-id="6847b-152">1009</span></span></p></td>
<td><p><span data-ttu-id="6847b-153">Le tri en cours de tentative ne dispose pas de suffisamment de mémoire pour se terminer.</span><span class="sxs-lookup"><span data-stu-id="6847b-153">The sort that is being attempted does not have enough memory to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-154">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="6847b-154">JET_wrnSeekNotEqual</span></span><br />
<span data-ttu-id="6847b-155">1039</span><span class="sxs-lookup"><span data-stu-id="6847b-155">1039</span></span></p></td>
<td><p><span data-ttu-id="6847b-156">Une correspondance exacte n’a pas été trouvée pendant une recherche.</span><span class="sxs-lookup"><span data-stu-id="6847b-156">An exact match was not found during a seek.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-157">JET_wrnRecordFoundGreater</span><span class="sxs-lookup"><span data-stu-id="6847b-157">JET_wrnRecordFoundGreater</span></span><br />
<span data-ttu-id="6847b-158">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="6847b-158">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="6847b-159">Une correspondance exacte n’a pas été trouvée pendant une recherche.</span><span class="sxs-lookup"><span data-stu-id="6847b-159">An exact match was not found during a seek.</span></span> <span data-ttu-id="6847b-160">Cette erreur est retournée par le gestionnaire d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6847b-160">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-161">JET_wrnRecordFoundLess</span><span class="sxs-lookup"><span data-stu-id="6847b-161">JET_wrnRecordFoundLess</span></span><br />
<span data-ttu-id="6847b-162">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="6847b-162">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="6847b-163">Une correspondance exacte n’a pas été trouvée pendant une recherche.</span><span class="sxs-lookup"><span data-stu-id="6847b-163">An exact match was not found during a seek.</span></span> <span data-ttu-id="6847b-164">Cette erreur est retournée par le gestionnaire d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6847b-164">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-165">JET_wrnNoErrorInfo</span><span class="sxs-lookup"><span data-stu-id="6847b-165">JET_wrnNoErrorInfo</span></span><br />
<span data-ttu-id="6847b-166">1055</span><span class="sxs-lookup"><span data-stu-id="6847b-166">1055</span></span></p></td>
<td><p><span data-ttu-id="6847b-167">Il n’y a pas d’informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="6847b-167">There is no extended error information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-168">JET_wrnNoIdleActivity</span><span class="sxs-lookup"><span data-stu-id="6847b-168">JET_wrnNoIdleActivity</span></span><br />
<span data-ttu-id="6847b-169">1058</span><span class="sxs-lookup"><span data-stu-id="6847b-169">1058</span></span></p></td>
<td><p><span data-ttu-id="6847b-170">Aucune activité inactive ne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6847b-170">No idle activity occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-171">JET_wrnNoWriteLock</span><span class="sxs-lookup"><span data-stu-id="6847b-171">JET_wrnNoWriteLock</span></span><br />
<span data-ttu-id="6847b-172">1067</span><span class="sxs-lookup"><span data-stu-id="6847b-172">1067</span></span></p></td>
<td><p><span data-ttu-id="6847b-173">Il n’existe aucun verrou d’écriture au niveau de la transaction 0.</span><span class="sxs-lookup"><span data-stu-id="6847b-173">There is a no write lock at transaction level 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-174">JET_wrnColumnSetNull</span><span class="sxs-lookup"><span data-stu-id="6847b-174">JET_wrnColumnSetNull</span></span><br />
<span data-ttu-id="6847b-175">1068</span><span class="sxs-lookup"><span data-stu-id="6847b-175">1068</span></span></p></td>
<td><p><span data-ttu-id="6847b-176">La colonne est définie sur une valeur <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="6847b-176">The column is set to a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-177">JET_wrnTableEmpty</span><span class="sxs-lookup"><span data-stu-id="6847b-177">JET_wrnTableEmpty</span></span><br />
<span data-ttu-id="6847b-178">1301</span><span class="sxs-lookup"><span data-stu-id="6847b-178">1301</span></span></p></td>
<td><p><span data-ttu-id="6847b-179">Une table vide a été ouverte.</span><span class="sxs-lookup"><span data-stu-id="6847b-179">An empty table was opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-180">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="6847b-180">JET_wrnTableInUseBySystem</span></span><br />
<span data-ttu-id="6847b-181">1327</span><span class="sxs-lookup"><span data-stu-id="6847b-181">1327</span></span></p></td>
<td><p><span data-ttu-id="6847b-182">Le nettoyage du système a un curseur ouvert sur la table.</span><span class="sxs-lookup"><span data-stu-id="6847b-182">The system cleanup has a cursor open on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-183">JET_wrnCorruptIndexDeleted</span><span class="sxs-lookup"><span data-stu-id="6847b-183">JET_wrnCorruptIndexDeleted</span></span><br />
<span data-ttu-id="6847b-184">1415</span><span class="sxs-lookup"><span data-stu-id="6847b-184">1415</span></span></p></td>
<td><p><span data-ttu-id="6847b-185">L’index obsolète doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="6847b-185">The out-of-date index must be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-186">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="6847b-186">JET_wrnColumnMaxTruncated</span></span><br />
<span data-ttu-id="6847b-187">1512</span><span class="sxs-lookup"><span data-stu-id="6847b-187">1512</span></span></p></td>
<td><p><span data-ttu-id="6847b-188">La longueur maximale est trop grande et a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="6847b-188">The Max length is too large and has been truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-189">JET_wrnCopyLongValue</span><span class="sxs-lookup"><span data-stu-id="6847b-189">JET_wrnCopyLongValue</span></span><br />
<span data-ttu-id="6847b-190">1520</span><span class="sxs-lookup"><span data-stu-id="6847b-190">1520</span></span></p></td>
<td><p><span data-ttu-id="6847b-191">Une valeur d’objet BLOB a été déplacée de l’enregistrement dans un stockage distinct d’objets BLOB volumineux.</span><span class="sxs-lookup"><span data-stu-id="6847b-191">A BLOB value has been moved from the record into a separate storage of large BLOBs.</span></span></p>
<p><span data-ttu-id="6847b-192"><strong>Remarque</strong> Cette erreur est réservée à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="6847b-192"><strong>Note</strong> This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-193">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="6847b-193">JET_wrnColumnSkipped</span></span><br />
<span data-ttu-id="6847b-194">1531</span><span class="sxs-lookup"><span data-stu-id="6847b-194">1531</span></span></p></td>
<td><p><span data-ttu-id="6847b-195">Les valeurs de colonne n’ont pas été retournées, car l’ID de colonne ou le membre <em>itagSequence</em> correspondant de la structure <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> qui a été demandée pour l’énumération a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="6847b-195">The column values were not returned because the corresponding column ID or <em>itagSequence</em> member from the <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> structure that was requested for enumeration was null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-196">JET_wrnColumnNotLocal</span><span class="sxs-lookup"><span data-stu-id="6847b-196">JET_wrnColumnNotLocal</span></span><br />
<span data-ttu-id="6847b-197">1532</span><span class="sxs-lookup"><span data-stu-id="6847b-197">1532</span></span></p></td>
<td><p><span data-ttu-id="6847b-198">Les valeurs de colonne n’ont pas été retournées, car elles n’ont pas pu être reconstruites à partir des données existantes.</span><span class="sxs-lookup"><span data-stu-id="6847b-198">The column values were not returned because they could not be reconstructed from the existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-199">JET_wrnColumnMoreTags</span><span class="sxs-lookup"><span data-stu-id="6847b-199">JET_wrnColumnMoreTags</span></span><br />
<span data-ttu-id="6847b-200">1533</span><span class="sxs-lookup"><span data-stu-id="6847b-200">1533</span></span></p></td>
<td><p><span data-ttu-id="6847b-201">Les valeurs de colonne existantes n’ont pas été demandées pour l’énumération.</span><span class="sxs-lookup"><span data-stu-id="6847b-201">The existing column values were not requested for enumeration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-202">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="6847b-202">JET_wrnColumnTruncated</span></span><br />
<span data-ttu-id="6847b-203">1534</span><span class="sxs-lookup"><span data-stu-id="6847b-203">1534</span></span></p></td>
<td><p><span data-ttu-id="6847b-204">La valeur de colonne a été tronquée à la limite de taille demandée pendant l’énumération.</span><span class="sxs-lookup"><span data-stu-id="6847b-204">The column value was truncated at the requested size limit during enumeration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-205">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="6847b-205">JET_wrnColumnPresent</span></span><br />
<span data-ttu-id="6847b-206">1535</span><span class="sxs-lookup"><span data-stu-id="6847b-206">1535</span></span></p></td>
<td><p><span data-ttu-id="6847b-207">Les valeurs de colonne existent mais n’ont pas été retournées par la demande.</span><span class="sxs-lookup"><span data-stu-id="6847b-207">The column values exist but were not returned by the request.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-208">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="6847b-208">JET_wrnColumnSingleValue</span></span><br />
<span data-ttu-id="6847b-209">1536</span><span class="sxs-lookup"><span data-stu-id="6847b-209">1536</span></span></p></td>
<td><p><span data-ttu-id="6847b-210">La valeur de colonne a été retournée dans JET_COLUMNENUM à la suite de la définition de la JET_bitEnumerateCompressOutput.</span><span class="sxs-lookup"><span data-stu-id="6847b-210">The column value was returned in JET_COLUMNENUM as a result of the JET_bitEnumerateCompressOutput being set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-211">JET_wrnColumnDefault</span><span class="sxs-lookup"><span data-stu-id="6847b-211">JET_wrnColumnDefault</span></span><br />
<span data-ttu-id="6847b-212">1537</span><span class="sxs-lookup"><span data-stu-id="6847b-212">1537</span></span></p></td>
<td><p><span data-ttu-id="6847b-213">La valeur de la colonne est définie sur la valeur par défaut de la colonne.</span><span class="sxs-lookup"><span data-stu-id="6847b-213">The column value is set to the default value of the column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-214">JET_wrnDataHasChanged</span><span class="sxs-lookup"><span data-stu-id="6847b-214">JET_wrnDataHasChanged</span></span><br />
<span data-ttu-id="6847b-215">1610</span><span class="sxs-lookup"><span data-stu-id="6847b-215">1610</span></span></p></td>
<td><p><span data-ttu-id="6847b-216">Les données ont changé.</span><span class="sxs-lookup"><span data-stu-id="6847b-216">The data has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-217">JET_wrnKeyChanged</span><span class="sxs-lookup"><span data-stu-id="6847b-217">JET_wrnKeyChanged</span></span><br />
<span data-ttu-id="6847b-218">1618</span><span class="sxs-lookup"><span data-stu-id="6847b-218">1618</span></span></p></td>
<td><p><span data-ttu-id="6847b-219">Une nouvelle clé est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6847b-219">A new key is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-220">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="6847b-220">JET_wrnFileOpenReadOnly</span></span><br />
<span data-ttu-id="6847b-221">1813</span><span class="sxs-lookup"><span data-stu-id="6847b-221">1813</span></span></p></td>
<td><p><span data-ttu-id="6847b-222">Le fichier de base de données est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6847b-222">The database file is read only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-223">JET_wrnIdleFull</span><span class="sxs-lookup"><span data-stu-id="6847b-223">JET_wrnIdleFull</span></span><br />
<span data-ttu-id="6847b-224">1908</span><span class="sxs-lookup"><span data-stu-id="6847b-224">1908</span></span></p></td>
<td><p><span data-ttu-id="6847b-225">Le registre inactif est plein.</span><span class="sxs-lookup"><span data-stu-id="6847b-225">The idle registry is full.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-226">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="6847b-226">JET_wrnDefragAlreadyRunning</span></span><br />
<span data-ttu-id="6847b-227">2000</span><span class="sxs-lookup"><span data-stu-id="6847b-227">2000</span></span></p></td>
<td><p><span data-ttu-id="6847b-228">Une défragmentation en ligne est déjà en cours d’exécution sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6847b-228">There was an online defragmentation already running on the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-229">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="6847b-229">JET_wrnDefragNotRunning</span></span><br />
<span data-ttu-id="6847b-230">2001</span><span class="sxs-lookup"><span data-stu-id="6847b-230">2001</span></span></p></td>
<td><p><span data-ttu-id="6847b-231">Une défragmentation en ligne n’est pas en cours d’exécution sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6847b-231">An online defragmentation is not running on the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-232">JET_wrnCallbackNotRegistered</span><span class="sxs-lookup"><span data-stu-id="6847b-232">JET_wrnCallbackNotRegistered</span></span><br />
<span data-ttu-id="6847b-233">2100</span><span class="sxs-lookup"><span data-stu-id="6847b-233">2100</span></span></p></td>
<td><p><span data-ttu-id="6847b-234">Une fonction de rappel inexistante n’a pas été inscrite.</span><span class="sxs-lookup"><span data-stu-id="6847b-234">A non-existent callback function was unregistered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6847b-235">Une valeur [JET_ERR](./jet-err.md) inférieure à zéro doit être interprétée comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="6847b-235">A [JET_ERR](./jet-err.md) value that is less than zero should be interpreted as an error.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6847b-236">Erreurs</span><span class="sxs-lookup"><span data-stu-id="6847b-236">Errors</span></span></p></th>
<th><p><span data-ttu-id="6847b-237">Description</span><span class="sxs-lookup"><span data-stu-id="6847b-237">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6847b-238">JET_wrnNyi</span><span class="sxs-lookup"><span data-stu-id="6847b-238">JET_wrnNyi</span></span><br />
<span data-ttu-id="6847b-239">-1</span><span class="sxs-lookup"><span data-stu-id="6847b-239">-1</span></span></p></td>
<td><p><span data-ttu-id="6847b-240">La fonction n’est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="6847b-240">The function is not yet implemented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-241">JET_errRfsFailure</span><span class="sxs-lookup"><span data-stu-id="6847b-241">JET_errRfsFailure</span></span><br />
<span data-ttu-id="6847b-242">-100</span><span class="sxs-lookup"><span data-stu-id="6847b-242">-100</span></span></p></td>
<td><p><span data-ttu-id="6847b-243">Le simulateur d’échec de ressource a échoué.</span><span class="sxs-lookup"><span data-stu-id="6847b-243">The Resource Failure Simulator failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-244">JET_errRfsNotArmed</span><span class="sxs-lookup"><span data-stu-id="6847b-244">JET_errRfsNotArmed</span></span><br />
<span data-ttu-id="6847b-245">-101</span><span class="sxs-lookup"><span data-stu-id="6847b-245">-101</span></span></p></td>
<td><p><span data-ttu-id="6847b-246">Le simulateur d’échec de ressource n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="6847b-246">The Resource Failure Simulator has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-247">JET_errFileClose</span><span class="sxs-lookup"><span data-stu-id="6847b-247">JET_errFileClose</span></span><br />
<span data-ttu-id="6847b-248">-102</span><span class="sxs-lookup"><span data-stu-id="6847b-248">-102</span></span></p></td>
<td><p><span data-ttu-id="6847b-249">Impossible de fermer le fichier.</span><span class="sxs-lookup"><span data-stu-id="6847b-249">The file could not be closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-250">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="6847b-250">JET_errOutOfThreads</span></span><br />
<span data-ttu-id="6847b-251">-103</span><span class="sxs-lookup"><span data-stu-id="6847b-251">-103</span></span></p></td>
<td><p><span data-ttu-id="6847b-252">Le thread n’a pas pu être démarré.</span><span class="sxs-lookup"><span data-stu-id="6847b-252">The thread could not be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-253">JET_errTooManyIO</span><span class="sxs-lookup"><span data-stu-id="6847b-253">JET_errTooManyIO</span></span><br />
<span data-ttu-id="6847b-254">-105</span><span class="sxs-lookup"><span data-stu-id="6847b-254">-105</span></span></p></td>
<td><p><span data-ttu-id="6847b-255">Le système est occupé en raison d’un trop grand nombre d’IOs.</span><span class="sxs-lookup"><span data-stu-id="6847b-255">The system is busy due to too many IOs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-256">JET_errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="6847b-256">JET_errTaskDropped</span></span><br />
<span data-ttu-id="6847b-257">-106</span><span class="sxs-lookup"><span data-stu-id="6847b-257">-106</span></span></p></td>
<td><p><span data-ttu-id="6847b-258">Impossible d’exécuter la tâche asynchrone demandée.</span><span class="sxs-lookup"><span data-stu-id="6847b-258">The requested asynchronous task could not be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-259">JET_errInternalError</span><span class="sxs-lookup"><span data-stu-id="6847b-259">JET_errInternalError</span></span><br />
<span data-ttu-id="6847b-260">-107</span><span class="sxs-lookup"><span data-stu-id="6847b-260">-107</span></span></p></td>
<td><p><span data-ttu-id="6847b-261">Une erreur interne irrécupérable s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6847b-261">There was a fatal internal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-262">JET_errDatabaseBufferDependenciesCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-262">JET_errDatabaseBufferDependenciesCorrupted</span></span><br />
<span data-ttu-id="6847b-263">-255</span><span class="sxs-lookup"><span data-stu-id="6847b-263">-255</span></span></p></td>
<td><p><span data-ttu-id="6847b-264">Les dépendances de mémoire tampon ont été définies de manière incorrecte et un échec de récupération s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6847b-264">The buffer dependencies were set improperly and there was a recovery failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-265">JET_errPreviousVersion</span><span class="sxs-lookup"><span data-stu-id="6847b-265">JET_errPreviousVersion</span></span><br />
<span data-ttu-id="6847b-266">-322</span><span class="sxs-lookup"><span data-stu-id="6847b-266">-322</span></span></p></td>
<td><p><span data-ttu-id="6847b-267">La version existait déjà et un échec de récupération s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6847b-267">The version already existed and there was a recovery failure.</span></span> <span data-ttu-id="6847b-268">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-268">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-269">JET_errPageBoundary</span><span class="sxs-lookup"><span data-stu-id="6847b-269">JET_errPageBoundary</span></span><br />
<span data-ttu-id="6847b-270">-323</span><span class="sxs-lookup"><span data-stu-id="6847b-270">-323</span></span></p></td>
<td><p><span data-ttu-id="6847b-271">La limite de la page a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="6847b-271">The page boundary has been reached.</span></span> <span data-ttu-id="6847b-272">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-272">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-273">JET_errKeyBoundary</span><span class="sxs-lookup"><span data-stu-id="6847b-273">JET_errKeyBoundary</span></span><br />
<span data-ttu-id="6847b-274">-324</span><span class="sxs-lookup"><span data-stu-id="6847b-274">-324</span></span></p></td>
<td><p><span data-ttu-id="6847b-275">La limite de la clé a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="6847b-275">The key boundary has been reached.</span></span> <span data-ttu-id="6847b-276">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-276">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-277">JET_errBadPageLink</span><span class="sxs-lookup"><span data-stu-id="6847b-277">JET_errBadPageLink</span></span><br />
<span data-ttu-id="6847b-278">-327</span><span class="sxs-lookup"><span data-stu-id="6847b-278">-327</span></span></p></td>
<td><p><span data-ttu-id="6847b-279">La base de données est endommagée.</span><span class="sxs-lookup"><span data-stu-id="6847b-279">The database is corrupt.</span></span> <span data-ttu-id="6847b-280">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-280">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-281">JET_errBadBookmark</span><span class="sxs-lookup"><span data-stu-id="6847b-281">JET_errBadBookmark</span></span><br />
<span data-ttu-id="6847b-282">-328</span><span class="sxs-lookup"><span data-stu-id="6847b-282">-328</span></span></p></td>
<td><p><span data-ttu-id="6847b-283">Le signet n’a pas d’adresse correspondante dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-283">The bookmark has no corresponding address in the database.</span></span> <span data-ttu-id="6847b-284">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-284">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-285">JET_errNTSystemCallFailed</span><span class="sxs-lookup"><span data-stu-id="6847b-285">JET_errNTSystemCallFailed</span></span><br />
<span data-ttu-id="6847b-286">-334</span><span class="sxs-lookup"><span data-stu-id="6847b-286">-334</span></span></p></td>
<td><p><span data-ttu-id="6847b-287">L’appel au système d’exploitation a échoué.</span><span class="sxs-lookup"><span data-stu-id="6847b-287">The call to the operating system failed.</span></span> <span data-ttu-id="6847b-288">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-288">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-289">JET_errBadParentPageLink</span><span class="sxs-lookup"><span data-stu-id="6847b-289">JET_errBadParentPageLink</span></span><br />
<span data-ttu-id="6847b-290">-338</span><span class="sxs-lookup"><span data-stu-id="6847b-290">-338</span></span></p></td>
<td><p><span data-ttu-id="6847b-291">Une base de données parente est endommagée.</span><span class="sxs-lookup"><span data-stu-id="6847b-291">A parent database is corrupt.</span></span> <span data-ttu-id="6847b-292">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-292">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-293">JET_errSPAvailExtCacheOutOfSync</span><span class="sxs-lookup"><span data-stu-id="6847b-293">JET_errSPAvailExtCacheOutOfSync</span></span><br />
<span data-ttu-id="6847b-294">-340</span><span class="sxs-lookup"><span data-stu-id="6847b-294">-340</span></span></p></td>
<td><p><span data-ttu-id="6847b-295">Le cache AvailExt ne correspond pas à l’arborescence B +.</span><span class="sxs-lookup"><span data-stu-id="6847b-295">The AvailExt cache does not match the B+ tree.</span></span> <span data-ttu-id="6847b-296">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-296">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-297">JET_errSPAvailExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-297">JET_errSPAvailExtCorrupted</span></span><br />
<span data-ttu-id="6847b-298">-341</span><span class="sxs-lookup"><span data-stu-id="6847b-298">-341</span></span></p></td>
<td><p><span data-ttu-id="6847b-299">L’arborescence de l’espace AllAvailExt est endommagée.</span><span class="sxs-lookup"><span data-stu-id="6847b-299">The AllAvailExt space tree is corrupt.</span></span> <span data-ttu-id="6847b-300">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-300">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-301">JET_errSPAvailExtCacheOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6847b-301">JET_errSPAvailExtCacheOutOfMemory</span></span><br />
<span data-ttu-id="6847b-302">-342</span><span class="sxs-lookup"><span data-stu-id="6847b-302">-342</span></span></p></td>
<td><p><span data-ttu-id="6847b-303">Une erreur de mémoire insuffisante s’est produite lors de l’allocation d’un nœud de cache AvailExt.</span><span class="sxs-lookup"><span data-stu-id="6847b-303">An out of memory error occurred while allocating an AvailExt cache node.</span></span> <span data-ttu-id="6847b-304">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-304">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-305">JET_errSPOwnExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-305">JET_errSPOwnExtCorrupted</span></span><br />
<span data-ttu-id="6847b-306">-343</span><span class="sxs-lookup"><span data-stu-id="6847b-306">-343</span></span></p></td>
<td><p><span data-ttu-id="6847b-307">L’arborescence de l’espace OwnExt est endommagée.</span><span class="sxs-lookup"><span data-stu-id="6847b-307">The OwnExt space tree is corrupt.</span></span> <span data-ttu-id="6847b-308">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-308">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-309">JET_errDbTimeCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-309">JET_errDbTimeCorrupted</span></span><br />
<span data-ttu-id="6847b-310">-344</span><span class="sxs-lookup"><span data-stu-id="6847b-310">-344</span></span></p></td>
<td><p><span data-ttu-id="6847b-311">La valeur dbTime sur la page actuelle est supérieure à la valeur dbTime de la base de données globale.</span><span class="sxs-lookup"><span data-stu-id="6847b-311">The Dbtime on the current page is greater than the global database dbtime.</span></span> <span data-ttu-id="6847b-312">Cette erreur est retournée par le gestionnaire de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6847b-312">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-313">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="6847b-313">JET_errKeyTruncated</span></span><br />
<span data-ttu-id="6847b-314">-346</span><span class="sxs-lookup"><span data-stu-id="6847b-314">-346</span></span></p></td>
<td><p><span data-ttu-id="6847b-315">Une tentative de création d’une clé pour une entrée d’index a échoué, car la clé aurait été tronquée et la définition de l’index interdit la troncation de clé.</span><span class="sxs-lookup"><span data-stu-id="6847b-315">An attempt to create a key for an index entry failed because the key would have been truncated and the index definition disallows key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-316">JET_errKeyTooBig</span><span class="sxs-lookup"><span data-stu-id="6847b-316">JET_errKeyTooBig</span></span><br />
<span data-ttu-id="6847b-317">-408</span><span class="sxs-lookup"><span data-stu-id="6847b-317">-408</span></span></p></td>
<td><p><span data-ttu-id="6847b-318">La clé est trop grande.</span><span class="sxs-lookup"><span data-stu-id="6847b-318">The key is too large.</span></span> <span data-ttu-id="6847b-319">Cette erreur est retournée par le gestionnaire d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6847b-319">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-320">JET_errInvalidLoggedOperation</span><span class="sxs-lookup"><span data-stu-id="6847b-320">JET_errInvalidLoggedOperation</span></span><br />
<span data-ttu-id="6847b-321">-500</span><span class="sxs-lookup"><span data-stu-id="6847b-321">-500</span></span></p></td>
<td><p><span data-ttu-id="6847b-322">L’opération journalisée ne peut pas être rétablie.</span><span class="sxs-lookup"><span data-stu-id="6847b-322">The logged operation cannot be redone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-323">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="6847b-323">JET_errLogFileCorrupt</span></span><br />
<span data-ttu-id="6847b-324">-501</span><span class="sxs-lookup"><span data-stu-id="6847b-324">-501</span></span></p></td>
<td><p><span data-ttu-id="6847b-325">Le fichier journal est endommagé.</span><span class="sxs-lookup"><span data-stu-id="6847b-325">The log file is corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-326">JET_errNoBackupDirectory</span><span class="sxs-lookup"><span data-stu-id="6847b-326">JET_errNoBackupDirectory</span></span><br />
<span data-ttu-id="6847b-327">-503</span><span class="sxs-lookup"><span data-stu-id="6847b-327">-503</span></span></p></td>
<td><p><span data-ttu-id="6847b-328">Un répertoire de sauvegarde n’a pas été fourni.</span><span class="sxs-lookup"><span data-stu-id="6847b-328">A backup directory was not given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-329">JET_errBackupDirectoryNotEmpty</span><span class="sxs-lookup"><span data-stu-id="6847b-329">JET_errBackupDirectoryNotEmpty</span></span><br />
<span data-ttu-id="6847b-330">-504</span><span class="sxs-lookup"><span data-stu-id="6847b-330">-504</span></span></p></td>
<td><p><span data-ttu-id="6847b-331">Le répertoire de sauvegarde n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="6847b-331">The backup directory is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-332">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="6847b-332">JET_errBackupInProgress</span></span><br />
<span data-ttu-id="6847b-333">-505</span><span class="sxs-lookup"><span data-stu-id="6847b-333">-505</span></span></p></td>
<td><p><span data-ttu-id="6847b-334">La sauvegarde est déjà active.</span><span class="sxs-lookup"><span data-stu-id="6847b-334">The backup is active already.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-335">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6847b-335">JET_errRestoreInProgress</span></span><br />
<span data-ttu-id="6847b-336">-506</span><span class="sxs-lookup"><span data-stu-id="6847b-336">-506</span></span></p></td>
<td><p><span data-ttu-id="6847b-337">Une restauration est en cours.</span><span class="sxs-lookup"><span data-stu-id="6847b-337">A restore is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-338">JET_errMissingPreviousLogFile</span><span class="sxs-lookup"><span data-stu-id="6847b-338">JET_errMissingPreviousLogFile</span></span><br />
<span data-ttu-id="6847b-339">-509</span><span class="sxs-lookup"><span data-stu-id="6847b-339">-509</span></span></p></td>
<td><p><span data-ttu-id="6847b-340">Le fichier journal est manquant pour le point de vérification.</span><span class="sxs-lookup"><span data-stu-id="6847b-340">The log file is missing for the check point.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-341">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="6847b-341">JET_errLogWriteFail</span></span><br />
<span data-ttu-id="6847b-342">-510</span><span class="sxs-lookup"><span data-stu-id="6847b-342">-510</span></span></p></td>
<td><p><span data-ttu-id="6847b-343">Une erreur s’est produite lors de l’écriture dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="6847b-343">There was a failure writing to the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-344">JET_errLogDisabledDueToRecoveryFailure</span><span class="sxs-lookup"><span data-stu-id="6847b-344">JET_errLogDisabledDueToRecoveryFailure</span></span><br />
<span data-ttu-id="6847b-345">-511</span><span class="sxs-lookup"><span data-stu-id="6847b-345">-511</span></span></p></td>
<td><p><span data-ttu-id="6847b-346">La tentative d’écriture dans le journal après la récupération a échoué.</span><span class="sxs-lookup"><span data-stu-id="6847b-346">The attempt to write to the log after recovery failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-347">JET_errCannotLogDuringRecoveryRedo</span><span class="sxs-lookup"><span data-stu-id="6847b-347">JET_errCannotLogDuringRecoveryRedo</span></span><br />
<span data-ttu-id="6847b-348">-512</span><span class="sxs-lookup"><span data-stu-id="6847b-348">-512</span></span></p></td>
<td><p><span data-ttu-id="6847b-349">La tentative d’écriture dans le journal pendant le rétablissement de la récupération a échoué.</span><span class="sxs-lookup"><span data-stu-id="6847b-349">The attempt to write to the log during the recovery redo failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-350">JET_errLogGenerationMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-350">JET_errLogGenerationMismatch</span></span><br />
<span data-ttu-id="6847b-351">-513</span><span class="sxs-lookup"><span data-stu-id="6847b-351">-513</span></span></p></td>
<td><p><span data-ttu-id="6847b-352">Le nom du fichier journal ne correspond pas au numéro de génération interne.</span><span class="sxs-lookup"><span data-stu-id="6847b-352">The name of of the log file does not match the internal generation number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-353">JET_errBadLogVersion</span><span class="sxs-lookup"><span data-stu-id="6847b-353">JET_errBadLogVersion</span></span><br />
<span data-ttu-id="6847b-354">-514</span><span class="sxs-lookup"><span data-stu-id="6847b-354">-514</span></span></p></td>
<td><p><span data-ttu-id="6847b-355">La version du fichier journal n’est pas compatible avec la version ESE.</span><span class="sxs-lookup"><span data-stu-id="6847b-355">The version of the log file is not compatible with the ESE version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-356">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="6847b-356">JET_errInvalidLogSequence</span></span><br />
<span data-ttu-id="6847b-357">-515</span><span class="sxs-lookup"><span data-stu-id="6847b-357">-515</span></span></p></td>
<td><p><span data-ttu-id="6847b-358">L’horodateur dans le journal suivant ne correspond pas à l’horodatage attendu.</span><span class="sxs-lookup"><span data-stu-id="6847b-358">The timestamp in the next log does not match the expected timestamp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-359">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="6847b-359">JET_errLoggingDisabled</span></span><br />
<span data-ttu-id="6847b-360">-516</span><span class="sxs-lookup"><span data-stu-id="6847b-360">-516</span></span></p></td>
<td><p><span data-ttu-id="6847b-361">Le journal n’est pas actif.</span><span class="sxs-lookup"><span data-stu-id="6847b-361">The log is not active.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-362">JET_errLogBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="6847b-362">JET_errLogBufferTooSmall</span></span><br />
<span data-ttu-id="6847b-363">-517</span><span class="sxs-lookup"><span data-stu-id="6847b-363">-517</span></span></p></td>
<td><p><span data-ttu-id="6847b-364">Le tampon du journal est trop petit pour la récupération.</span><span class="sxs-lookup"><span data-stu-id="6847b-364">The log buffer is too small for recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-365">JET_errLogSequenceEnd</span><span class="sxs-lookup"><span data-stu-id="6847b-365">JET_errLogSequenceEnd</span></span><br />
<span data-ttu-id="6847b-366">-519</span><span class="sxs-lookup"><span data-stu-id="6847b-366">-519</span></span></p></td>
<td><p><span data-ttu-id="6847b-367">Le nombre maximal de fichiers journaux a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="6847b-367">The maximum log file number has been exceeded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-368">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="6847b-368">JET_errNoBackup</span></span><br />
<span data-ttu-id="6847b-369">-520</span><span class="sxs-lookup"><span data-stu-id="6847b-369">-520</span></span></p></td>
<td><p><span data-ttu-id="6847b-370">Aucune sauvegarde n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="6847b-370">There is no backup in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-371">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="6847b-371">JET_errInvalidBackupSequence</span></span><br />
<span data-ttu-id="6847b-372">-521</span><span class="sxs-lookup"><span data-stu-id="6847b-372">-521</span></span></p></td>
<td><p><span data-ttu-id="6847b-373">L’appel de sauvegarde est hors séquence.</span><span class="sxs-lookup"><span data-stu-id="6847b-373">The backup call is out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-374">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="6847b-374">JET_errBackupNotAllowedYet</span></span><br />
<span data-ttu-id="6847b-375">-523</span><span class="sxs-lookup"><span data-stu-id="6847b-375">-523</span></span></p></td>
<td><p><span data-ttu-id="6847b-376">Une sauvegarde ne peut pas être effectuée pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="6847b-376">A backup cannot be done at this time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-377">JET_errDeleteBackupFileFail</span><span class="sxs-lookup"><span data-stu-id="6847b-377">JET_errDeleteBackupFileFail</span></span><br />
<span data-ttu-id="6847b-378">-524</span><span class="sxs-lookup"><span data-stu-id="6847b-378">-524</span></span></p></td>
<td><p><span data-ttu-id="6847b-379">Un fichier de sauvegarde n’a pas pu être supprimé.</span><span class="sxs-lookup"><span data-stu-id="6847b-379">A backup file could not be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-380">JET_errMakeBackupDirectoryFail</span><span class="sxs-lookup"><span data-stu-id="6847b-380">JET_errMakeBackupDirectoryFail</span></span><br />
<span data-ttu-id="6847b-381">-525</span><span class="sxs-lookup"><span data-stu-id="6847b-381">-525</span></span></p></td>
<td><p><span data-ttu-id="6847b-382">Impossible de créer le répertoire temporaire de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6847b-382">The backup temporary directory could not be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-383">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="6847b-383">JET_errInvalidBackup</span></span><br />
<span data-ttu-id="6847b-384">-526</span><span class="sxs-lookup"><span data-stu-id="6847b-384">-526</span></span></p></td>
<td><p><span data-ttu-id="6847b-385">La journalisation circulaire est activée ; Impossible d’effectuer une sauvegarde incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="6847b-385">Circular logging is enabled; an incremental backup cannot be performed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-386">JET_errRecoveredWithErrors</span><span class="sxs-lookup"><span data-stu-id="6847b-386">JET_errRecoveredWithErrors</span></span><br />
<span data-ttu-id="6847b-387">-527</span><span class="sxs-lookup"><span data-stu-id="6847b-387">-527</span></span></p></td>
<td><p><span data-ttu-id="6847b-388">Les données ont été restaurées avec des erreurs.</span><span class="sxs-lookup"><span data-stu-id="6847b-388">The data was restored with errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-389">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="6847b-389">JET_errMissingLogFile</span></span><br />
<span data-ttu-id="6847b-390">-528</span><span class="sxs-lookup"><span data-stu-id="6847b-390">-528</span></span></p></td>
<td><p><span data-ttu-id="6847b-391">Le fichier journal actuel est manquant.</span><span class="sxs-lookup"><span data-stu-id="6847b-391">The current log file is missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-392">JET_errLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="6847b-392">JET_errLogDiskFull</span></span><br />
<span data-ttu-id="6847b-393">-529</span><span class="sxs-lookup"><span data-stu-id="6847b-393">-529</span></span></p></td>
<td><p><span data-ttu-id="6847b-394">Le disque journal est saturé.</span><span class="sxs-lookup"><span data-stu-id="6847b-394">The log disk is full.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-395">JET_errBadLogSignature</span><span class="sxs-lookup"><span data-stu-id="6847b-395">JET_errBadLogSignature</span></span><br />
<span data-ttu-id="6847b-396">-530</span><span class="sxs-lookup"><span data-stu-id="6847b-396">-530</span></span></p></td>
<td><p><span data-ttu-id="6847b-397">La signature d’un fichier journal est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-397">There is a bad signature for a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-398">JET_errBadDbSignature</span><span class="sxs-lookup"><span data-stu-id="6847b-398">JET_errBadDbSignature</span></span><br />
<span data-ttu-id="6847b-399">-531</span><span class="sxs-lookup"><span data-stu-id="6847b-399">-531</span></span></p></td>
<td><p><span data-ttu-id="6847b-400">La signature d’un fichier de base de données est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-400">There is a bad signature for a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-401">JET_errBadCheckpointSignature</span><span class="sxs-lookup"><span data-stu-id="6847b-401">JET_errBadCheckpointSignature</span></span><br />
<span data-ttu-id="6847b-402">-532</span><span class="sxs-lookup"><span data-stu-id="6847b-402">-532</span></span></p></td>
<td><p><span data-ttu-id="6847b-403">La signature d’un fichier de point de contrôle est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-403">There is a bad signature for a checkpoint file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-404">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="6847b-404">JET_errCheckpointCorrupt</span></span><br />
<span data-ttu-id="6847b-405">-533</span><span class="sxs-lookup"><span data-stu-id="6847b-405">-533</span></span></p></td>
<td><p><span data-ttu-id="6847b-406">Le fichier de point de contrôle est introuvable ou endommagé.</span><span class="sxs-lookup"><span data-stu-id="6847b-406">The checkpoint file was not found or was corrupt.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-407">JET_errMissingPatchPage</span><span class="sxs-lookup"><span data-stu-id="6847b-407">JET_errMissingPatchPage</span></span><br />
<span data-ttu-id="6847b-408">-534</span><span class="sxs-lookup"><span data-stu-id="6847b-408">-534</span></span></p></td>
<td><p><span data-ttu-id="6847b-409">La page du fichier de correctif de base de données est introuvable lors de la récupération.</span><span class="sxs-lookup"><span data-stu-id="6847b-409">The database patch file page was not found during recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-410">JET_errBadPatchPage</span><span class="sxs-lookup"><span data-stu-id="6847b-410">JET_errBadPatchPage</span></span><br />
<span data-ttu-id="6847b-411">-535</span><span class="sxs-lookup"><span data-stu-id="6847b-411">-535</span></span></p></td>
<td><p><span data-ttu-id="6847b-412">La page du fichier de correctif de base de données n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-412">The database patch file page is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-413">JET_errRedoAbruptEnded</span><span class="sxs-lookup"><span data-stu-id="6847b-413">JET_errRedoAbruptEnded</span></span><br />
<span data-ttu-id="6847b-414">-536</span><span class="sxs-lookup"><span data-stu-id="6847b-414">-536</span></span></p></td>
<td><p><span data-ttu-id="6847b-415">Le rétablissement s’est soudainement arrêté en raison d’une défaillance soudaine lors de la lecture des journaux à partir du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="6847b-415">The redo abruptly ended due to a sudden failure while reading logs from the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-416">JET_errBadSLVSignature</span><span class="sxs-lookup"><span data-stu-id="6847b-416">JET_errBadSLVSignature</span></span><br />
<span data-ttu-id="6847b-417">-537</span><span class="sxs-lookup"><span data-stu-id="6847b-417">-537</span></span></p></td>
<td><p><span data-ttu-id="6847b-418">Cet indicateur est réservé.</span><span class="sxs-lookup"><span data-stu-id="6847b-418">This flag is reserved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-419">JET_errPatchFileMissing</span><span class="sxs-lookup"><span data-stu-id="6847b-419">JET_errPatchFileMissing</span></span><br />
<span data-ttu-id="6847b-420">-538</span><span class="sxs-lookup"><span data-stu-id="6847b-420">-538</span></span></p></td>
<td><p><span data-ttu-id="6847b-421">La restauration matérielle a détecté qu’un fichier correctif de base de données est manquant dans le jeu de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6847b-421">The hard restore detected that a database patch file is missing from the backup set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-422">JET_errDatabaseLogSetMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-422">JET_errDatabaseLogSetMismatch</span></span><br />
<span data-ttu-id="6847b-423">-539</span><span class="sxs-lookup"><span data-stu-id="6847b-423">-539</span></span></p></td>
<td><p><span data-ttu-id="6847b-424">La base de données n’appartient pas à l’ensemble actuel de fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="6847b-424">The database does not belong with the current set of log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-425">JET_errDatabaseStreamingFileMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-425">JET_errDatabaseStreamingFileMismatch</span></span><br />
<span data-ttu-id="6847b-426">-540</span><span class="sxs-lookup"><span data-stu-id="6847b-426">-540</span></span></p></td>
<td><p><span data-ttu-id="6847b-427">Cet indicateur est réservé.</span><span class="sxs-lookup"><span data-stu-id="6847b-427">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-428">JET_errLogFileSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-428">JET_errLogFileSizeMismatch</span></span><br />
<span data-ttu-id="6847b-429">-541</span><span class="sxs-lookup"><span data-stu-id="6847b-429">-541</span></span></p></td>
<td><p><span data-ttu-id="6847b-430">La taille réelle du fichier journal ne correspond pas à <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="6847b-430">The actual log file size does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-431">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="6847b-431">JET_errCheckpointFileNotFound</span></span><br />
<span data-ttu-id="6847b-432">-542</span><span class="sxs-lookup"><span data-stu-id="6847b-432">-542</span></span></p></td>
<td><p><span data-ttu-id="6847b-433">Le fichier de point de contrôle est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6847b-433">The checkpoint file could not be located.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-434">JET_errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="6847b-434">JET_errRequiredLogFilesMissing</span></span><br />
<span data-ttu-id="6847b-435">-543</span><span class="sxs-lookup"><span data-stu-id="6847b-435">-543</span></span></p></td>
<td><p><span data-ttu-id="6847b-436">Les fichiers journaux requis pour la récupération sont absents.</span><span class="sxs-lookup"><span data-stu-id="6847b-436">The required log files for recovery are missing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-437">JET_errSoftRecoveryOnBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="6847b-437">JET_errSoftRecoveryOnBackupDatabase</span></span><br />
<span data-ttu-id="6847b-438">-544</span><span class="sxs-lookup"><span data-stu-id="6847b-438">-544</span></span></p></td>
<td><p><span data-ttu-id="6847b-439">Une récupération logicielle va être utilisée sur une base de données de sauvegarde lorsqu’une restauration doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="6847b-439">A soft recovery is about to be used on a backup database when a restore should be used instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-440">JET_errLogFileSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="6847b-440">JET_errLogFileSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="6847b-441">-545</span><span class="sxs-lookup"><span data-stu-id="6847b-441">-545</span></span></p></td>
<td><p><span data-ttu-id="6847b-442">Les bases de données ont été récupérées, mais la taille du fichier journal utilisée lors de la récupération ne correspond pas à <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="6847b-442">The databases have been recovered, but the log file size used during recovery does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-443">JET_errLogSectorSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-443">JET_errLogSectorSizeMismatch</span></span><br />
<span data-ttu-id="6847b-444">-546</span><span class="sxs-lookup"><span data-stu-id="6847b-444">-546</span></span></p></td>
<td><p><span data-ttu-id="6847b-445">La taille des secteurs du fichier journal ne correspond pas à la taille des secteurs du volume actuel.</span><span class="sxs-lookup"><span data-stu-id="6847b-445">The log file sector size does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="6847b-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="6847b-447">-547</span><span class="sxs-lookup"><span data-stu-id="6847b-447">-547</span></span></p></td>
<td><p><span data-ttu-id="6847b-448">Les bases de données ont été récupérées, mais la taille des secteurs du fichier journal (utilisée lors de la récupération) ne correspond pas à la taille des secteurs du volume actuel.</span><span class="sxs-lookup"><span data-stu-id="6847b-448">The databases have been recovered, but the log file sector size (used during recovery) does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-449">JET_errLogSequenceEndDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="6847b-449">JET_errLogSequenceEndDatabasesConsistent</span></span><br />
<span data-ttu-id="6847b-450">-548</span><span class="sxs-lookup"><span data-stu-id="6847b-450">-548</span></span></p></td>
<td><p><span data-ttu-id="6847b-451">Les bases de données ont été récupérées, mais toutes les générations de journaux possibles dans la séquence actuelle ont été utilisées.</span><span class="sxs-lookup"><span data-stu-id="6847b-451">The databases have been recovered, but all possible log generations in the current sequence have been used.</span></span> <span data-ttu-id="6847b-452">Tous les fichiers journaux et le fichier de point de contrôle doivent être supprimés et les bases de données doivent être sauvegardées avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="6847b-452">All log files and the checkpoint file must be deleted and databases must be backed up before continuing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-453">JET_errStreamingDataNotLogged</span><span class="sxs-lookup"><span data-stu-id="6847b-453">JET_errStreamingDataNotLogged</span></span><br />
<span data-ttu-id="6847b-454">-549</span><span class="sxs-lookup"><span data-stu-id="6847b-454">-549</span></span></p></td>
<td><p><span data-ttu-id="6847b-455">Une tentative illégale de relecture d’une opération de lecture de fichier de diffusion en continu a été effectuée, où les données n’étaient pas journalisées.</span><span class="sxs-lookup"><span data-stu-id="6847b-455">There was an illegal attempt to replay a streaming file operation where the data was not logged.</span></span> <span data-ttu-id="6847b-456">Cela est probablement dû à une tentative de restauration par progression avec la journalisation circulaire activée.</span><span class="sxs-lookup"><span data-stu-id="6847b-456">This is probably caused by an attempt to rollforward with circular logging enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-457">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="6847b-457">JET_errDatabaseDirtyShutdown</span></span><br />
<span data-ttu-id="6847b-458">-550</span><span class="sxs-lookup"><span data-stu-id="6847b-458">-550</span></span></p></td>
<td><p><span data-ttu-id="6847b-459">La base de données n’a pas été arrêtée correctement.</span><span class="sxs-lookup"><span data-stu-id="6847b-459">The database was not shutdown cleanly.</span></span> <span data-ttu-id="6847b-460">Une récupération doit d’abord être exécutée pour terminer correctement les opérations de base de données pour l’arrêt précédent.</span><span class="sxs-lookup"><span data-stu-id="6847b-460">A recovery must first be run to properly complete database operations for the previous shutdown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-461">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="6847b-461">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="6847b-462">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="6847b-462">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="6847b-463">Cette erreur est obsolète et a été remplacée par JET_errDatabaseDirtyShutdown.</span><span class="sxs-lookup"><span data-stu-id="6847b-463">This error is obsolete and has been replaced by JET_errDatabaseDirtyShutdown.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-464">JET_errConsistentTimeMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-464">JET_errConsistentTimeMismatch</span></span><br />
<span data-ttu-id="6847b-465">-551</span><span class="sxs-lookup"><span data-stu-id="6847b-465">-551</span></span></p></td>
<td><p><span data-ttu-id="6847b-466">L’heure de la dernière cohérence pour la base de données n’a pas été mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="6847b-466">The last consistent time for the database has not been matched.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-467">JET_errDatabasePatchFileMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-467">JET_errDatabasePatchFileMismatch</span></span><br />
<span data-ttu-id="6847b-468">-552</span><span class="sxs-lookup"><span data-stu-id="6847b-468">-552</span></span></p></td>
<td><p><span data-ttu-id="6847b-469">Le fichier de correctif de base de données n’est pas généré à partir de cette sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6847b-469">The database patch file is not generated from this backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-470">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="6847b-470">JET_errEndingRestoreLogTooLow</span></span><br />
<span data-ttu-id="6847b-471">-553</span><span class="sxs-lookup"><span data-stu-id="6847b-471">-553</span></span></p></td>
<td><p><span data-ttu-id="6847b-472">Le numéro de journal de début est trop faible pour la restauration.</span><span class="sxs-lookup"><span data-stu-id="6847b-472">The starting log number is too low for the restore.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-473">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="6847b-473">JET_errStartingRestoreLogTooHigh</span></span><br />
<span data-ttu-id="6847b-474">-554</span><span class="sxs-lookup"><span data-stu-id="6847b-474">-554</span></span></p></td>
<td><p><span data-ttu-id="6847b-475">Le numéro de journal de début est trop élevé pour la restauration.</span><span class="sxs-lookup"><span data-stu-id="6847b-475">The starting log number is too high for the restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-476">JET_errGivenLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="6847b-476">JET_errGivenLogFileHasBadSignature</span></span><br />
<span data-ttu-id="6847b-477">-555</span><span class="sxs-lookup"><span data-stu-id="6847b-477">-555</span></span></p></td>
<td><p><span data-ttu-id="6847b-478">La signature du fichier journal de restauration est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-478">The restore log file has a bad signature.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-479">JET_errGivenLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="6847b-479">JET_errGivenLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="6847b-480">-556</span><span class="sxs-lookup"><span data-stu-id="6847b-480">-556</span></span></p></td>
<td><p><span data-ttu-id="6847b-481">Le fichier journal de restauration n’est pas contigu.</span><span class="sxs-lookup"><span data-stu-id="6847b-481">The restore log file is not contiguous.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-482">JET_errMissingRestoreLogFiles</span><span class="sxs-lookup"><span data-stu-id="6847b-482">JET_errMissingRestoreLogFiles</span></span><br />
<span data-ttu-id="6847b-483">-557</span><span class="sxs-lookup"><span data-stu-id="6847b-483">-557</span></span></p></td>
<td><p><span data-ttu-id="6847b-484">Certains fichiers journaux de restauration sont manquants.</span><span class="sxs-lookup"><span data-stu-id="6847b-484">Some restore log files are missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-485">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="6847b-485">JET_errMissingFullBackup</span></span><br />
<span data-ttu-id="6847b-486">-560</span><span class="sxs-lookup"><span data-stu-id="6847b-486">-560</span></span></p></td>
<td><p><span data-ttu-id="6847b-487">La base de données a manqué une sauvegarde complète précédente avant de tenter d’effectuer une sauvegarde incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="6847b-487">The database missed a previous full backup before attempting to perform an incremental backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-488">JET_errBadBackupDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="6847b-488">JET_errBadBackupDatabaseSize</span></span><br />
<span data-ttu-id="6847b-489">-561</span><span class="sxs-lookup"><span data-stu-id="6847b-489">-561</span></span></p></td>
<td><p><span data-ttu-id="6847b-490">La taille de la base de données de sauvegarde n’est pas un multiple de la taille de la page de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-490">The backup database size is not a multiple of the database page size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-491">JET_errDatabaseAlreadyUpgraded</span><span class="sxs-lookup"><span data-stu-id="6847b-491">JET_errDatabaseAlreadyUpgraded</span></span><br />
<span data-ttu-id="6847b-492">-562</span><span class="sxs-lookup"><span data-stu-id="6847b-492">-562</span></span></p></td>
<td><p><span data-ttu-id="6847b-493">La tentative actuelle de mise à niveau d’une base de données a été arrêtée, car la base de données est déjà à jour.</span><span class="sxs-lookup"><span data-stu-id="6847b-493">The current attempt to upgrade a database has been stopped because the database is already current.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-494">JET_errDatabaseIncompleteUpgrade</span><span class="sxs-lookup"><span data-stu-id="6847b-494">JET_errDatabaseIncompleteUpgrade</span></span><br />
<span data-ttu-id="6847b-495">-563</span><span class="sxs-lookup"><span data-stu-id="6847b-495">-563</span></span></p></td>
<td><p><span data-ttu-id="6847b-496">La base de données n’a été convertie que partiellement au format actuel.</span><span class="sxs-lookup"><span data-stu-id="6847b-496">The database was only partially converted to the current format.</span></span> <span data-ttu-id="6847b-497">La base de données doit être restaurée à partir d’une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6847b-497">The database must be restored from backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-498">JET_errMissingCurrentLogFiles</span><span class="sxs-lookup"><span data-stu-id="6847b-498">JET_errMissingCurrentLogFiles</span></span><br />
<span data-ttu-id="6847b-499">-565</span><span class="sxs-lookup"><span data-stu-id="6847b-499">-565</span></span></p></td>
<td><p><span data-ttu-id="6847b-500">Certains fichiers journaux sont manquants pour la restauration continue.</span><span class="sxs-lookup"><span data-stu-id="6847b-500">Some current log files are missing for continuous restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-501">JET_errDbTimeTooOld</span><span class="sxs-lookup"><span data-stu-id="6847b-501">JET_errDbTimeTooOld</span></span><br />
<span data-ttu-id="6847b-502">-566</span><span class="sxs-lookup"><span data-stu-id="6847b-502">-566</span></span></p></td>
<td><p><span data-ttu-id="6847b-503">L’dbtime sur une page est plus petite que le dbtimeBefore dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6847b-503">The dbtime on a page is smaller than the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-504">JET_errDbTimeTooNew</span><span class="sxs-lookup"><span data-stu-id="6847b-504">JET_errDbTimeTooNew</span></span><br />
<span data-ttu-id="6847b-505">-567</span><span class="sxs-lookup"><span data-stu-id="6847b-505">-567</span></span></p></td>
<td><p><span data-ttu-id="6847b-506">L’dbtime sur une page est à l’avance du dbtimeBefore dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6847b-506">The dbtime on a page is in advance of the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-507">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="6847b-507">JET_errMissingFileToBackup</span></span><br />
<span data-ttu-id="6847b-508">-569</span><span class="sxs-lookup"><span data-stu-id="6847b-508">-569</span></span></p></td>
<td><p><span data-ttu-id="6847b-509">Certains fichiers de correctifs de base de données ou de journal étaient manquants pendant la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6847b-509">Some log or database patch files were missing during the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-510">JET_errLogTornWriteDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="6847b-510">JET_errLogTornWriteDuringHardRestore</span></span><br />
<span data-ttu-id="6847b-511">-570</span><span class="sxs-lookup"><span data-stu-id="6847b-511">-570</span></span></p></td>
<td><p><span data-ttu-id="6847b-512">Une écriture endommagée a été détectée dans une sauvegarde qui a été définie lors d’une restauration matérielle.</span><span class="sxs-lookup"><span data-stu-id="6847b-512">A torn write was detected in a backup that was set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-513">JET_errLogTornWriteDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="6847b-513">JET_errLogTornWriteDuringHardRecovery</span></span><br />
<span data-ttu-id="6847b-514">-571</span><span class="sxs-lookup"><span data-stu-id="6847b-514">-571</span></span></p></td>
<td><p><span data-ttu-id="6847b-515">Une écriture endommagée a été détectée lors d’une récupération matérielle (le journal ne fait pas partie d’un jeu de sauvegarde).</span><span class="sxs-lookup"><span data-stu-id="6847b-515">A torn write was detected during a hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-516">JET_errLogCorruptDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="6847b-516">JET_errLogCorruptDuringHardRestore</span></span><br />
<span data-ttu-id="6847b-517">-573</span><span class="sxs-lookup"><span data-stu-id="6847b-517">-573</span></span></p></td>
<td><p><span data-ttu-id="6847b-518">Une altération a été détectée dans un jeu de sauvegarde lors d’une restauration matérielle.</span><span class="sxs-lookup"><span data-stu-id="6847b-518">Corruption was detected in a backup set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-519">JET_errLogCorruptDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="6847b-519">JET_errLogCorruptDuringHardRecovery</span></span><br />
<span data-ttu-id="6847b-520">-574</span><span class="sxs-lookup"><span data-stu-id="6847b-520">-574</span></span></p></td>
<td><p><span data-ttu-id="6847b-521">Une altération a été détectée pendant la récupération matérielle (le journal ne fait pas partie d’un jeu de sauvegarde).</span><span class="sxs-lookup"><span data-stu-id="6847b-521">Corruption was detected during hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-522">JET_errMustDisableLoggingForDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="6847b-522">JET_errMustDisableLoggingForDbUpgrade</span></span><br />
<span data-ttu-id="6847b-523">-575</span><span class="sxs-lookup"><span data-stu-id="6847b-523">-575</span></span></p></td>
<td><p><span data-ttu-id="6847b-524">Impossible d’activer la journalisation lors de la tentative de mise à niveau d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-524">Logging cannot be enabled while attempting to upgrade a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-525">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="6847b-525">JET_errBadRestoreTargetInstance</span></span><br />
<span data-ttu-id="6847b-526">-577</span><span class="sxs-lookup"><span data-stu-id="6847b-526">-577</span></span></p></td>
<td><p><span data-ttu-id="6847b-527">Le TargetInstance spécifié pour la restauration n’a pas été trouvé ou les fichiers journaux ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="6847b-527">Either the TargetInstance that was specified for restore has not been found or the log files do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-528">JET_errRecoveredWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="6847b-528">JET_errRecoveredWithoutUndo</span></span><br />
<span data-ttu-id="6847b-529">-579</span><span class="sxs-lookup"><span data-stu-id="6847b-529">-579</span></span></p></td>
<td><p><span data-ttu-id="6847b-530">Le moteur de base de données a relu toutes les opérations du journal des transactions pour effectuer une récupération après incident, mais l’appelant a choisi d’arrêter la récupération sans restaurer les mises à jour non validées.</span><span class="sxs-lookup"><span data-stu-id="6847b-530">The database engine successfully replayed all operations in the transaction log to perform a crash recovery but the caller elected to stop recovery without rolling back uncommitted updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-531">JET_errDatabasesNotFromSameSnapshot</span><span class="sxs-lookup"><span data-stu-id="6847b-531">JET_errDatabasesNotFromSameSnapshot</span></span><br />
<span data-ttu-id="6847b-532">-580</span><span class="sxs-lookup"><span data-stu-id="6847b-532">-580</span></span></p></td>
<td><p><span data-ttu-id="6847b-533">Les bases de données à restaurer ne proviennent pas de la même sauvegarde de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="6847b-533">The databases to be restored are not from the same shadow copy backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-534">JET_errSoftRecoveryOnSnapshot</span><span class="sxs-lookup"><span data-stu-id="6847b-534">JET_errSoftRecoveryOnSnapshot</span></span><br />
<span data-ttu-id="6847b-535">-581</span><span class="sxs-lookup"><span data-stu-id="6847b-535">-581</span></span></p></td>
<td><p><span data-ttu-id="6847b-536">Il existe une récupération logicielle sur une base de données à partir d’un jeu de sauvegarde de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="6847b-536">There is a soft recovery on a database from a shadow copy backup set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-537">JET_errUnicodeTranslationBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="6847b-537">JET_errUnicodeTranslationBufferTooSmall</span></span><br />
<span data-ttu-id="6847b-538">-601</span><span class="sxs-lookup"><span data-stu-id="6847b-538">-601</span></span></p></td>
<td><p><span data-ttu-id="6847b-539">La mémoire tampon de traduction Unicode est trop petite.</span><span class="sxs-lookup"><span data-stu-id="6847b-539">The Unicode translation buffer is too small.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-540">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="6847b-540">JET_errUnicodeTranslationFail</span></span><br />
<span data-ttu-id="6847b-541">-602</span><span class="sxs-lookup"><span data-stu-id="6847b-541">-602</span></span></p></td>
<td><p><span data-ttu-id="6847b-542">Échec de la normalisation Unicode.</span><span class="sxs-lookup"><span data-stu-id="6847b-542">The Unicode normalization failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-543">JET_errUnicodeNormalizationNotSupported</span><span class="sxs-lookup"><span data-stu-id="6847b-543">JET_errUnicodeNormalizationNotSupported</span></span><br />
<span data-ttu-id="6847b-544">-603</span><span class="sxs-lookup"><span data-stu-id="6847b-544">-603</span></span></p></td>
<td><p><span data-ttu-id="6847b-545">Le système d’exploitation ne prend pas en charge la normalisation Unicode et aucun rappel de normalisation n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="6847b-545">The operating system does not provide support for Unicode normalization and a normalization callback was not specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-546">JET_errExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="6847b-546">JET_errExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="6847b-547">-610</span><span class="sxs-lookup"><span data-stu-id="6847b-547">-610</span></span></p></td>
<td><p><span data-ttu-id="6847b-548">La signature du fichier journal existant est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-548">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-549">JET_errExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="6847b-549">JET_errExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="6847b-550">-611</span><span class="sxs-lookup"><span data-stu-id="6847b-550">-611</span></span></p></td>
<td><p><span data-ttu-id="6847b-551">Un fichier journal existant n’est pas contigu.</span><span class="sxs-lookup"><span data-stu-id="6847b-551">An existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-552">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="6847b-552">JET_errLogReadVerifyFailure</span></span><br />
<span data-ttu-id="6847b-553">-612</span><span class="sxs-lookup"><span data-stu-id="6847b-553">-612</span></span></p></td>
<td><p><span data-ttu-id="6847b-554">Une erreur de somme de contrôle a été trouvée dans le fichier journal lors de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6847b-554">A checksum error was found in the log file during backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-555">JET_errSLVReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="6847b-555">JET_errSLVReadVerifyFailure</span></span><br />
<span data-ttu-id="6847b-556">-613</span><span class="sxs-lookup"><span data-stu-id="6847b-556">-613</span></span></p></td>
<td><p><span data-ttu-id="6847b-557">Cet indicateur est réservé.</span><span class="sxs-lookup"><span data-stu-id="6847b-557">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-558">JET_errCheckpointDepthTooDeep</span><span class="sxs-lookup"><span data-stu-id="6847b-558">JET_errCheckpointDepthTooDeep</span></span><br />
<span data-ttu-id="6847b-559">-614</span><span class="sxs-lookup"><span data-stu-id="6847b-559">-614</span></span></p></td>
<td><p><span data-ttu-id="6847b-560">Il y a trop de générations en suspens entre le point de contrôle et la génération actuelle.</span><span class="sxs-lookup"><span data-stu-id="6847b-560">There are too many outstanding generations between the checkpoint and the current generation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-561">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="6847b-561">JET_errRestoreOfNonBackupDatabase</span></span><br />
<span data-ttu-id="6847b-562">-615</span><span class="sxs-lookup"><span data-stu-id="6847b-562">-615</span></span></p></td>
<td><p><span data-ttu-id="6847b-563">Une récupération matérielle a été tentée sur une base de données qui n’était pas une base de données de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6847b-563">A hard recovery was attempted on a database that was not a backup database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-564">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="6847b-564">JET_errInvalidGrbit</span></span><br />
<span data-ttu-id="6847b-565">-900</span><span class="sxs-lookup"><span data-stu-id="6847b-565">-900</span></span></p></td>
<td><p><span data-ttu-id="6847b-566">Un paramètre Grbit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-566">There is an invalid grbit parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-567">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6847b-567">JET_errTermInProgress</span></span><br />
<span data-ttu-id="6847b-568">-1 000</span><span class="sxs-lookup"><span data-stu-id="6847b-568">-1000</span></span></p></td>
<td><p><span data-ttu-id="6847b-569">Arrêt en cours.</span><span class="sxs-lookup"><span data-stu-id="6847b-569">Termination is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-570">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="6847b-570">JET_errFeatureNotAvailable</span></span><br />
<span data-ttu-id="6847b-571">-1001</span><span class="sxs-lookup"><span data-stu-id="6847b-571">-1001</span></span></p></td>
<td><p><span data-ttu-id="6847b-572">Cet élément d’API n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6847b-572">This API element is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-573">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="6847b-573">JET_errInvalidName</span></span><br />
<span data-ttu-id="6847b-574">-1002</span><span class="sxs-lookup"><span data-stu-id="6847b-574">-1002</span></span></p></td>
<td><p><span data-ttu-id="6847b-575">Un nom non valide est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6847b-575">An invalid name is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-576">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6847b-576">JET_errInvalidParameter</span></span><br />
<span data-ttu-id="6847b-577">-1003</span><span class="sxs-lookup"><span data-stu-id="6847b-577">-1003</span></span></p></td>
<td><p><span data-ttu-id="6847b-578">Un paramètre d’API non valide est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6847b-578">An invalid API parameter is being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-579">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="6847b-579">JET_errDatabaseFileReadOnly</span></span><br />
<span data-ttu-id="6847b-580">-1008</span><span class="sxs-lookup"><span data-stu-id="6847b-580">-1008</span></span></p></td>
<td><p><span data-ttu-id="6847b-581">Une tentative d’attachement à un fichier de base de données en lecture seule a été tentée pour les opérations de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6847b-581">There was an attempt to attach to a read-only database file for read/write operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-582">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="6847b-582">JET_errInvalidDatabaseId</span></span><br />
<span data-ttu-id="6847b-583">-1010</span><span class="sxs-lookup"><span data-stu-id="6847b-583">-1010</span></span></p></td>
<td><p><span data-ttu-id="6847b-584">Un ID de base de données n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-584">There is an invalid database ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-585">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6847b-585">JET_errOutOfMemory</span></span><br />
<span data-ttu-id="6847b-586">-1011</span><span class="sxs-lookup"><span data-stu-id="6847b-586">-1011</span></span></p></td>
<td><p><span data-ttu-id="6847b-587">La mémoire du système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6847b-587">The system is out of memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-588">JET_errOutOfDatabaseSpace</span><span class="sxs-lookup"><span data-stu-id="6847b-588">JET_errOutOfDatabaseSpace</span></span><br />
<span data-ttu-id="6847b-589">-1012</span><span class="sxs-lookup"><span data-stu-id="6847b-589">-1012</span></span></p></td>
<td><p><span data-ttu-id="6847b-590">La taille maximale de la base de données a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="6847b-590">The maximum database size has been reached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-591">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="6847b-591">JET_errOutOfCursors</span></span><br />
<span data-ttu-id="6847b-592">-1013</span><span class="sxs-lookup"><span data-stu-id="6847b-592">-1013</span></span></p></td>
<td><p><span data-ttu-id="6847b-593">La table est hors des curseurs.</span><span class="sxs-lookup"><span data-stu-id="6847b-593">The table is out of cursors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-594">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="6847b-594">JET_errOutOfBuffers</span></span><br />
<span data-ttu-id="6847b-595">-1014</span><span class="sxs-lookup"><span data-stu-id="6847b-595">-1014</span></span></p></td>
<td><p><span data-ttu-id="6847b-596">La base de données est en dehors des tampons de page.</span><span class="sxs-lookup"><span data-stu-id="6847b-596">The database is out of page buffers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-597">JET_errTooManyIndexes</span><span class="sxs-lookup"><span data-stu-id="6847b-597">JET_errTooManyIndexes</span></span><br />
<span data-ttu-id="6847b-598">-1015</span><span class="sxs-lookup"><span data-stu-id="6847b-598">-1015</span></span></p></td>
<td><p><span data-ttu-id="6847b-599">Le nombre d’index est trop important.</span><span class="sxs-lookup"><span data-stu-id="6847b-599">There are too many indexes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-600">JET_errTooManyKeys</span><span class="sxs-lookup"><span data-stu-id="6847b-600">JET_errTooManyKeys</span></span><br />
<span data-ttu-id="6847b-601">-1016</span><span class="sxs-lookup"><span data-stu-id="6847b-601">-1016</span></span></p></td>
<td><p><span data-ttu-id="6847b-602">Le nombre de colonnes dans un index est trop important.</span><span class="sxs-lookup"><span data-stu-id="6847b-602">There are too many columns in an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-603">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="6847b-603">JET_errRecordDeleted</span></span><br />
<span data-ttu-id="6847b-604">-1017</span><span class="sxs-lookup"><span data-stu-id="6847b-604">-1017</span></span></p></td>
<td><p><span data-ttu-id="6847b-605">L’enregistrement a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="6847b-605">The record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-606">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="6847b-606">JET_errReadVerifyFailure</span></span><br />
<span data-ttu-id="6847b-607">-1018</span><span class="sxs-lookup"><span data-stu-id="6847b-607">-1018</span></span></p></td>
<td><p><span data-ttu-id="6847b-608">Une page de base de données contient une erreur de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6847b-608">There is a checksum error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-609">JET_errPageNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6847b-609">JET_errPageNotInitialized</span></span><br />
<span data-ttu-id="6847b-610">-1019</span><span class="sxs-lookup"><span data-stu-id="6847b-610">-1019</span></span></p></td>
<td><p><span data-ttu-id="6847b-611">Il y a une page de base de données vide.</span><span class="sxs-lookup"><span data-stu-id="6847b-611">There is a blank database page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-612">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="6847b-612">JET_errOutOfFileHandles</span></span><br />
<span data-ttu-id="6847b-613">-1020</span><span class="sxs-lookup"><span data-stu-id="6847b-613">-1020</span></span></p></td>
<td><p><span data-ttu-id="6847b-614">Il n’y a aucun descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="6847b-614">There are no file handles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-615">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="6847b-615">JET_errDiskIO</span></span><br />
<span data-ttu-id="6847b-616">-1022</span><span class="sxs-lookup"><span data-stu-id="6847b-616">-1022</span></span></p></td>
<td><p><span data-ttu-id="6847b-617">Il y a une erreur d’e/s disque.</span><span class="sxs-lookup"><span data-stu-id="6847b-617">There is a disk IO error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-618">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6847b-618">JET_errInvalidPath</span></span><br />
<span data-ttu-id="6847b-619">-1023</span><span class="sxs-lookup"><span data-stu-id="6847b-619">-1023</span></span></p></td>
<td><p><span data-ttu-id="6847b-620">Un chemin d’accès au fichier n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-620">There is an invalid file path.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-621">JET_errInvalidSystemPath</span><span class="sxs-lookup"><span data-stu-id="6847b-621">JET_errInvalidSystemPath</span></span><br />
<span data-ttu-id="6847b-622">-1024</span><span class="sxs-lookup"><span data-stu-id="6847b-622">-1024</span></span></p></td>
<td><p><span data-ttu-id="6847b-623">Le chemin d’accès au système est incorrect.</span><span class="sxs-lookup"><span data-stu-id="6847b-623">There is an invalid system path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-624">JET_errInvalidLogDirectory</span><span class="sxs-lookup"><span data-stu-id="6847b-624">JET_errInvalidLogDirectory</span></span><br />
<span data-ttu-id="6847b-625">-1025</span><span class="sxs-lookup"><span data-stu-id="6847b-625">-1025</span></span></p></td>
<td><p><span data-ttu-id="6847b-626">Le répertoire de journal n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-626">There is an invalid log directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-627">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="6847b-627">JET_errRecordTooBig</span></span><br />
<span data-ttu-id="6847b-628">-1026</span><span class="sxs-lookup"><span data-stu-id="6847b-628">-1026</span></span></p></td>
<td><p><span data-ttu-id="6847b-629">L’enregistrement est plus grand que la taille maximale.</span><span class="sxs-lookup"><span data-stu-id="6847b-629">The record is larger than maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-630">JET_errTooManyOpenDatabases</span><span class="sxs-lookup"><span data-stu-id="6847b-630">JET_errTooManyOpenDatabases</span></span><br />
<span data-ttu-id="6847b-631">-1027</span><span class="sxs-lookup"><span data-stu-id="6847b-631">-1027</span></span></p></td>
<td><p><span data-ttu-id="6847b-632">Le nombre de bases de données ouvertes est trop important.</span><span class="sxs-lookup"><span data-stu-id="6847b-632">There are too many open databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-633">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="6847b-633">JET_errInvalidDatabase</span></span><br />
<span data-ttu-id="6847b-634">-1028</span><span class="sxs-lookup"><span data-stu-id="6847b-634">-1028</span></span></p></td>
<td><p><span data-ttu-id="6847b-635">Il ne s’agit pas d’un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-635">This is not a database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-636">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6847b-636">JET_errNotInitialized</span></span><br />
<span data-ttu-id="6847b-637">-1029</span><span class="sxs-lookup"><span data-stu-id="6847b-637">-1029</span></span></p></td>
<td><p><span data-ttu-id="6847b-638">Le moteur de base de données n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="6847b-638">The database engine has not been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-639">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="6847b-639">JET_errAlreadyInitialized</span></span><br />
<span data-ttu-id="6847b-640">-1030</span><span class="sxs-lookup"><span data-stu-id="6847b-640">-1030</span></span></p></td>
<td><p><span data-ttu-id="6847b-641">Le moteur de base de données est déjà initialisé.</span><span class="sxs-lookup"><span data-stu-id="6847b-641">The database engine is already initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-642">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="6847b-642">JET_errInitInProgress</span></span><br />
<span data-ttu-id="6847b-643">-1031</span><span class="sxs-lookup"><span data-stu-id="6847b-643">-1031</span></span></p></td>
<td><p><span data-ttu-id="6847b-644">Le moteur de base de données est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-644">The database engine is being initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-645">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="6847b-645">JET_errFileAccessDenied</span></span><br />
<span data-ttu-id="6847b-646">-1032</span><span class="sxs-lookup"><span data-stu-id="6847b-646">-1032</span></span></p></td>
<td><p><span data-ttu-id="6847b-647">Impossible d’accéder au fichier, car le fichier est verrouillé ou en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-647">The file cannot be accessed because the file is locked or in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-648">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="6847b-648">JET_errBufferTooSmall</span></span><br />
<span data-ttu-id="6847b-649">-1038</span><span class="sxs-lookup"><span data-stu-id="6847b-649">-1038</span></span></p></td>
<td><p><span data-ttu-id="6847b-650">La mémoire tampon est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6847b-650">The buffer is too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-651">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="6847b-651">JET_errTooManyColumns</span></span><br />
<span data-ttu-id="6847b-652">-1040</span><span class="sxs-lookup"><span data-stu-id="6847b-652">-1040</span></span></p></td>
<td><p><span data-ttu-id="6847b-653">Trop de colonnes sont définies.</span><span class="sxs-lookup"><span data-stu-id="6847b-653">Too many columns are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-654">JET_errContainerNotEmpty</span><span class="sxs-lookup"><span data-stu-id="6847b-654">JET_errContainerNotEmpty</span></span><br />
<span data-ttu-id="6847b-655">-1043</span><span class="sxs-lookup"><span data-stu-id="6847b-655">-1043</span></span></p></td>
<td><p><span data-ttu-id="6847b-656">Le conteneur n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="6847b-656">The container is not empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-657">JET_errInvalidFilename</span><span class="sxs-lookup"><span data-stu-id="6847b-657">JET_errInvalidFilename</span></span><br />
<span data-ttu-id="6847b-658">-1044</span><span class="sxs-lookup"><span data-stu-id="6847b-658">-1044</span></span></p></td>
<td><p><span data-ttu-id="6847b-659">Le nom de fichier n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-659">The filename is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-660">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="6847b-660">JET_errInvalidBookmark</span></span><br />
<span data-ttu-id="6847b-661">-1045</span><span class="sxs-lookup"><span data-stu-id="6847b-661">-1045</span></span></p></td>
<td><p><span data-ttu-id="6847b-662">Il y a un signet non valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-662">There is an invalid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-663">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-663">JET_errColumnInUse</span></span><br />
<span data-ttu-id="6847b-664">-1046</span><span class="sxs-lookup"><span data-stu-id="6847b-664">-1046</span></span></p></td>
<td><p><span data-ttu-id="6847b-665">La colonne utilisée se trouve dans un index.</span><span class="sxs-lookup"><span data-stu-id="6847b-665">The column used is in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-666">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="6847b-666">JET_errInvalidBufferSize</span></span><br />
<span data-ttu-id="6847b-667">-1047</span><span class="sxs-lookup"><span data-stu-id="6847b-667">-1047</span></span></p></td>
<td><p><span data-ttu-id="6847b-668">La mémoire tampon de données ne correspond pas à la taille de colonne.</span><span class="sxs-lookup"><span data-stu-id="6847b-668">The data buffer does not match the column size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-669">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="6847b-669">JET_errColumnNotUpdatable</span></span><br />
<span data-ttu-id="6847b-670">-1048</span><span class="sxs-lookup"><span data-stu-id="6847b-670">-1048</span></span></p></td>
<td><p><span data-ttu-id="6847b-671">La valeur de la colonne ne peut pas être définie.</span><span class="sxs-lookup"><span data-stu-id="6847b-671">The column value cannot be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-672">JET_errIndexInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-672">JET_errIndexInUse</span></span><br />
<span data-ttu-id="6847b-673">-1051</span><span class="sxs-lookup"><span data-stu-id="6847b-673">-1051</span></span></p></td>
<td><p><span data-ttu-id="6847b-674">L’index est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-674">The index is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-675">JET_errLinkNotSupported</span><span class="sxs-lookup"><span data-stu-id="6847b-675">JET_errLinkNotSupported</span></span><br />
<span data-ttu-id="6847b-676">-1052</span><span class="sxs-lookup"><span data-stu-id="6847b-676">-1052</span></span></p></td>
<td><p><span data-ttu-id="6847b-677">La prise en charge des liens n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="6847b-677">The link support is unavailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-678">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="6847b-678">JET_errNullKeyDisallowed</span></span><br />
<span data-ttu-id="6847b-679">-1053</span><span class="sxs-lookup"><span data-stu-id="6847b-679">-1053</span></span></p></td>
<td><p><span data-ttu-id="6847b-680">Les clés NULL ne sont pas autorisées sur un index.</span><span class="sxs-lookup"><span data-stu-id="6847b-680">Null keys are not allowed on an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-681">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="6847b-681">JET_errNotInTransaction</span></span><br />
<span data-ttu-id="6847b-682">-1054</span><span class="sxs-lookup"><span data-stu-id="6847b-682">-1054</span></span></p></td>
<td><p><span data-ttu-id="6847b-683">L’opération doit se produire dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="6847b-683">The operation must occur within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-684">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="6847b-684">JET_errTooManyActiveUsers</span></span><br />
<span data-ttu-id="6847b-685">-1059</span><span class="sxs-lookup"><span data-stu-id="6847b-685">-1059</span></span></p></td>
<td><p><span data-ttu-id="6847b-686">Le nombre d’utilisateurs de base de données actifs est trop important</span><span class="sxs-lookup"><span data-stu-id="6847b-686">There are too many active database users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-687">JET_errInvalidCountry</span><span class="sxs-lookup"><span data-stu-id="6847b-687">JET_errInvalidCountry</span></span><br />
<span data-ttu-id="6847b-688">-1061</span><span class="sxs-lookup"><span data-stu-id="6847b-688">-1061</span></span></p></td>
<td><p><span data-ttu-id="6847b-689">Code de pays non valide ou inconnu.</span><span class="sxs-lookup"><span data-stu-id="6847b-689">There is an invalid or unknown country code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-690">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="6847b-690">JET_errInvalidLanguageId</span></span><br />
<span data-ttu-id="6847b-691">-1062</span><span class="sxs-lookup"><span data-stu-id="6847b-691">-1062</span></span></p></td>
<td><p><span data-ttu-id="6847b-692">ID de langue non valide ou inconnu.</span><span class="sxs-lookup"><span data-stu-id="6847b-692">There is an invalid or unknown language ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-693">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="6847b-693">JET_errInvalidCodePage</span></span><br />
<span data-ttu-id="6847b-694">-1063</span><span class="sxs-lookup"><span data-stu-id="6847b-694">-1063</span></span></p></td>
<td><p><span data-ttu-id="6847b-695">Une page de codes n’est pas valide ou est inconnue.</span><span class="sxs-lookup"><span data-stu-id="6847b-695">There is an invalid or unknown code page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-696">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="6847b-696">JET_errInvalidLCMapStringFlags</span></span><br />
<span data-ttu-id="6847b-697">-1064</span><span class="sxs-lookup"><span data-stu-id="6847b-697">-1064</span></span></p></td>
<td><p><span data-ttu-id="6847b-698">Des indicateurs non valides sont utilisés pour <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span><span class="sxs-lookup"><span data-stu-id="6847b-698">There are invalid flags being used for <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-699">JET_errVersionStoreEntryTooBig</span><span class="sxs-lookup"><span data-stu-id="6847b-699">JET_errVersionStoreEntryTooBig</span></span><br />
<span data-ttu-id="6847b-700">-1065</span><span class="sxs-lookup"><span data-stu-id="6847b-700">-1065</span></span></p></td>
<td><p><span data-ttu-id="6847b-701">Une tentative de création d’une entrée de la Banque des versions (RCE) supérieure à celle d’un compartiment de version a été tentée.</span><span class="sxs-lookup"><span data-stu-id="6847b-701">There was an attempt to create a version store entry (RCE) that was larger than a version bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="6847b-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span></span><br />
<span data-ttu-id="6847b-703">-1066</span><span class="sxs-lookup"><span data-stu-id="6847b-703">-1066</span></span></p></td>
<td><p><span data-ttu-id="6847b-704">La Banque des versions ne dispose pas de suffisamment de mémoire et la tentative de nettoyage a échoué.</span><span class="sxs-lookup"><span data-stu-id="6847b-704">The version store is out of memory and the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-705">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6847b-705">JET_errVersionStoreOutOfMemory</span></span><br />
<span data-ttu-id="6847b-706">-1069</span><span class="sxs-lookup"><span data-stu-id="6847b-706">-1069</span></span></p></td>
<td><p><span data-ttu-id="6847b-707">La Banque des versions ne dispose pas de suffisamment de mémoire et une tentative de nettoyage a déjà été effectuée.</span><span class="sxs-lookup"><span data-stu-id="6847b-707">The version store is out of memory and a cleanup was already attempted).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-708">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="6847b-708">JET_errCannotIndex</span></span><br />
<span data-ttu-id="6847b-709">-1071</span><span class="sxs-lookup"><span data-stu-id="6847b-709">-1071</span></span></p></td>
<td><p><span data-ttu-id="6847b-710">Les colonnes tiers de confiance et SLV ne peuvent pas être indexées.</span><span class="sxs-lookup"><span data-stu-id="6847b-710">The escrow and SLV columns cannot be indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-711">JET_errRecordNotDeleted</span><span class="sxs-lookup"><span data-stu-id="6847b-711">JET_errRecordNotDeleted</span></span><br />
<span data-ttu-id="6847b-712">-1072</span><span class="sxs-lookup"><span data-stu-id="6847b-712">-1072</span></span></p></td>
<td><p><span data-ttu-id="6847b-713">L’enregistrement n’a pas été supprimé.</span><span class="sxs-lookup"><span data-stu-id="6847b-713">The record has not been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-714">JET_errTooManyMempoolEntries</span><span class="sxs-lookup"><span data-stu-id="6847b-714">JET_errTooManyMempoolEntries</span></span><br />
<span data-ttu-id="6847b-715">-1073</span><span class="sxs-lookup"><span data-stu-id="6847b-715">-1073</span></span></p></td>
<td><p><span data-ttu-id="6847b-716">Trop d’entrées mempool ont été demandées.</span><span class="sxs-lookup"><span data-stu-id="6847b-716">Too many mempool entries have been requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-717">JET_errOutOfObjectIDs</span><span class="sxs-lookup"><span data-stu-id="6847b-717">JET_errOutOfObjectIDs</span></span><br />
<span data-ttu-id="6847b-718">-1074</span><span class="sxs-lookup"><span data-stu-id="6847b-718">-1074</span></span></p></td>
<td><p><span data-ttu-id="6847b-719">La base de données est en dehors de l’arbre B + ObjectIDs, de sorte qu’une défragmentation hors connexion doit être effectuée pour récupérer des ObjectIds libérés ou inutilisés.</span><span class="sxs-lookup"><span data-stu-id="6847b-719">The database is out of B+ tree ObjectIDs so an offline defragmentation must be performed to reclaim freed or unused ObjectIds.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-720">JET_errOutOfLongValueIDs</span><span class="sxs-lookup"><span data-stu-id="6847b-720">JET_errOutOfLongValueIDs</span></span><br />
<span data-ttu-id="6847b-721">-1075</span><span class="sxs-lookup"><span data-stu-id="6847b-721">-1075</span></span></p></td>
<td><p><span data-ttu-id="6847b-722">Le compteur de l’ID de valeur long a atteint la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="6847b-722">The Long-value ID counter has reached the maximum value.</span></span> <span data-ttu-id="6847b-723">Une défragmentation hors connexion doit être effectuée pour récupérer des LongValueIDs libres ou inutilisés.</span><span class="sxs-lookup"><span data-stu-id="6847b-723">An offline defragmentation must be performed to reclaim free or unused LongValueIDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-724">JET_errOutOfAutoincrementValues</span><span class="sxs-lookup"><span data-stu-id="6847b-724">JET_errOutOfAutoincrementValues</span></span><br />
<span data-ttu-id="6847b-725">-1076</span><span class="sxs-lookup"><span data-stu-id="6847b-725">-1076</span></span></p></td>
<td><p><span data-ttu-id="6847b-726">Le compteur d’incrémentation automatique a atteint la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="6847b-726">The auto-increment counter has reached the maximum value.</span></span> <span data-ttu-id="6847b-727">Une défragmentation hors connexion ne sera pas en mesure de récupérer des valeurs d’incrémentation automatique libres ou inutilisées.</span><span class="sxs-lookup"><span data-stu-id="6847b-727">An offline defragmentation will not be able to reclaim free or unused auto-increment values).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-728">JET_errOutOfDbtimeValues</span><span class="sxs-lookup"><span data-stu-id="6847b-728">JET_errOutOfDbtimeValues</span></span><br />
<span data-ttu-id="6847b-729">-1077</span><span class="sxs-lookup"><span data-stu-id="6847b-729">-1077</span></span></p></td>
<td><p><span data-ttu-id="6847b-730">Le compteur dbtime a atteint la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="6847b-730">The Dbtime counter has reached the maximum value.</span></span> <span data-ttu-id="6847b-731">Une défragmentation hors connexion doit être effectuée pour récupérer des valeurs dbtime libres ou inutilisées.</span><span class="sxs-lookup"><span data-stu-id="6847b-731">An offline defragmentation must be performed to reclaim free or unused Dbtime values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-732">JET_errOutOfSequentialIndexValues</span><span class="sxs-lookup"><span data-stu-id="6847b-732">JET_errOutOfSequentialIndexValues</span></span><br />
<span data-ttu-id="6847b-733">-1078</span><span class="sxs-lookup"><span data-stu-id="6847b-733">-1078</span></span></p></td>
<td><p><span data-ttu-id="6847b-734">Un compteur d’index séquentiels a atteint la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="6847b-734">A sequential index counter has reached the maximum value.</span></span> <span data-ttu-id="6847b-735">Une défragmentation hors connexion doit être effectuée pour récupérer des valeurs SequentialIndex libres ou inutilisées.</span><span class="sxs-lookup"><span data-stu-id="6847b-735">An offline defragmentation must be performed to reclaim free or unused SequentialIndex values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-736">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6847b-736">JET_errRunningInOneInstanceMode</span></span><br />
<span data-ttu-id="6847b-737">-1080</span><span class="sxs-lookup"><span data-stu-id="6847b-737">-1080</span></span></p></td>
<td><p><span data-ttu-id="6847b-738">Le mode d’instance unique est activé pour cet appel multi-instance.</span><span class="sxs-lookup"><span data-stu-id="6847b-738">This multi-instance call has the single-instance mode enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-739">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6847b-739">JET_errRunningInMultiInstanceMode</span></span><br />
<span data-ttu-id="6847b-740">-1081</span><span class="sxs-lookup"><span data-stu-id="6847b-740">-1081</span></span></p></td>
<td><p><span data-ttu-id="6847b-741">L’appel à instance unique est activé pour le mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="6847b-741">This single-instance call has the multi-instance mode enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-742">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="6847b-742">JET_errSystemParamsAlreadySet</span></span><br />
<span data-ttu-id="6847b-743">-1082</span><span class="sxs-lookup"><span data-stu-id="6847b-743">-1082</span></span></p></td>
<td><p><span data-ttu-id="6847b-744">Les paramètres globaux du système ont déjà été définis.</span><span class="sxs-lookup"><span data-stu-id="6847b-744">The global system parameters have already been set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-745">JET_errSystemPathInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-745">JET_errSystemPathInUse</span></span><br />
<span data-ttu-id="6847b-746">-1083</span><span class="sxs-lookup"><span data-stu-id="6847b-746">-1083</span></span></p></td>
<td><p><span data-ttu-id="6847b-747">Le chemin d’accès système est déjà utilisé par une autre instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-747">The system path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-748">JET_errLogFilePathInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-748">JET_errLogFilePathInUse</span></span><br />
<span data-ttu-id="6847b-749">-1084</span><span class="sxs-lookup"><span data-stu-id="6847b-749">-1084</span></span></p></td>
<td><p><span data-ttu-id="6847b-750">Le chemin d’accès du fichier journal est déjà utilisé par une autre instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-750">The log file path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-751">JET_errTempPathInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-751">JET_errTempPathInUse</span></span><br />
<span data-ttu-id="6847b-752">-1085</span><span class="sxs-lookup"><span data-stu-id="6847b-752">-1085</span></span></p></td>
<td><p><span data-ttu-id="6847b-753">Le chemin d’accès à la base de données temporaire est déjà utilisé par une autre instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-753">The path to the temporary database is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-754">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-754">JET_errInstanceNameInUse</span></span><br />
<span data-ttu-id="6847b-755">-1086</span><span class="sxs-lookup"><span data-stu-id="6847b-755">-1086</span></span></p></td>
<td><p><span data-ttu-id="6847b-756">Le nom de l’instance est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="6847b-756">The instance name is already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-757">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6847b-757">JET_errInstanceUnavailable</span></span><br />
<span data-ttu-id="6847b-758">-1090</span><span class="sxs-lookup"><span data-stu-id="6847b-758">-1090</span></span></p></td>
<td><p><span data-ttu-id="6847b-759">Cette instance ne peut pas être utilisée car elle a rencontré une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="6847b-759">This instance cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-760">JET_errDatabaseUnavailable</span><span class="sxs-lookup"><span data-stu-id="6847b-760">JET_errDatabaseUnavailable</span></span><br />
<span data-ttu-id="6847b-761">-1091</span><span class="sxs-lookup"><span data-stu-id="6847b-761">-1091</span></span></p></td>
<td><p><span data-ttu-id="6847b-762">Impossible d’utiliser cette base de données, car elle a rencontré une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="6847b-762">This database cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="6847b-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span></span><br />
<span data-ttu-id="6847b-764">-1092</span><span class="sxs-lookup"><span data-stu-id="6847b-764">-1092</span></span></p></td>
<td><p><span data-ttu-id="6847b-765">Cette instance ne peut pas être utilisée car elle a rencontré une erreur log-Disk-Full lors de l’exécution d’une opération (par exemple, une restauration de transaction) qui n’a pas pu tolérer d’échec.</span><span class="sxs-lookup"><span data-stu-id="6847b-765">This instance cannot be used because it encountered a log-disk-full error while performing an operation (such as a transaction rollback) that could not tolerate failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-766">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="6847b-766">JET_errOutOfSessions</span></span><br />
<span data-ttu-id="6847b-767">-1101</span><span class="sxs-lookup"><span data-stu-id="6847b-767">-1101</span></span></p></td>
<td><p><span data-ttu-id="6847b-768">La base de données est en dehors des sessions.</span><span class="sxs-lookup"><span data-stu-id="6847b-768">The database is out of sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-769">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="6847b-769">JET_errWriteConflict</span></span><br />
<span data-ttu-id="6847b-770">-1102</span><span class="sxs-lookup"><span data-stu-id="6847b-770">-1102</span></span></p></td>
<td><p><span data-ttu-id="6847b-771">Le verrou d’écriture a échoué en raison de l’existence d’un verrou d’écriture en attente.</span><span class="sxs-lookup"><span data-stu-id="6847b-771">The write lock failed due to the existence of an outstanding write lock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-772">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="6847b-772">JET_errTransTooDeep</span></span><br />
<span data-ttu-id="6847b-773">-1103</span><span class="sxs-lookup"><span data-stu-id="6847b-773">-1103</span></span></p></td>
<td><p><span data-ttu-id="6847b-774">Les transactions sont imbriquées trop profondément.</span><span class="sxs-lookup"><span data-stu-id="6847b-774">The transactions are nested too deeply.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-775">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="6847b-775">JET_errInvalidSesid</span></span><br />
<span data-ttu-id="6847b-776">-1104</span><span class="sxs-lookup"><span data-stu-id="6847b-776">-1104</span></span></p></td>
<td><p><span data-ttu-id="6847b-777">Un descripteur de session n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-777">There is an invalid session handle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-778">JET_errWriteConflictPrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="6847b-778">JET_errWriteConflictPrimaryIndex</span></span><br />
<span data-ttu-id="6847b-779">-1105</span><span class="sxs-lookup"><span data-stu-id="6847b-779">-1105</span></span></p></td>
<td><p><span data-ttu-id="6847b-780">Une mise à jour a été tentée sur un index principal non validé.</span><span class="sxs-lookup"><span data-stu-id="6847b-780">An update was attempted on an uncommitted primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-781">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="6847b-781">JET_errInTransaction</span></span><br />
<span data-ttu-id="6847b-782">-1108</span><span class="sxs-lookup"><span data-stu-id="6847b-782">-1108</span></span></p></td>
<td><p><span data-ttu-id="6847b-783">L’opération n’est pas autorisée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="6847b-783">The operation is not allowed within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-784">JET_errRollbackRequired</span><span class="sxs-lookup"><span data-stu-id="6847b-784">JET_errRollbackRequired</span></span><br />
<span data-ttu-id="6847b-785">-1109</span><span class="sxs-lookup"><span data-stu-id="6847b-785">-1109</span></span></p></td>
<td><p><span data-ttu-id="6847b-786">La transaction en cours doit être restaurée.</span><span class="sxs-lookup"><span data-stu-id="6847b-786">The current transaction must be rolled back.</span></span> <span data-ttu-id="6847b-787">Elle ne peut pas être validée et une nouvelle ne peut pas être démarrée.</span><span class="sxs-lookup"><span data-stu-id="6847b-787">It cannot be committed and a new one cannot be started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-788">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="6847b-788">JET_errTransReadOnly</span></span><br />
<span data-ttu-id="6847b-789">-1110</span><span class="sxs-lookup"><span data-stu-id="6847b-789">-1110</span></span></p></td>
<td><p><span data-ttu-id="6847b-790">Une transaction en lecture seule a tenté de modifier la base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-790">A read-only transaction tried to modify the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-791">JET_errSessionWriteConflict</span><span class="sxs-lookup"><span data-stu-id="6847b-791">JET_errSessionWriteConflict</span></span><br />
<span data-ttu-id="6847b-792">-1111</span><span class="sxs-lookup"><span data-stu-id="6847b-792">-1111</span></span></p></td>
<td><p><span data-ttu-id="6847b-793">Tentative de remplacement du même enregistrement par deux curseurs différents dans la même session.</span><span class="sxs-lookup"><span data-stu-id="6847b-793">There was an attempt to replace the same record by two different cursors in the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-794">JET_errRecordTooBigForBackwardCompatibility</span><span class="sxs-lookup"><span data-stu-id="6847b-794">JET_errRecordTooBigForBackwardCompatibility</span></span><br />
<span data-ttu-id="6847b-795">-1112</span><span class="sxs-lookup"><span data-stu-id="6847b-795">-1112</span></span></p></td>
<td><p><span data-ttu-id="6847b-796">L’enregistrement est trop grand s’il est représenté dans un format de base de données à partir d’une version précédente de jet.</span><span class="sxs-lookup"><span data-stu-id="6847b-796">The record would be too big if represented in a database format from a previous version of Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-797">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="6847b-797">JET_errCannotMaterializeForwardOnlySort</span></span><br />
<span data-ttu-id="6847b-798">-1113</span><span class="sxs-lookup"><span data-stu-id="6847b-798">-1113</span></span></p></td>
<td><p><span data-ttu-id="6847b-799">La table temporaire n’a pas pu être créée en raison de paramètres qui sont en conflit avec JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="6847b-799">The temporary table could not be created due to parameters that conflict with JET_bitTTForwardOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-800">JET_errSesidTableIdMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-800">JET_errSesidTableIdMismatch</span></span><br />
<span data-ttu-id="6847b-801">-1114</span><span class="sxs-lookup"><span data-stu-id="6847b-801">-1114</span></span></p></td>
<td><p><span data-ttu-id="6847b-802">Le descripteur de session ne peut pas être utilisé avec l’ID de table, car il n’a pas été utilisé pour le créer.</span><span class="sxs-lookup"><span data-stu-id="6847b-802">The session handle cannot be used with the table id because it was not used to create it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-803">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="6847b-803">JET_errInvalidInstance</span></span><br />
<span data-ttu-id="6847b-804">-1115</span><span class="sxs-lookup"><span data-stu-id="6847b-804">-1115</span></span></p></td>
<td><p><span data-ttu-id="6847b-805">Le descripteur d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="6847b-805">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-806">JET_errReadLostFlushVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="6847b-806">JET_errReadLostFlushVerifyFailure</span></span><br />
<span data-ttu-id="6847b-807">-1119</span><span class="sxs-lookup"><span data-stu-id="6847b-807">-1119</span></span></p></td>
<td><p><span data-ttu-id="6847b-808">La page de base de données lue à partir du disque avait une écriture précédente non représentée sur la page.</span><span class="sxs-lookup"><span data-stu-id="6847b-808">The database page read from disk had a previous write not represented on the page.</span></span> <span data-ttu-id="6847b-809">Disponible sur Windows 8 et versions ultérieures pour le client et Windows Server 2012 et versions ultérieures pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="6847b-809">Available on Windows 8 and later for client, and Windows Server 2012 and later for server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-810">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="6847b-810">JET_errDatabaseDuplicate</span></span><br />
<span data-ttu-id="6847b-811">-1201</span><span class="sxs-lookup"><span data-stu-id="6847b-811">-1201</span></span></p></td>
<td><p><span data-ttu-id="6847b-812">La base de données existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6847b-812">The database already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-813">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-813">JET_errDatabaseInUse</span></span><br />
<span data-ttu-id="6847b-814">-1202</span><span class="sxs-lookup"><span data-stu-id="6847b-814">-1202</span></span></p></td>
<td><p><span data-ttu-id="6847b-815">Base de données en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-815">The database in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-816">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="6847b-816">JET_errDatabaseNotFound</span></span><br />
<span data-ttu-id="6847b-817">-1203</span><span class="sxs-lookup"><span data-stu-id="6847b-817">-1203</span></span></p></td>
<td><p><span data-ttu-id="6847b-818">Il n’existe aucune base de données de ce type.</span><span class="sxs-lookup"><span data-stu-id="6847b-818">There is no such database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-819">JET_errDatabaseInvalidName</span><span class="sxs-lookup"><span data-stu-id="6847b-819">JET_errDatabaseInvalidName</span></span><br />
<span data-ttu-id="6847b-820">-1204</span><span class="sxs-lookup"><span data-stu-id="6847b-820">-1204</span></span></p></td>
<td><p><span data-ttu-id="6847b-821">Le nom de la base de données n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-821">The database name is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-822">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="6847b-822">JET_errDatabaseInvalidPages</span></span><br />
<span data-ttu-id="6847b-823">-1205</span><span class="sxs-lookup"><span data-stu-id="6847b-823">-1205</span></span></p></td>
<td><p><span data-ttu-id="6847b-824">Le nombre de pages est incorrect.</span><span class="sxs-lookup"><span data-stu-id="6847b-824">There are an invalid number of pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-825">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-825">JET_errDatabaseCorrupted</span></span><br />
<span data-ttu-id="6847b-826">-1206</span><span class="sxs-lookup"><span data-stu-id="6847b-826">-1206</span></span></p></td>
<td><p><span data-ttu-id="6847b-827">Il n’existe pas de fichier de base de données ou de base de données endommagée.</span><span class="sxs-lookup"><span data-stu-id="6847b-827">There is a non-database file or corrupt database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-828">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="6847b-828">JET_errDatabaseLocked</span></span><br />
<span data-ttu-id="6847b-829">-1207</span><span class="sxs-lookup"><span data-stu-id="6847b-829">-1207</span></span></p></td>
<td><p><span data-ttu-id="6847b-830">La base de données est verrouillée en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="6847b-830">The database is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-831">JET_errCannotDisableVersioning</span><span class="sxs-lookup"><span data-stu-id="6847b-831">JET_errCannotDisableVersioning</span></span><br />
<span data-ttu-id="6847b-832">-1208</span><span class="sxs-lookup"><span data-stu-id="6847b-832">-1208</span></span></p></td>
<td><p><span data-ttu-id="6847b-833">Le contrôle de version de cette base de données ne peut pas être désactivé.</span><span class="sxs-lookup"><span data-stu-id="6847b-833">The versioning for this database cannot be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-834">JET_errInvalidDatabaseVersion</span><span class="sxs-lookup"><span data-stu-id="6847b-834">JET_errInvalidDatabaseVersion</span></span><br />
<span data-ttu-id="6847b-835">-1209</span><span class="sxs-lookup"><span data-stu-id="6847b-835">-1209</span></span></p></td>
<td><p><span data-ttu-id="6847b-836">Le moteur de base de données est incompatible avec la base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-836">The database engine is incompatible with the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-837">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="6847b-837">JET_errDatabase200Format</span></span><br />
<span data-ttu-id="6847b-838">-1210</span><span class="sxs-lookup"><span data-stu-id="6847b-838">-1210</span></span></p></td>
<td><p><span data-ttu-id="6847b-839">La base de données est dans un format plus ancien (200).</span><span class="sxs-lookup"><span data-stu-id="6847b-839">The database is in an older (200) format.</span></span> <span data-ttu-id="6847b-840">Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-840">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="6847b-841">Client Windows NT uniquement.</span><span class="sxs-lookup"><span data-stu-id="6847b-841">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-842">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="6847b-842">JET_errDatabase400Format</span></span><br />
<span data-ttu-id="6847b-843">-1211</span><span class="sxs-lookup"><span data-stu-id="6847b-843">-1211</span></span></p></td>
<td><p><span data-ttu-id="6847b-844">La base de données est dans un format plus ancien (400).</span><span class="sxs-lookup"><span data-stu-id="6847b-844">The database is in an older (400) format.</span></span> <span data-ttu-id="6847b-845">Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-845">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="6847b-846">Client Windows NT uniquement.</span><span class="sxs-lookup"><span data-stu-id="6847b-846">Windows NT client only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-847">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="6847b-847">JET_errDatabase500Format</span></span><br />
<span data-ttu-id="6847b-848">-1212</span><span class="sxs-lookup"><span data-stu-id="6847b-848">-1212</span></span></p></td>
<td><p><span data-ttu-id="6847b-849">La base de données est dans un format plus ancien (500).</span><span class="sxs-lookup"><span data-stu-id="6847b-849">The database is in an older (500) format.</span></span> <span data-ttu-id="6847b-850">Cette erreur est retournée par <a href="gg294068(v=exchg.10).md">JetInit</a> si <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> est défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-850">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="6847b-851">Client Windows NT uniquement.</span><span class="sxs-lookup"><span data-stu-id="6847b-851">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-852">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-852">JET_errPageSizeMismatch</span></span><br />
<span data-ttu-id="6847b-853">-1213</span><span class="sxs-lookup"><span data-stu-id="6847b-853">-1213</span></span></p></td>
<td><p><span data-ttu-id="6847b-854">La taille de la page de la base de données ne correspond pas au moteur.</span><span class="sxs-lookup"><span data-stu-id="6847b-854">The database page size does not match the engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-855">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="6847b-855">JET_errTooManyInstances</span></span><br />
<span data-ttu-id="6847b-856">-1214</span><span class="sxs-lookup"><span data-stu-id="6847b-856">-1214</span></span></p></td>
<td><p><span data-ttu-id="6847b-857">Aucune instance de base de données supplémentaire ne peut être démarrée.</span><span class="sxs-lookup"><span data-stu-id="6847b-857">No more database instances can be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-858">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6847b-858">JET_errDatabaseSharingViolation</span></span><br />
<span data-ttu-id="6847b-859">-1215</span><span class="sxs-lookup"><span data-stu-id="6847b-859">-1215</span></span></p></td>
<td><p><span data-ttu-id="6847b-860">Une autre instance de base de données utilise cette base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-860">A different database instance is using this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-861">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="6847b-861">JET_errAttachedDatabaseMismatch</span></span><br />
<span data-ttu-id="6847b-862">-1216</span><span class="sxs-lookup"><span data-stu-id="6847b-862">-1216</span></span></p></td>
<td><p><span data-ttu-id="6847b-863">Une pièce jointe de base de données en attente a été détectée au début ou à la fin de la récupération, mais la base de données est manquante ou ne correspond pas aux informations de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6847b-863">An outstanding database attachment has been detected at the start or end of the recovery, but the database is missing or does not match attachment info.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-864">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6847b-864">JET_errDatabaseInvalidPath</span></span><br />
<span data-ttu-id="6847b-865">-1217</span><span class="sxs-lookup"><span data-stu-id="6847b-865">-1217</span></span></p></td>
<td><p><span data-ttu-id="6847b-866">Le chemin d’accès au fichier de base de données spécifié n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="6847b-866">The specified path to the database file is illegal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-867">JET_errDatabaseIdInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-867">JET_errDatabaseIdInUse</span></span><br />
<span data-ttu-id="6847b-868">-1218</span><span class="sxs-lookup"><span data-stu-id="6847b-868">-1218</span></span></p></td>
<td><p><span data-ttu-id="6847b-869">Un ID qui est déjà en cours d’utilisation est assigné à une base de données.</span><span class="sxs-lookup"><span data-stu-id="6847b-869">A database is being assigned an ID that is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-870">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="6847b-870">JET_errForceDetachNotAllowed</span></span><br />
<span data-ttu-id="6847b-871">-1219</span><span class="sxs-lookup"><span data-stu-id="6847b-871">-1219</span></span></p></td>
<td><p><span data-ttu-id="6847b-872">Le détachement forcé est autorisé uniquement après l’arrêt du détachement normal en raison d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="6847b-872">The force detach is allowed only after the normal detach was stopped due to an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-873">JET_errCatalogCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-873">JET_errCatalogCorrupted</span></span><br />
<span data-ttu-id="6847b-874">-1220</span><span class="sxs-lookup"><span data-stu-id="6847b-874">-1220</span></span></p></td>
<td><p><span data-ttu-id="6847b-875">Une altération a été détectée dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="6847b-875">Corruption was detected in the catalog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-876">JET_errPartiallyAttachedDB</span><span class="sxs-lookup"><span data-stu-id="6847b-876">JET_errPartiallyAttachedDB</span></span><br />
<span data-ttu-id="6847b-877">-1221</span><span class="sxs-lookup"><span data-stu-id="6847b-877">-1221</span></span></p></td>
<td><p><span data-ttu-id="6847b-878">La base de données n’est attachée que partiellement et l’opération d’attachement ne peut pas être effectuée.</span><span class="sxs-lookup"><span data-stu-id="6847b-878">The database is only partially attached and the attach operation cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-879">JET_errDatabaseSignInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-879">JET_errDatabaseSignInUse</span></span><br />
<span data-ttu-id="6847b-880">-1222</span><span class="sxs-lookup"><span data-stu-id="6847b-880">-1222</span></span></p></td>
<td><p><span data-ttu-id="6847b-881">La base de données avec la même signature est déjà en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-881">The database with the same signature is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-882">JET_errDatabaseCorruptedNoRepair</span><span class="sxs-lookup"><span data-stu-id="6847b-882">JET_errDatabaseCorruptedNoRepair</span></span><br />
<span data-ttu-id="6847b-883">-1224</span><span class="sxs-lookup"><span data-stu-id="6847b-883">-1224</span></span></p></td>
<td><p><span data-ttu-id="6847b-884">La base de données est endommagée, mais aucune réparation n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="6847b-884">The database is corrupted but a repair is not allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-885">JET_errInvalidCreateDbVersion</span><span class="sxs-lookup"><span data-stu-id="6847b-885">JET_errInvalidCreateDbVersion</span></span><br />
<span data-ttu-id="6847b-886">-1225</span><span class="sxs-lookup"><span data-stu-id="6847b-886">-1225</span></span></p></td>
<td><p><span data-ttu-id="6847b-887">Le moteur de base de données a tenté de relire une opération créer une base de données à partir du journal des transactions mais a échoué en raison d’une version incompatible de cette opération.</span><span class="sxs-lookup"><span data-stu-id="6847b-887">The database engine attempted to replay a Create Database operation from the transaction log but failed due to an incompatible version of that operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-888">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="6847b-888">JET_errTableLocked</span></span><br />
<span data-ttu-id="6847b-889">-1302</span><span class="sxs-lookup"><span data-stu-id="6847b-889">-1302</span></span></p></td>
<td><p><span data-ttu-id="6847b-890">La table est verrouillée en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="6847b-890">The table is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-891">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="6847b-891">JET_errTableDuplicate</span></span><br />
<span data-ttu-id="6847b-892">-1303</span><span class="sxs-lookup"><span data-stu-id="6847b-892">-1303</span></span></p></td>
<td><p><span data-ttu-id="6847b-893">La table existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6847b-893">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-894">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="6847b-894">JET_errTableInUse</span></span><br />
<span data-ttu-id="6847b-895">-1304</span><span class="sxs-lookup"><span data-stu-id="6847b-895">-1304</span></span></p></td>
<td><p><span data-ttu-id="6847b-896">La table est en cours d’utilisation et ne peut pas être verrouillée.</span><span class="sxs-lookup"><span data-stu-id="6847b-896">The table is in use and cannot be locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-897">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="6847b-897">JET_errObjectNotFound</span></span><br />
<span data-ttu-id="6847b-898">-1305</span><span class="sxs-lookup"><span data-stu-id="6847b-898">-1305</span></span></p></td>
<td><p><span data-ttu-id="6847b-899">Il n’existe pas de table ou d’objet de ce type.</span><span class="sxs-lookup"><span data-stu-id="6847b-899">There is no such table or object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-900">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="6847b-900">JET_errDensityInvalid</span></span><br />
<span data-ttu-id="6847b-901">-1307</span><span class="sxs-lookup"><span data-stu-id="6847b-901">-1307</span></span></p></td>
<td><p><span data-ttu-id="6847b-902">La densité d’un fichier ou d’un index est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-902">There is a bad file or index density.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-903">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="6847b-903">JET_errTableNotEmpty</span></span><br />
<span data-ttu-id="6847b-904">-1308</span><span class="sxs-lookup"><span data-stu-id="6847b-904">-1308</span></span></p></td>
<td><p><span data-ttu-id="6847b-905">La table n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="6847b-905">The table is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-906">JET_errInvalidTableId</span><span class="sxs-lookup"><span data-stu-id="6847b-906">JET_errInvalidTableId</span></span><br />
<span data-ttu-id="6847b-907">-1310</span><span class="sxs-lookup"><span data-stu-id="6847b-907">-1310</span></span></p></td>
<td><p><span data-ttu-id="6847b-908">L’ID de table n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-908">The table ID is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-909">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="6847b-909">JET_errTooManyOpenTables</span></span><br />
<span data-ttu-id="6847b-910">-1311</span><span class="sxs-lookup"><span data-stu-id="6847b-910">-1311</span></span></p></td>
<td><p><span data-ttu-id="6847b-911">Aucune autre table ne peut être ouverte, même après l’exécution de la tâche de nettoyage interne.</span><span class="sxs-lookup"><span data-stu-id="6847b-911">No more tables can be opened, even after the internal cleanup task has run.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-912">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="6847b-912">JET_errIllegalOperation</span></span><br />
<span data-ttu-id="6847b-913">-1312</span><span class="sxs-lookup"><span data-stu-id="6847b-913">-1312</span></span></p></td>
<td><p><span data-ttu-id="6847b-914">L’opération n’est pas prise en charge sur la table.</span><span class="sxs-lookup"><span data-stu-id="6847b-914">The operation is not supported on the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="6847b-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span></span><br />
<span data-ttu-id="6847b-916">-1313</span><span class="sxs-lookup"><span data-stu-id="6847b-916">-1313</span></span></p></td>
<td><p><span data-ttu-id="6847b-917">Impossible d’ouvrir davantage de tables en raison de l’échec de la tentative de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="6847b-917">No more tables can be opened because the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-918">JET_errObjectDuplicate</span><span class="sxs-lookup"><span data-stu-id="6847b-918">JET_errObjectDuplicate</span></span><br />
<span data-ttu-id="6847b-919">-1314</span><span class="sxs-lookup"><span data-stu-id="6847b-919">-1314</span></span></p></td>
<td><p><span data-ttu-id="6847b-920">Le nom de la table ou de l’objet est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-920">The table or object name is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-921">JET_errInvalidObject</span><span class="sxs-lookup"><span data-stu-id="6847b-921">JET_errInvalidObject</span></span><br />
<span data-ttu-id="6847b-922">-1316</span><span class="sxs-lookup"><span data-stu-id="6847b-922">-1316</span></span></p></td>
<td><p><span data-ttu-id="6847b-923">L’objet n’est pas valide pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="6847b-923">The object is invalid for operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-924">JET_errCannotDeleteTempTable</span><span class="sxs-lookup"><span data-stu-id="6847b-924">JET_errCannotDeleteTempTable</span></span><br />
<span data-ttu-id="6847b-925">-1317</span><span class="sxs-lookup"><span data-stu-id="6847b-925">-1317</span></span></p></td>
<td><p><span data-ttu-id="6847b-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> doit être utilisé à la place de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> pour supprimer une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="6847b-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> must be used instead of <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> to delete a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-927">JET_errCannotDeleteSystemTable</span><span class="sxs-lookup"><span data-stu-id="6847b-927">JET_errCannotDeleteSystemTable</span></span><br />
<span data-ttu-id="6847b-928">-1318</span><span class="sxs-lookup"><span data-stu-id="6847b-928">-1318</span></span></p></td>
<td><p><span data-ttu-id="6847b-929">Tentative non autorisée de suppression d’une table système.</span><span class="sxs-lookup"><span data-stu-id="6847b-929">There was an illegal attempt to delete a system table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-930">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="6847b-930">JET_errCannotDeleteTemplateTable</span></span><br />
<span data-ttu-id="6847b-931">-1319</span><span class="sxs-lookup"><span data-stu-id="6847b-931">-1319</span></span></p></td>
<td><p><span data-ttu-id="6847b-932">Une tentative non autorisée de suppression d’une table de modèle a été créée.</span><span class="sxs-lookup"><span data-stu-id="6847b-932">There was an illegal attempt to delete a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-933">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="6847b-933">JET_errExclusiveTableLockRequired</span></span><br />
<span data-ttu-id="6847b-934">-1322</span><span class="sxs-lookup"><span data-stu-id="6847b-934">-1322</span></span></p></td>
<td><p><span data-ttu-id="6847b-935">Il doit y avoir un verrou exclusif sur la table.</span><span class="sxs-lookup"><span data-stu-id="6847b-935">There must be an exclusive lock on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-936">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="6847b-936">JET_errFixedDDL</span></span><br />
<span data-ttu-id="6847b-937">-1323</span><span class="sxs-lookup"><span data-stu-id="6847b-937">-1323</span></span></p></td>
<td><p><span data-ttu-id="6847b-938">Les opérations DDL sont interdites sur cette table.</span><span class="sxs-lookup"><span data-stu-id="6847b-938">DDL operations are prohibited on this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-939">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="6847b-939">JET_errFixedInheritedDDL</span></span><br />
<span data-ttu-id="6847b-940">-1324</span><span class="sxs-lookup"><span data-stu-id="6847b-940">-1324</span></span></p></td>
<td><p><span data-ttu-id="6847b-941">Sur une table dérivée, les opérations DDL sont interdites sur la partie héritée du DDL.</span><span class="sxs-lookup"><span data-stu-id="6847b-941">On a derived table, DDL operations are prohibited on the inherited portion of the DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-942">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="6847b-942">JET_errCannotNestDDL</span></span><br />
<span data-ttu-id="6847b-943">-1325</span><span class="sxs-lookup"><span data-stu-id="6847b-943">-1325</span></span></p></td>
<td><p><span data-ttu-id="6847b-944">L’imbrication du DDL hiérarchique n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="6847b-944">Nesting the hierarchical DDL is not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-945">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="6847b-945">JET_errDDLNotInheritable</span></span><br />
<span data-ttu-id="6847b-946">-1326</span><span class="sxs-lookup"><span data-stu-id="6847b-946">-1326</span></span></p></td>
<td><p><span data-ttu-id="6847b-947">Une tentative d’héritage d’une DDL a été tentée à partir d’une table qui n’est pas marquée comme table de modèle.</span><span class="sxs-lookup"><span data-stu-id="6847b-947">There was an attempt to inherit a DDL from a table that is not marked as a template table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-948">JET_errInvalidSettings</span><span class="sxs-lookup"><span data-stu-id="6847b-948">JET_errInvalidSettings</span></span><br />
<span data-ttu-id="6847b-949">-1328</span><span class="sxs-lookup"><span data-stu-id="6847b-949">-1328</span></span></p></td>
<td><p><span data-ttu-id="6847b-950">Les paramètres système ont été définis de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-950">The system parameters were set improperly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-951">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6847b-951">JET_errClientRequestToStopJetService</span></span><br />
<span data-ttu-id="6847b-952">-1329</span><span class="sxs-lookup"><span data-stu-id="6847b-952">-1329</span></span></p></td>
<td><p><span data-ttu-id="6847b-953">Le client a demandé l’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="6847b-953">The client has requested that the service be stopped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-954">JET_errCannotAddFixedVarColumnToDerivedTable</span><span class="sxs-lookup"><span data-stu-id="6847b-954">JET_errCannotAddFixedVarColumnToDerivedTable</span></span><br />
<span data-ttu-id="6847b-955">-1330</span><span class="sxs-lookup"><span data-stu-id="6847b-955">-1330</span></span></p></td>
<td><p><span data-ttu-id="6847b-956">La table de modèle a été créée avec l’indicateur NoFixedVarColumnsInDerivedTables défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-956">The Template table was created with the NoFixedVarColumnsInDerivedTables flag set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-957">JET_errIndexCantBuild</span><span class="sxs-lookup"><span data-stu-id="6847b-957">JET_errIndexCantBuild</span></span><br />
<span data-ttu-id="6847b-958">-1401</span><span class="sxs-lookup"><span data-stu-id="6847b-958">-1401</span></span></p></td>
<td><p><span data-ttu-id="6847b-959">Échec de la génération de l’index.</span><span class="sxs-lookup"><span data-stu-id="6847b-959">The index build failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-960">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="6847b-960">JET_errIndexHasPrimary</span></span><br />
<span data-ttu-id="6847b-961">-1402</span><span class="sxs-lookup"><span data-stu-id="6847b-961">-1402</span></span></p></td>
<td><p><span data-ttu-id="6847b-962">L’index primaire est déjà défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-962">The primary index is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-963">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="6847b-963">JET_errIndexDuplicate</span></span><br />
<span data-ttu-id="6847b-964">-1403</span><span class="sxs-lookup"><span data-stu-id="6847b-964">-1403</span></span></p></td>
<td><p><span data-ttu-id="6847b-965">L’index est déjà défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-965">The index is already defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-966">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="6847b-966">JET_errIndexNotFound</span></span><br />
<span data-ttu-id="6847b-967">-1404</span><span class="sxs-lookup"><span data-stu-id="6847b-967">-1404</span></span></p></td>
<td><p><span data-ttu-id="6847b-968">Il n’y a pas d’index de ce type.</span><span class="sxs-lookup"><span data-stu-id="6847b-968">There is no such index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-969">JET_errIndexMustStay</span><span class="sxs-lookup"><span data-stu-id="6847b-969">JET_errIndexMustStay</span></span><br />
<span data-ttu-id="6847b-970">-1405</span><span class="sxs-lookup"><span data-stu-id="6847b-970">-1405</span></span></p></td>
<td><p><span data-ttu-id="6847b-971">Impossible de supprimer l’index cluster.</span><span class="sxs-lookup"><span data-stu-id="6847b-971">The clustered index cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-972">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="6847b-972">JET_errIndexInvalidDef</span></span><br />
<span data-ttu-id="6847b-973">-1406</span><span class="sxs-lookup"><span data-stu-id="6847b-973">-1406</span></span></p></td>
<td><p><span data-ttu-id="6847b-974">La définition de l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-974">The index definition is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-975">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="6847b-975">JET_errInvalidCreateIndex</span></span><br />
<span data-ttu-id="6847b-976">-1409</span><span class="sxs-lookup"><span data-stu-id="6847b-976">-1409</span></span></p></td>
<td><p><span data-ttu-id="6847b-977">La création de la description de l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-977">The creation of the index description was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-978">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="6847b-978">JET_errTooManyOpenIndexes</span></span><br />
<span data-ttu-id="6847b-979">-1410</span><span class="sxs-lookup"><span data-stu-id="6847b-979">-1410</span></span></p></td>
<td><p><span data-ttu-id="6847b-980">La base de données est en dehors des blocs de description d’index.</span><span class="sxs-lookup"><span data-stu-id="6847b-980">The database is out of index description blocks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-981">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="6847b-981">JET_errMultiValuedIndexViolation</span></span><br />
<span data-ttu-id="6847b-982">-1411</span><span class="sxs-lookup"><span data-stu-id="6847b-982">-1411</span></span></p></td>
<td><p><span data-ttu-id="6847b-983">Des clés d’index entre enregistrements non uniques ont été générées pour un index à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="6847b-983">Non-unique inter-record index keys have been generated for a multi-valued index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-984">JET_errIndexBuildCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-984">JET_errIndexBuildCorrupted</span></span><br />
<span data-ttu-id="6847b-985">-1412</span><span class="sxs-lookup"><span data-stu-id="6847b-985">-1412</span></span></p></td>
<td><p><span data-ttu-id="6847b-986">Un index secondaire qui reflète correctement l’index primaire n’a pas pu être généré.</span><span class="sxs-lookup"><span data-stu-id="6847b-986">A secondary index that properly reflects the primary index failed to build.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-987">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-987">JET_errPrimaryIndexCorrupted</span></span><br />
<span data-ttu-id="6847b-988">-1413</span><span class="sxs-lookup"><span data-stu-id="6847b-988">-1413</span></span></p></td>
<td><p><span data-ttu-id="6847b-989">L’index primaire est endommagé et la base de données doit être défragmentée.</span><span class="sxs-lookup"><span data-stu-id="6847b-989">The primary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-990">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="6847b-990">JET_errSecondaryIndexCorrupted</span></span><br />
<span data-ttu-id="6847b-991">-1414</span><span class="sxs-lookup"><span data-stu-id="6847b-991">-1414</span></span></p></td>
<td><p><span data-ttu-id="6847b-992">L’index secondaire est endommagé et la base de données doit être défragmentée.</span><span class="sxs-lookup"><span data-stu-id="6847b-992">The secondary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-993">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="6847b-993">JET_errInvalidIndexId</span></span><br />
<span data-ttu-id="6847b-994">-1416</span><span class="sxs-lookup"><span data-stu-id="6847b-994">-1416</span></span></p></td>
<td><p><span data-ttu-id="6847b-995">L’ID d’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-995">The index ID is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-996">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="6847b-996">JET_errIndexTuplesSecondaryIndexOnly</span></span><br />
<span data-ttu-id="6847b-997">-1430</span><span class="sxs-lookup"><span data-stu-id="6847b-997">-1430</span></span></p></td>
<td><p><span data-ttu-id="6847b-998">L’index de tuple ne peut être défini que sur un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="6847b-998">The tuple index can only be set on a secondary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-999">JET_errIndexTuplesTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="6847b-999">JET_errIndexTuplesTooManyColumns</span></span><br />
<span data-ttu-id="6847b-1000">-1431</span><span class="sxs-lookup"><span data-stu-id="6847b-1000">-1431</span></span></p></td>
<td><p><span data-ttu-id="6847b-1001">La définition d’index de l’index de tuple contient plus de colonnes clés que le moteur de base de données peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="6847b-1001">The index definition for the tuple index contains more key columns that the database engine can support.</span></span></p>
<p><span data-ttu-id="6847b-1002"><strong>Remarque  </strong> L’erreur de JET_errIndexTuplesOneColumnOnly est obsolète et a été remplacée par JET_errIndexTuplesTooManyColumns.</span><span class="sxs-lookup"><span data-stu-id="6847b-1002"><strong>Note  </strong>The JET_errIndexTuplesOneColumnOnly error is obsolete and has been replaced by JET_errIndexTuplesTooManyColumns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1003">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="6847b-1003">JET_errIndexTuplesNonUniqueOnly</span></span><br />
<span data-ttu-id="6847b-1004">-1432</span><span class="sxs-lookup"><span data-stu-id="6847b-1004">-1432</span></span></p></td>
<td><p><span data-ttu-id="6847b-1005">L’index de tuple doit être un index non unique.</span><span class="sxs-lookup"><span data-stu-id="6847b-1005">The tuple index must be a non-unique index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="6847b-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span></span><br />
<span data-ttu-id="6847b-1007">-1433</span><span class="sxs-lookup"><span data-stu-id="6847b-1007">-1433</span></span></p></td>
<td><p><span data-ttu-id="6847b-1008">Une définition d’index de tuple ne peut contenir que des colonnes clés qui ont des types de colonnes texte ou binaires.</span><span class="sxs-lookup"><span data-stu-id="6847b-1008">A tuple index definition can only contain key columns that have text or binary column types.</span></span></p>
<p><span data-ttu-id="6847b-1009"><strong>Remarque  </strong> L’erreur de JET_errIndexTuplesTextColumnsOnly est obsolète et a été remplacée par JET_errIndexTuplesTextBinaryColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="6847b-1009"><strong>Note  </strong>The JET_errIndexTuplesTextColumnsOnly error is obsolete and has been replaced by JET_errIndexTuplesTextBinaryColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1010">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="6847b-1010">JET_errIndexTuplesVarSegMacNotAllowed</span></span><br />
<span data-ttu-id="6847b-1011">-1434</span><span class="sxs-lookup"><span data-stu-id="6847b-1011">-1434</span></span></p></td>
<td><p><span data-ttu-id="6847b-1012">L’index du tuple n’autorise pas la définition de cbVarSegMac.</span><span class="sxs-lookup"><span data-stu-id="6847b-1012">The tuple index does not allow setting cbVarSegMac.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1013">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="6847b-1013">JET_errIndexTuplesInvalidLimits</span></span><br />
<span data-ttu-id="6847b-1014">-1435</span><span class="sxs-lookup"><span data-stu-id="6847b-1014">-1435</span></span></p></td>
<td><p><span data-ttu-id="6847b-1015">La longueur minimale/maximale du tuple ou le nombre maximal de caractères spécifiés pour un index ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="6847b-1015">The minimum/maximum tuple length or the maximum number of characters that are specified for an index are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="6847b-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span></span><br />
<span data-ttu-id="6847b-1017">-1436</span><span class="sxs-lookup"><span data-stu-id="6847b-1017">-1436</span></span></p></td>
<td><p><span data-ttu-id="6847b-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ne peut pas être appelé avec l’indicateur JET_bitRetrieveFromIndex défini lors de la récupération d’une colonne sur un index de Tuple.</span><span class="sxs-lookup"><span data-stu-id="6847b-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> cannot be called with the JET_bitRetrieveFromIndex flag set while retrieving a column on a tuple index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1019">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="6847b-1019">JET_errIndexTuplesKeyTooSmall</span></span><br />
<span data-ttu-id="6847b-1020">-1437</span><span class="sxs-lookup"><span data-stu-id="6847b-1020">-1437</span></span></p></td>
<td><p><span data-ttu-id="6847b-1021">La clé spécifiée ne répond pas à la longueur minimale du tuple.</span><span class="sxs-lookup"><span data-stu-id="6847b-1021">The specified key does not meet the minimum tuple length.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1022">JET_errColumnLong</span><span class="sxs-lookup"><span data-stu-id="6847b-1022">JET_errColumnLong</span></span><br />
<span data-ttu-id="6847b-1023">-1501</span><span class="sxs-lookup"><span data-stu-id="6847b-1023">-1501</span></span></p></td>
<td><p><span data-ttu-id="6847b-1024">La valeur de la colonne est longue.</span><span class="sxs-lookup"><span data-stu-id="6847b-1024">The column value is long.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1025">JET_errColumnNoChunk</span><span class="sxs-lookup"><span data-stu-id="6847b-1025">JET_errColumnNoChunk</span></span><br />
<span data-ttu-id="6847b-1026">-1502</span><span class="sxs-lookup"><span data-stu-id="6847b-1026">-1502</span></span></p></td>
<td><p><span data-ttu-id="6847b-1027">Il n’existe pas de ce type de bloc dans une valeur long.</span><span class="sxs-lookup"><span data-stu-id="6847b-1027">There is no such chunk in a long value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1028">JET_errColumnDoesNotFit</span><span class="sxs-lookup"><span data-stu-id="6847b-1028">JET_errColumnDoesNotFit</span></span><br />
<span data-ttu-id="6847b-1029">-1503</span><span class="sxs-lookup"><span data-stu-id="6847b-1029">-1503</span></span></p></td>
<td><p><span data-ttu-id="6847b-1030">Le champ ne peut pas être contenu dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6847b-1030">The field will not fit in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1031">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="6847b-1031">JET_errNullInvalid</span></span><br />
<span data-ttu-id="6847b-1032">-1504</span><span class="sxs-lookup"><span data-stu-id="6847b-1032">-1504</span></span></p></td>
<td><p><span data-ttu-id="6847b-1033">NULL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-1033">Null is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1034">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="6847b-1034">JET_errColumnIllegalNull</span></span><br />
<span data-ttu-id="6847b-1035">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="6847b-1035">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="6847b-1036">NULL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-1036">Null is not valid.</span></span> <span data-ttu-id="6847b-1037">Cette erreur est retournée par le gestionnaire d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6847b-1037">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1038">JET_errColumnIndexed-1505</span><span class="sxs-lookup"><span data-stu-id="6847b-1038">JET_errColumnIndexed -1505</span></span></p></td>
<td><p><span data-ttu-id="6847b-1039">La colonne est indexée et ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1039">The column is indexed and cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1040">JET_errColumnTooBig-1506</span><span class="sxs-lookup"><span data-stu-id="6847b-1040">JET_errColumnTooBig -1506</span></span></p></td>
<td><p><span data-ttu-id="6847b-1041">La longueur du champ est supérieure à la longueur maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1041">The field length is greater than maximum allowed length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1042">JET_errColumnNotFound-1507</span><span class="sxs-lookup"><span data-stu-id="6847b-1042">JET_errColumnNotFound -1507</span></span></p></td>
<td><p><span data-ttu-id="6847b-1043">Il n’existe aucune colonne de ce type.</span><span class="sxs-lookup"><span data-stu-id="6847b-1043">There is no such column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1044">JET_errColumnDuplicate-1508</span><span class="sxs-lookup"><span data-stu-id="6847b-1044">JET_errColumnDuplicate -1508</span></span></p></td>
<td><p><span data-ttu-id="6847b-1045">Ce champ est déjà défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-1045">This field is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1046">JET_errMultiValuedColumnMustBeTagged-1509</span><span class="sxs-lookup"><span data-stu-id="6847b-1046">JET_errMultiValuedColumnMustBeTagged -1509</span></span></p></td>
<td><p><span data-ttu-id="6847b-1047">Une tentative de création d’une colonne à valeurs multiples a été effectuée, mais la colonne n’a pas été marquée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1047">An attempt was made to create a multi-valued column, but the column was not tagged.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1048">JET_errColumnRedundant-1510</span><span class="sxs-lookup"><span data-stu-id="6847b-1048">JET_errColumnRedundant -1510</span></span></p></td>
<td><p><span data-ttu-id="6847b-1049">Une deuxième colonne d’auto-incrémentation ou de version était présente.</span><span class="sxs-lookup"><span data-stu-id="6847b-1049">There was a second auto-increment or version column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1050">JET_errInvalidColumnType-1511</span><span class="sxs-lookup"><span data-stu-id="6847b-1050">JET_errInvalidColumnType -1511</span></span></p></td>
<td><p><span data-ttu-id="6847b-1051">Le type de données de la colonne n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-1051">The column data type is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1052">JET_errTaggedNotNULL-1514</span><span class="sxs-lookup"><span data-stu-id="6847b-1052">JET_errTaggedNotNULL -1514</span></span></p></td>
<td><p><span data-ttu-id="6847b-1053">Il n’existe aucune colonne avec balises non NULL.</span><span class="sxs-lookup"><span data-stu-id="6847b-1053">There are no non-NULL tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1054">JET_errNoCurrentIndex-1515</span><span class="sxs-lookup"><span data-stu-id="6847b-1054">JET_errNoCurrentIndex -1515</span></span></p></td>
<td><p><span data-ttu-id="6847b-1055">La base de données n’est pas valide, car elle ne contient pas d’index en cours.</span><span class="sxs-lookup"><span data-stu-id="6847b-1055">The database is invalid because it does not contain a current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1056">JET_errKeyIsMade-1516</span><span class="sxs-lookup"><span data-stu-id="6847b-1056">JET_errKeyIsMade -1516</span></span></p></td>
<td><p><span data-ttu-id="6847b-1057">La clé est entièrement créée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1057">The key is completely made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1058">JET_errBadColumnId-1517</span><span class="sxs-lookup"><span data-stu-id="6847b-1058">JET_errBadColumnId -1517</span></span></p></td>
<td><p><span data-ttu-id="6847b-1059">L’ID de colonne est incorrect.</span><span class="sxs-lookup"><span data-stu-id="6847b-1059">The column ID is incorrect.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1060">JET_errBadItagSequence-1518</span><span class="sxs-lookup"><span data-stu-id="6847b-1060">JET_errBadItagSequence -1518</span></span></p></td>
<td><p><span data-ttu-id="6847b-1061">Il y a un mauvais itagSequence pour la colonne avec balises.</span><span class="sxs-lookup"><span data-stu-id="6847b-1061">There is a bad itagSequence for the tagged column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1062">JET_errColumnInRelationship-1519</span><span class="sxs-lookup"><span data-stu-id="6847b-1062">JET_errColumnInRelationship -1519</span></span></p></td>
<td><p><span data-ttu-id="6847b-1063">Une colonne ne peut pas être supprimée, car elle fait partie d’une relation.</span><span class="sxs-lookup"><span data-stu-id="6847b-1063">A column cannot be deleted because it is part of a relationship.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1064">JET_errCannotBeTagged-1521</span><span class="sxs-lookup"><span data-stu-id="6847b-1064">JET_errCannotBeTagged -1521</span></span></p></td>
<td><p><span data-ttu-id="6847b-1065">Impossible d’étiqueter l’incrément et la version automatiques.</span><span class="sxs-lookup"><span data-stu-id="6847b-1065">The auto increment and version cannot be tagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1066">JET_errDefaultValueTooBig-1524</span><span class="sxs-lookup"><span data-stu-id="6847b-1066">JET_errDefaultValueTooBig -1524</span></span></p></td>
<td><p><span data-ttu-id="6847b-1067">La valeur par défaut dépasse la taille maximale.</span><span class="sxs-lookup"><span data-stu-id="6847b-1067">The default value exceeds the maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1068">JET_errMultiValuedDuplicate-1525</span><span class="sxs-lookup"><span data-stu-id="6847b-1068">JET_errMultiValuedDuplicate -1525</span></span></p></td>
<td><p><span data-ttu-id="6847b-1069">Une valeur dupliquée a été détectée sur une colonne à valeurs multiples unique.</span><span class="sxs-lookup"><span data-stu-id="6847b-1069">A duplicate value was detected on a unique multi-valued column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1070">JET_errLVCorrupted-1526</span><span class="sxs-lookup"><span data-stu-id="6847b-1070">JET_errLVCorrupted -1526</span></span></p></td>
<td><p><span data-ttu-id="6847b-1071">Une altération s’est produite dans une arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="6847b-1071">Corruption was encountered in a long-value tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1072">JET_errMultiValuedDuplicateAfterTruncation-1528</span><span class="sxs-lookup"><span data-stu-id="6847b-1072">JET_errMultiValuedDuplicateAfterTruncation -1528</span></span></p></td>
<td><p><span data-ttu-id="6847b-1073">Une valeur dupliquée a été détectée sur une colonne à valeurs multiples unique une fois que les données ont été normalisées, et la normalisation des données a été tronquée avant la comparaison.</span><span class="sxs-lookup"><span data-stu-id="6847b-1073">A duplicate value was detected on a unique multi-valued column after the data was normalized, and it is normalizing truncated the data before comparison.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1074">JET_errDerivedColumnCorruption-1529</span><span class="sxs-lookup"><span data-stu-id="6847b-1074">JET_errDerivedColumnCorruption -1529</span></span></p></td>
<td><p><span data-ttu-id="6847b-1075">Il existe une colonne non valide dans la table dérivée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1075">There is an invalid column in derived table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1076">JET_errInvalidPlaceholderColumn-1530</span><span class="sxs-lookup"><span data-stu-id="6847b-1076">JET_errInvalidPlaceholderColumn -1530</span></span></p></td>
<td><p><span data-ttu-id="6847b-1077">Une tentative de conversion d’une colonne en espace réservé d’index principal a été effectuée, mais la colonne ne répond pas aux critères requis.</span><span class="sxs-lookup"><span data-stu-id="6847b-1077">An attempt was made to convert a column to a primary index placeholder, but the column does not meet the necessary criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1078">JET_errRecordNotFound-1601</span><span class="sxs-lookup"><span data-stu-id="6847b-1078">JET_errRecordNotFound -1601</span></span></p></td>
<td><p><span data-ttu-id="6847b-1079">La clé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6847b-1079">The key was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1080">JET_errRecordNoCopy-1602</span><span class="sxs-lookup"><span data-stu-id="6847b-1080">JET_errRecordNoCopy -1602</span></span></p></td>
<td><p><span data-ttu-id="6847b-1081">Il n’existe aucune mémoire tampon de travail.</span><span class="sxs-lookup"><span data-stu-id="6847b-1081">There is no working buffer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1082">JET_errNoCurrentRecord-1603</span><span class="sxs-lookup"><span data-stu-id="6847b-1082">JET_errNoCurrentRecord -1603</span></span></p></td>
<td><p><span data-ttu-id="6847b-1083">Aucun enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="6847b-1083">There is no current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1084">JET_errRecordPrimaryChanged-1604</span><span class="sxs-lookup"><span data-stu-id="6847b-1084">JET_errRecordPrimaryChanged -1604</span></span></p></td>
<td><p><span data-ttu-id="6847b-1085">La clé primaire n’est peut-être pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1085">The primary key might not change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1086">JET_errKeyDuplicate-1605</span><span class="sxs-lookup"><span data-stu-id="6847b-1086">JET_errKeyDuplicate -1605</span></span></p></td>
<td><p><span data-ttu-id="6847b-1087">Une clé dupliquée est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6847b-1087">There is an illegal duplicate key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1088">JET_errAlreadyPrepared-1607</span><span class="sxs-lookup"><span data-stu-id="6847b-1088">JET_errAlreadyPrepared -1607</span></span></p></td>
<td><p><span data-ttu-id="6847b-1089">Une tentative a été effectuée pour mettre à jour un enregistrement alors qu’une mise à jour d’enregistrement était déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="6847b-1089">An attempt was made to update a record while a record update was already in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1090">JET_errKeyNotMade-1608</span><span class="sxs-lookup"><span data-stu-id="6847b-1090">JET_errKeyNotMade -1608</span></span></p></td>
<td><p><span data-ttu-id="6847b-1091">Aucun appel n’a été effectué à <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="6847b-1091">A call was not made to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1092">JET_errUpdateNotPrepared-1609</span><span class="sxs-lookup"><span data-stu-id="6847b-1092">JET_errUpdateNotPrepared -1609</span></span></p></td>
<td><p><span data-ttu-id="6847b-1093">Aucun appel n’a été effectué à <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="6847b-1093">A call was not made to <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1094">JET_errDataHasChanged-1611</span><span class="sxs-lookup"><span data-stu-id="6847b-1094">JET_errDataHasChanged -1611</span></span></p></td>
<td><p><span data-ttu-id="6847b-1095">Les données ont changé et l’opération a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1095">The data has changed and the operation was aborted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1096">JET_errLanguageNotSupported-1619</span><span class="sxs-lookup"><span data-stu-id="6847b-1096">JET_errLanguageNotSupported -1619</span></span></p></td>
<td><p><span data-ttu-id="6847b-1097">Cette installation de Windows ne prend pas en charge la langue sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1097">This Windows installation does not support the selected language.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1098">JET_errTooManySorts-1701</span><span class="sxs-lookup"><span data-stu-id="6847b-1098">JET_errTooManySorts -1701</span></span></p></td>
<td><p><span data-ttu-id="6847b-1099">Le nombre de processus de tri est trop important.</span><span class="sxs-lookup"><span data-stu-id="6847b-1099">There are too many sort processes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1100">JET_errInvalidOnSort-1702</span><span class="sxs-lookup"><span data-stu-id="6847b-1100">JET_errInvalidOnSort -1702</span></span></p></td>
<td><p><span data-ttu-id="6847b-1101">Une opération non valide s’est produite pendant un tri.</span><span class="sxs-lookup"><span data-stu-id="6847b-1101">An invalid operation occurred during a sort.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1102">JET_errTempFileOpenError-1803</span><span class="sxs-lookup"><span data-stu-id="6847b-1102">JET_errTempFileOpenError -1803</span></span></p></td>
<td><p><span data-ttu-id="6847b-1103">Impossible d’ouvrir le fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="6847b-1103">The temporary file could not be opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1104">JET_errTooManyAttachedDatabases-1805</span><span class="sxs-lookup"><span data-stu-id="6847b-1104">JET_errTooManyAttachedDatabases -1805</span></span></p></td>
<td><p><span data-ttu-id="6847b-1105">Un trop grand nombre de bases de données sont ouvertes.</span><span class="sxs-lookup"><span data-stu-id="6847b-1105">Too many databases are open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1106">JET_errDiskFull-1808</span><span class="sxs-lookup"><span data-stu-id="6847b-1106">JET_errDiskFull -1808</span></span></p></td>
<td><p><span data-ttu-id="6847b-1107">Il n’y a pas d’espace disponible sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6847b-1107">There is no space left on disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1108">JET_errPermissionDenied-1809</span><span class="sxs-lookup"><span data-stu-id="6847b-1108">JET_errPermissionDenied -1809</span></span></p></td>
<td><p><span data-ttu-id="6847b-1109">Autorisation refusée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1109">Permission is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1110">JET_errFileNotFound-1811</span><span class="sxs-lookup"><span data-stu-id="6847b-1110">JET_errFileNotFound -1811</span></span></p></td>
<td><p><span data-ttu-id="6847b-1111">Ce fichier est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6847b-1111">The file was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1112">JET_errFileInvalidType-1812</span><span class="sxs-lookup"><span data-stu-id="6847b-1112">JET_errFileInvalidType -1812</span></span></p></td>
<td><p><span data-ttu-id="6847b-1113">Le type de fichier n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-1113">The file type is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1114">JET_errAfterInitialization-1850</span><span class="sxs-lookup"><span data-stu-id="6847b-1114">JET_errAfterInitialization -1850</span></span></p></td>
<td><p><span data-ttu-id="6847b-1115">Une restauration ne peut pas être démarrée après l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-1115">A restore cannot be started after initialization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1116">JET_errLogCorrupted-1852</span><span class="sxs-lookup"><span data-stu-id="6847b-1116">JET_errLogCorrupted -1852</span></span></p></td>
<td><p><span data-ttu-id="6847b-1117">Les journaux n’ont pas pu être interprétés.</span><span class="sxs-lookup"><span data-stu-id="6847b-1117">The logs could not be interpreted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1118">JET_errInvalidOperation-1906</span><span class="sxs-lookup"><span data-stu-id="6847b-1118">JET_errInvalidOperation -1906</span></span></p></td>
<td><p><span data-ttu-id="6847b-1119">L’opération n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-1119">The operation is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1120">JET_errAccessDenied-1907</span><span class="sxs-lookup"><span data-stu-id="6847b-1120">JET_errAccessDenied -1907</span></span></p></td>
<td><p><span data-ttu-id="6847b-1121">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="6847b-1121">Access is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1122">JET_errTooManySplits-1909</span><span class="sxs-lookup"><span data-stu-id="6847b-1122">JET_errTooManySplits -1909</span></span></p></td>
<td><p><span data-ttu-id="6847b-1123">Fractionnement infini.</span><span class="sxs-lookup"><span data-stu-id="6847b-1123">An infinite split.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1124">JET_errSessionSharingViolation-1910</span><span class="sxs-lookup"><span data-stu-id="6847b-1124">JET_errSessionSharingViolation -1910</span></span></p></td>
<td><p><span data-ttu-id="6847b-1125">Plusieurs threads utilisent la même session.</span><span class="sxs-lookup"><span data-stu-id="6847b-1125">Multiple threads are using the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1126">JET_errEntryPointNotFound-1911</span><span class="sxs-lookup"><span data-stu-id="6847b-1126">JET_errEntryPointNotFound -1911</span></span></p></td>
<td><p><span data-ttu-id="6847b-1127">Impossible de trouver un point d’entrée dans une DLL requise.</span><span class="sxs-lookup"><span data-stu-id="6847b-1127">An entry point in a required DLL could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1128">JET_errSessionContextAlreadySet-1912</span><span class="sxs-lookup"><span data-stu-id="6847b-1128">JET_errSessionContextAlreadySet -1912</span></span></p></td>
<td><p><span data-ttu-id="6847b-1129">La session spécifiée a déjà un contexte de session défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-1129">The specified session already has a session context set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1130">JET_errSessionContextNotSetByThisThread-1913</span><span class="sxs-lookup"><span data-stu-id="6847b-1130">JET_errSessionContextNotSetByThisThread -1913</span></span></p></td>
<td><p><span data-ttu-id="6847b-1131">Une tentative de réinitialisation du contexte de session a été effectuée, mais le thread actuel n’était pas celui d’origine qui définit le contexte de session.</span><span class="sxs-lookup"><span data-stu-id="6847b-1131">An attempt was made to reset the session context, but the current thread was not the original one that set the session context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1132">JET_errSessionInUse-1914</span><span class="sxs-lookup"><span data-stu-id="6847b-1132">JET_errSessionInUse -1914</span></span></p></td>
<td><p><span data-ttu-id="6847b-1133">Une tentative a été effectuée pour mettre fin à la session en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6847b-1133">An attempt was made to terminate the session currently in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1134">JET_errRecordFormatConversionFailed-1915</span><span class="sxs-lookup"><span data-stu-id="6847b-1134">JET_errRecordFormatConversionFailed -1915</span></span></p></td>
<td><p><span data-ttu-id="6847b-1135">Une erreur interne s’est produite lors d’une conversion de format d’enregistrement dynamique.</span><span class="sxs-lookup"><span data-stu-id="6847b-1135">An internal error occurred during a dynamic record format conversion.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1136">JET_errOneDatabasePerSession-1916</span><span class="sxs-lookup"><span data-stu-id="6847b-1136">JET_errOneDatabasePerSession -1916</span></span></p></td>
<td><p><span data-ttu-id="6847b-1137">Une seule base de données utilisateur ouverte par session est autorisée (comme indiqué par la définition de l’indicateur <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> lors de la création de la base de données).</span><span class="sxs-lookup"><span data-stu-id="6847b-1137">Only one open user database per session is allowed (as indicated by setting the <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> flag during database creation).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1138">JET_errRollbackError-1917</span><span class="sxs-lookup"><span data-stu-id="6847b-1138">JET_errRollbackError -1917</span></span></p></td>
<td><p><span data-ttu-id="6847b-1139">Une erreur s’est produite lors de la restauration.</span><span class="sxs-lookup"><span data-stu-id="6847b-1139">There was an error during rollback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1140">JET_errCallbackFailed-2101</span><span class="sxs-lookup"><span data-stu-id="6847b-1140">JET_errCallbackFailed -2101</span></span></p></td>
<td><p><span data-ttu-id="6847b-1141">Un appel de fonction de rappel a échoué.</span><span class="sxs-lookup"><span data-stu-id="6847b-1141">A callback function call failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1142">JET_errCallbackNotResolved-2102</span><span class="sxs-lookup"><span data-stu-id="6847b-1142">JET_errCallbackNotResolved -2102</span></span></p></td>
<td><p><span data-ttu-id="6847b-1143">Impossible de trouver une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="6847b-1143">A callback function could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1144">JET_errOSSnapshotInvalidSequence-2401</span><span class="sxs-lookup"><span data-stu-id="6847b-1144">JET_errOSSnapshotInvalidSequence -2401</span></span></p></td>
<td><p><span data-ttu-id="6847b-1145">L’API de cliché instantané du système d’exploitation a été utilisée dans une séquence non valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-1145">The operating system shadow copy API was used in an invalid sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1146">JET_errOSSnapshotTimeOut-2402</span><span class="sxs-lookup"><span data-stu-id="6847b-1146">JET_errOSSnapshotTimeOut -2402</span></span></p></td>
<td><p><span data-ttu-id="6847b-1147">Le cliché instantané du système d’exploitation s’est terminé avec un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="6847b-1147">The operating system shadow copy ended with a time-out.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1148">JET_errOSSnapshotNotAllowed-2403</span><span class="sxs-lookup"><span data-stu-id="6847b-1148">JET_errOSSnapshotNotAllowed -2403</span></span></p></td>
<td><p><span data-ttu-id="6847b-1149">Le cliché instantané du système d’exploitation n’est pas autorisé, car une sauvegarde ou une récupération dans est en cours.</span><span class="sxs-lookup"><span data-stu-id="6847b-1149">The operating system shadow copy is not allowed because a backup or recovery in is progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1150">JET_errOSSnapshotInvalidSnapId-2404</span><span class="sxs-lookup"><span data-stu-id="6847b-1150">JET_errOSSnapshotInvalidSnapId -2404</span></span></p></td>
<td><p><span data-ttu-id="6847b-1151">L’opération a échoué, car le handle de cliché instantané du système d’exploitation spécifié n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="6847b-1151">The operation failed because the specified operating system shadow copy handle was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1152">JET_errLSCallbackNotSpecified-3000</span><span class="sxs-lookup"><span data-stu-id="6847b-1152">JET_errLSCallbackNotSpecified -3000</span></span></p></td>
<td><p><span data-ttu-id="6847b-1153">Une tentative d’utilisation du stockage local a été effectuée sans qu’une fonction de rappel soit spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1153">An attempt was made to use local storage without a callback function being specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1154">JET_errLSAlreadySet-3001</span><span class="sxs-lookup"><span data-stu-id="6847b-1154">JET_errLSAlreadySet -3001</span></span></p></td>
<td><p><span data-ttu-id="6847b-1155">Une tentative a été effectuée pour définir le stockage local pour un objet déjà défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-1155">An attempt was made to set the local storage for an object which already had it set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1156">JET_errLSNotSet-3002</span><span class="sxs-lookup"><span data-stu-id="6847b-1156">JET_errLSNotSet -3002</span></span></p></td>
<td><p><span data-ttu-id="6847b-1157">Une tentative a été effectuée pour récupérer le stockage local d’un objet pour lequel il n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="6847b-1157">An attempt was made to retrieve local storage from an object which did not have it set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1158">JET_errFileIOSparse-4000</span><span class="sxs-lookup"><span data-stu-id="6847b-1158">JET_errFileIOSparse -4000</span></span></p></td>
<td><p><span data-ttu-id="6847b-1159">Une opération d’e/s a échoué, car elle a été tentée sur une zone non allouée d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="6847b-1159">An I/O operation failed because it was attempted against an unallocated region of a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1160">JET_errFileIOBeyondEOF-4001</span><span class="sxs-lookup"><span data-stu-id="6847b-1160">JET_errFileIOBeyondEOF -4001</span></span></p></td>
<td><p><span data-ttu-id="6847b-1161">Une lecture a été émise vers un emplacement situé au-delà de la EOF (les écritures vont développer le fichier).</span><span class="sxs-lookup"><span data-stu-id="6847b-1161">A read was issued to a location beyond the EOF (writes will expand the file).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1162">JET_errFileIOAbort-4002</span><span class="sxs-lookup"><span data-stu-id="6847b-1162">JET_errFileIOAbort -4002</span></span></p></td>
<td><p><span data-ttu-id="6847b-1163">Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK d’abandonner l’e/s spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1163">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to abort the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1164">JET_errFileIORetry-4003</span><span class="sxs-lookup"><span data-stu-id="6847b-1164">JET_errFileIORetry -4003</span></span></p></td>
<td><p><span data-ttu-id="6847b-1165">Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK de retenter l’e/s spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1165">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to retry the specified I/O.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1166">JET_errFileIOFail-4004</span><span class="sxs-lookup"><span data-stu-id="6847b-1166">JET_errFileIOFail -4004</span></span></p></td>
<td><p><span data-ttu-id="6847b-1167">Cet indicateur demande à l’appelant JET_ABORTRETRYFAILCALLBACK d’effectuer l’échec de l’e/s spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6847b-1167">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to fail the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1168">JET_errFileCompressed-4005</span><span class="sxs-lookup"><span data-stu-id="6847b-1168">JET_errFileCompressed -4005</span></span></p></td>
<td><p><span data-ttu-id="6847b-1169">L’accès en lecture/écriture n’est pas pris en charge sur les fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="6847b-1169">Read/write access is not supported on compressed files.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="6847b-1170">Notes</span><span class="sxs-lookup"><span data-stu-id="6847b-1170">Remarks</span></span>

<span data-ttu-id="6847b-1171">En général, une valeur supérieure à zéro doit être interprétée comme un avertissement, une valeur de zéro doit être interprétée comme une réussite et une valeur inférieure à zéro doit être interprétée comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="6847b-1171">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="6847b-1172">Aucun autre modèle dans ces valeurs, comme des plages de valeurs, ne doit être basé sur une application.</span><span class="sxs-lookup"><span data-stu-id="6847b-1172">No other patterns in these values, such as ranges of values, should be relied upon by an application.</span></span>

### <a name="requirements"></a><span data-ttu-id="6847b-1173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6847b-1173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1174"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6847b-1174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6847b-1175">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="6847b-1175">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847b-1176"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6847b-1176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6847b-1177">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6847b-1177">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847b-1178"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6847b-1178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6847b-1179">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6847b-1179">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6847b-1180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6847b-1180">See Also</span></span>

[<span data-ttu-id="6847b-1181">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="6847b-1181">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="6847b-1182">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="6847b-1182">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="6847b-1183">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="6847b-1183">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)
