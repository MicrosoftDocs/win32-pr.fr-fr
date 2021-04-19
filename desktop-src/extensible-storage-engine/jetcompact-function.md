---
description: 'En savoir plus sur : fonction JetCompact'
title: JetCompact fonction)
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523239"
---
# <a name="jetcompact-function"></a><span data-ttu-id="afa83-103">JetCompact fonction)</span><span class="sxs-lookup"><span data-stu-id="afa83-103">JetCompact Function</span></span>


<span data-ttu-id="afa83-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="afa83-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcompact-function"></a><span data-ttu-id="afa83-105">JetCompact fonction)</span><span class="sxs-lookup"><span data-stu-id="afa83-105">JetCompact Function</span></span>

<span data-ttu-id="afa83-106">La fonction **JetCompact** effectue une copie d’une base de données existante.</span><span class="sxs-lookup"><span data-stu-id="afa83-106">The **JetCompact** function makes a copy of an existing database.</span></span> <span data-ttu-id="afa83-107">La copie est compactée dans un état optimal pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="afa83-107">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="afa83-108">Les données dans les données copiées seront empaquetées en fonction des mesures choisies pour les index lors de la création de l’index.</span><span class="sxs-lookup"><span data-stu-id="afa83-108">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="afa83-109">De cette façon, les données compactées peuvent être stockées aussi denses que possible.</span><span class="sxs-lookup"><span data-stu-id="afa83-109">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="afa83-110">Les données compactées peuvent également réserver de l’espace pour la croissance des enregistrements ou les insertions d’index suivantes.</span><span class="sxs-lookup"><span data-stu-id="afa83-110">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="afa83-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afa83-111">Parameters</span></span>

<span data-ttu-id="afa83-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="afa83-112">*sesid*</span></span>

<span data-ttu-id="afa83-113">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="afa83-113">The session to use for this call.</span></span>

<span data-ttu-id="afa83-114">*szDatabaseSrc*</span><span class="sxs-lookup"><span data-stu-id="afa83-114">*szDatabaseSrc*</span></span>

<span data-ttu-id="afa83-115">Base de données source qui sera compactée.</span><span class="sxs-lookup"><span data-stu-id="afa83-115">The source database that will be compacted.</span></span>

<span data-ttu-id="afa83-116">*szDatabaseDest*</span><span class="sxs-lookup"><span data-stu-id="afa83-116">*szDatabaseDest*</span></span>

<span data-ttu-id="afa83-117">Nom à utiliser pour la base de données compactée.</span><span class="sxs-lookup"><span data-stu-id="afa83-117">The name to use for the compacted database.</span></span>

<span data-ttu-id="afa83-118">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="afa83-118">*pfnStatus*</span></span>

<span data-ttu-id="afa83-119">Fonction de rappel qui peut être appelée régulièrement via l’opération de compactage de la base de données pour signaler la progression.</span><span class="sxs-lookup"><span data-stu-id="afa83-119">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<span data-ttu-id="afa83-120">*pconvert*</span><span class="sxs-lookup"><span data-stu-id="afa83-120">*pconvert*</span></span>

<span data-ttu-id="afa83-121">Pointeur utilisé pour désigner une autre DLL ESE pouvant être utilisée pour lire la base de données source et pour fournir des paramètres facultatifs pour une opération **JetCompact** qui convertit une base de données d’un format antérieur à un format de version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="afa83-121">A pointer used to designate an alternative ESE DLL that can be used to read the source database, and to provide optional parameters for a **JetCompact** operation that is converting a database from an earlier to a later version format.</span></span> <span data-ttu-id="afa83-122">Cette fonctionnalité a été supprimée dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="afa83-122">This feature was discontinued in Windows Server 2003.</span></span>

<span data-ttu-id="afa83-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="afa83-123">*grbit*</span></span>

<span data-ttu-id="afa83-124">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="afa83-124">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="afa83-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="afa83-125">Value</span></span></p></th>
<th><p><span data-ttu-id="afa83-126">Signification</span><span class="sxs-lookup"><span data-stu-id="afa83-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afa83-127">JET_bitCompactRepair</span><span class="sxs-lookup"><span data-stu-id="afa83-127">JET_bitCompactRepair</span></span></p></td>
<td><p><span data-ttu-id="afa83-128">Utilisé lorsque la base de données source est endommagée.</span><span class="sxs-lookup"><span data-stu-id="afa83-128">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="afa83-129">Il active un ensemble complet de nouveaux comportements destinés à récupérer autant de données que possible à partir de la base de données source.</span><span class="sxs-lookup"><span data-stu-id="afa83-129">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="afa83-130"><strong>JetCompact</strong> avec ce groupe d’options peut retourner JET_errSuccess mais pas copier toutes les données créées dans la base de données source.</span><span class="sxs-lookup"><span data-stu-id="afa83-130"><strong>JetCompact</strong> with this option set may return JET_errSuccess but not copy all of the data created in the source database.</span></span> <span data-ttu-id="afa83-131">Les données qui étaient dans des parties endommagées de la base de données source seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="afa83-131">Data that was in damaged portions of the source database will be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-132">JET_bitCompactStats</span><span class="sxs-lookup"><span data-stu-id="afa83-132">JET_bitCompactStats</span></span></p></td>
<td><p><span data-ttu-id="afa83-133">Fait en sorte que <strong>JetCompact</strong> vide les statistiques de la base de données source vers un fichier nommé DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="afa83-133">Causes <strong>JetCompact</strong> to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="afa83-134">Les statistiques incluent le nom de chaque table dans la base de données source, le nombre de lignes dans chaque table, la taille totale, en octets, de toutes les lignes de chaque table, la taille totale en octets de toutes les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> qui étaient suffisamment volumineuses pour être stockées séparément de l’enregistrement, le nombre de pages de feuilles d’index cluster et le nombre de pages de</span><span class="sxs-lookup"><span data-stu-id="afa83-134">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="afa83-135">En outre, les statistiques récapitulatives, y compris la taille de la base de données source, la base de données de destination, le temps requis pour le compactage de base de données, l’espace temporaire de la base de données sont également vidées.</span><span class="sxs-lookup"><span data-stu-id="afa83-135">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="afa83-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="afa83-136">Return Value</span></span>

<span data-ttu-id="afa83-137">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="afa83-137">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="afa83-138">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="afa83-138">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="afa83-139">Code de retour</span><span class="sxs-lookup"><span data-stu-id="afa83-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="afa83-140">Description</span><span class="sxs-lookup"><span data-stu-id="afa83-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afa83-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="afa83-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="afa83-142">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="afa83-142">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="afa83-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="afa83-144">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="afa83-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afa83-145">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="afa83-145">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="afa83-146">Un pointeur <em>pconvert</em> non null a été fourni, mais la version de ESE utilisée ne prend pas en charge la fonctionnalité de conversion.</span><span class="sxs-lookup"><span data-stu-id="afa83-146">A non-NULL <em>pconvert</em> pointer has been supplied but the version of ESE being used does not support the convert feature.</span></span> <span data-ttu-id="afa83-147">Cette fonctionnalité a été supprimée dans la version Windows Server 2003 de ESE.</span><span class="sxs-lookup"><span data-stu-id="afa83-147">This feature was removed in the Windows Server 2003 version of ESE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="afa83-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="afa83-149">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="afa83-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="afa83-150">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="afa83-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afa83-151">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="afa83-151">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="afa83-152">La session appelante est dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="afa83-152">The calling session is within a transaction.</span></span> <span data-ttu-id="afa83-153"><strong>JetCompact</strong> doit être appelé par une session en dehors d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="afa83-153"><strong>JetCompact</strong> must be called by a session outside of any transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-154">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="afa83-154">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="afa83-155">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="afa83-155">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afa83-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="afa83-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="afa83-157">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="afa83-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="afa83-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="afa83-159">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="afa83-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="afa83-160">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="afa83-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afa83-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="afa83-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="afa83-162">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="afa83-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="afa83-163">En cas de réussite, la base de données source est copiée dans la base de données de destination.</span><span class="sxs-lookup"><span data-stu-id="afa83-163">On success, the source database is copied to the destination database.</span></span> <span data-ttu-id="afa83-164">La base de données de destination est dans un état optimal, par exemple, tous les index de table se trouvent dans l’espace disque logique adjacent.</span><span class="sxs-lookup"><span data-stu-id="afa83-164">The destination database is in an optimal state, for example, all table indexes are located in adjacent logical disk space.</span></span> <span data-ttu-id="afa83-165">Chaque page d’index est remplie à la quantité configurée lorsque les index ont été créés à l’origine dans la base de données source.</span><span class="sxs-lookup"><span data-stu-id="afa83-165">Each index page is padded to the amount configured when the indexes were originally created in the source database.</span></span> <span data-ttu-id="afa83-166">Tous les paramètres de données et de métadonnées sont copiés avec une fidélité complète, sauf si l’option de réparation a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="afa83-166">All data and metadata settings are copied with full fidelity, unless the repair option was specified.</span></span> <span data-ttu-id="afa83-167">Si l’option de réparation a été spécifiée, certaines données de la base de données source n’ont peut-être pas été copiées.</span><span class="sxs-lookup"><span data-stu-id="afa83-167">If the repair option was specified, some data from the source database may not have been copied.</span></span>

<span data-ttu-id="afa83-168">En cas d’échec, la base de données de destination peut exister, mais n’est pas une copie complète de la base de données source.</span><span class="sxs-lookup"><span data-stu-id="afa83-168">On failure, the destination database may exist but is not a full copy of the source database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="afa83-169">Notes</span><span class="sxs-lookup"><span data-stu-id="afa83-169">Remarks</span></span>

<span data-ttu-id="afa83-170">Le compactage d’une base de données est également utilisé pour mettre à niveau une base de données d’un format de version antérieure vers une version plus moderne.</span><span class="sxs-lookup"><span data-stu-id="afa83-170">Compacting a database is also used to upgrade a database from an earlier version format to a more modern version.</span></span> <span data-ttu-id="afa83-171">Un paramètre facultatif est *pconvert*, qui contient une structure qui peut contenir une description d’une dll de version antérieure à utiliser pour la lecture du format de base de données source.</span><span class="sxs-lookup"><span data-stu-id="afa83-171">An optional parameter is *pconvert*, which contains a structure that can hold a description for an earlier version DLL to use for reading the source database format.</span></span> <span data-ttu-id="afa83-172">Cette fonctionnalité a été supprimée dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="afa83-172">This feature was discontinued in Windows Server 2003.</span></span> <span data-ttu-id="afa83-173">À la suite de Windows Server 2003, les nouvelles versions de ESE sont toujours en mesure de lire les anciennes versions du format de base de données. par conséquent, cette fonctionnalité n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="afa83-173">Subsequent to Windows Server 2003, new versions of ESE are always able to read older versions of the database format and hence this feature is not needed.</span></span>

<span data-ttu-id="afa83-174">La densité de données souhaitée après une opération compact est spécifiée lors de la création de tables et d’index.</span><span class="sxs-lookup"><span data-stu-id="afa83-174">The desired density of data after a compact operation is specified when tables and indexes are created.</span></span> <span data-ttu-id="afa83-175">La densité doit être comprise entre 20% et 100%.</span><span class="sxs-lookup"><span data-stu-id="afa83-175">The density must be between 20% and 100%.</span></span> <span data-ttu-id="afa83-176">Si une base de données est principalement lue et non mise à jour, les applications définissent la densité à 100% pour réduire le nombre d’opérations d’e/s lors du traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="afa83-176">If a database is primarily read and not updated, applications will set the density to 100% to reduce the number of I/O operations during query processing.</span></span> <span data-ttu-id="afa83-177">Toutefois, si les données sont fréquemment mises à jour avec des opérations qui augmentent la taille des données stockées avec l’enregistrement, ou si de nouvelles données sont fréquemment insérées, l’application choisit une densité inférieure afin que les mises à jour trouvent les ressources nécessaires disponibles.</span><span class="sxs-lookup"><span data-stu-id="afa83-177">However, if the data is updated frequently with operations that increase the size of data stored together with the record, or new data is frequently inserted, the application will choose a lower density so that updates will more often find needed resources available.</span></span> <span data-ttu-id="afa83-178">Le fait de compacter la base de données rend la base de données idéalement imposée en fonction du remplissage choisi par l’application.</span><span class="sxs-lookup"><span data-stu-id="afa83-178">The operation of compacting the database causes the database to be ideally laid out according to the fill chosen by the application.</span></span>

<span data-ttu-id="afa83-179">Le compactage de base de données est une opération hors connexion.</span><span class="sxs-lookup"><span data-stu-id="afa83-179">Database compaction is an off-line operation.</span></span> <span data-ttu-id="afa83-180">Elle ne peut pas être effectuée tant que la base de données est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="afa83-180">It cannot be performed while the database is in use.</span></span> <span data-ttu-id="afa83-181">En conséquence, elle est généralement effectuée dans le cadre d’un processus de génération de développement d’une application qui remet un jeu de données dans le cadre d’elle-même.</span><span class="sxs-lookup"><span data-stu-id="afa83-181">As a result, it is typically done as part of a build process of developing an application which delivers a data set as part of itself.</span></span>

<span data-ttu-id="afa83-182">La compression de la base de données hors connexion touche chaque bit de données dans une base de données et peut être utilisée pour vérifier la cohérence d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="afa83-182">Offline database compaction touches every bit of data in a database and can be used as a means of checking the consistency of a database.</span></span> <span data-ttu-id="afa83-183">Si une base de données est suspecte, elle peut être compactée.</span><span class="sxs-lookup"><span data-stu-id="afa83-183">If a database is suspect then it can be compacted.</span></span> <span data-ttu-id="afa83-184">Si aucune erreur n’est détectée dans le compactage, il est connu que la base de données est dans un état valide pour ESE.</span><span class="sxs-lookup"><span data-stu-id="afa83-184">If no error is found from compaction then it will be known that the database is in a valid state for ESE.</span></span>

#### <a name="requirements"></a><span data-ttu-id="afa83-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afa83-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afa83-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="afa83-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="afa83-187">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="afa83-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-188"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="afa83-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="afa83-189">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="afa83-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afa83-190"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="afa83-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="afa83-191">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="afa83-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-192"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="afa83-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="afa83-193">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="afa83-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afa83-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="afa83-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="afa83-195">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="afa83-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa83-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="afa83-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="afa83-197">Implémenté en tant que <strong>JetCompactW</strong> (Unicode) et <strong>JetCompactA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="afa83-197">Implemented as <strong>JetCompactW</strong> (Unicode) and <strong>JetCompactA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="afa83-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afa83-198">See Also</span></span>

[<span data-ttu-id="afa83-199">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="afa83-199">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="afa83-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="afa83-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="afa83-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="afa83-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="afa83-202">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="afa83-202">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="afa83-203">JetStopService</span><span class="sxs-lookup"><span data-stu-id="afa83-203">JetStopService</span></span>](./jetstopservice-function.md)
