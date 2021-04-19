---
description: 'En savoir plus sur : fonction JetCreateDatabase2'
title: Fonction JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521904"
---
# <a name="jetcreatedatabase2-function"></a><span data-ttu-id="6a32f-103">Fonction JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="6a32f-103">JetCreateDatabase2 Function</span></span>


<span data-ttu-id="6a32f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6a32f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase2-function"></a><span data-ttu-id="6a32f-105">Fonction JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="6a32f-105">JetCreateDatabase2 Function</span></span>

<span data-ttu-id="6a32f-106">La fonction **JetCreateDatabase2** crée et attache un fichier de base de données à utiliser avec le moteur de base de données ESE avec une taille de base de données maximale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6a32f-106">The **JetCreateDatabase2** function creates and attaches a database file to be used with the ESE database engine with a maximum database size specified.</span></span> <span data-ttu-id="6a32f-107">L’appel de **JetCreateDatabase2** avec *cpgDatabaseSizeMax* défini à zéro est identique à l’appel de [JETCREATEDATABASE](./jetcreatedatabase-function.md) avec *szConnect* défini sur null.</span><span class="sxs-lookup"><span data-stu-id="6a32f-107">Calling **JetCreateDatabase2** with *cpgDatabaseSizeMax* set to zero is identical to calling [JetCreateDatabase](./jetcreatedatabase-function.md) with *szConnect* set to NULL.</span></span> <span data-ttu-id="6a32f-108">Il est actuellement possible de créer jusqu’à sept bases de données par instance.</span><span class="sxs-lookup"><span data-stu-id="6a32f-108">Currently up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6a32f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a32f-109">Parameters</span></span>

<span data-ttu-id="6a32f-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6a32f-110">*sesid*</span></span>

<span data-ttu-id="6a32f-111">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="6a32f-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="6a32f-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="6a32f-112">*szFilename*</span></span>

<span data-ttu-id="6a32f-113">Nom de la base de données à créer.</span><span class="sxs-lookup"><span data-stu-id="6a32f-113">The name of the database to be created.</span></span>

<span data-ttu-id="6a32f-114">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="6a32f-114">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="6a32f-115">Taille maximale, en pages de base de données, pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="6a32f-115">The maximum size, in database pages, for the database.</span></span> <span data-ttu-id="6a32f-116">La taille de page de la base de données par défaut est de 4 kilo-octets et peut être modifiée avec [JetSetSystemParameter](./jetsetsystemparameter-function.md) avant de créer une base de données.</span><span class="sxs-lookup"><span data-stu-id="6a32f-116">The default database page size is 4 kilobytes, and can be changed with [JetSetSystemParameter](./jetsetsystemparameter-function.md) prior to creating a database.</span></span>

<span data-ttu-id="6a32f-117">Le fait de passer la valeur zéro signifie qu’il n’y a pas de valeur maximale appliquée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="6a32f-117">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="6a32f-118">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="6a32f-118">*pdbid*</span></span>

<span data-ttu-id="6a32f-119">Pointeur vers une mémoire tampon qui, sur un appel réussi, contient l’identificateur de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6a32f-119">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="6a32f-120">En cas d’échec, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="6a32f-120">On failure, the value is undefined.</span></span>

<span data-ttu-id="6a32f-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6a32f-121">*grbit*</span></span>

<span data-ttu-id="6a32f-122">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a32f-122">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a32f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a32f-123">Value</span></span></p></th>
<th><p><span data-ttu-id="6a32f-124">Signification</span><span class="sxs-lookup"><span data-stu-id="6a32f-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-125">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="6a32f-125">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="6a32f-126">Par défaut, si <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> ou <strong>JetCreateDatabase2</strong> est appelé et que la base de données existe déjà, l’appel d’API échoue et la base de données d’origine n’est pas remplacée.</span><span class="sxs-lookup"><span data-stu-id="6a32f-126">By default, if <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> or <strong>JetCreateDatabase2</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="6a32f-127">JET_bitDbOverwriteExisting modifie ce comportement et l’ancienne base de données sera remplacée par une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="6a32f-127">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="6a32f-128">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6a32f-128">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-129">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="6a32f-129">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="6a32f-130">JET_bitDbRecoveryOff désactive la journalisation.</span><span class="sxs-lookup"><span data-stu-id="6a32f-130">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="6a32f-131">La définition de ce bit perd la possibilité de relire les fichiers journaux et de récupérer la base de données à un État utilisable cohérent après un événement catastrophique.</span><span class="sxs-lookup"><span data-stu-id="6a32f-131">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-132">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="6a32f-132">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="6a32f-133">La définition de JET_bitDbShadowingOff désactive la duplication de certaines structures de base de données internes (occultation).</span><span class="sxs-lookup"><span data-stu-id="6a32f-133">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="6a32f-134">La duplication de ces structures étant effectuée à des fins de résilience, la définition de JET_bitDbShadowingOff supprime cette résilience.</span><span class="sxs-lookup"><span data-stu-id="6a32f-134">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6a32f-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a32f-135">Return Value</span></span>

<span data-ttu-id="6a32f-136">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="6a32f-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6a32f-137">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6a32f-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a32f-138">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6a32f-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="6a32f-139">Description</span><span class="sxs-lookup"><span data-stu-id="6a32f-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6a32f-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6a32f-141">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6a32f-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-142">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="6a32f-142">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="6a32f-143">La base de données nommée dans <em>szFilename</em> existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6a32f-143">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="6a32f-144">Lorsque cette erreur est retournée, la base de données n’est pas attachée.</span><span class="sxs-lookup"><span data-stu-id="6a32f-144">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-145">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="6a32f-145">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="6a32f-146">Peut être retourné si l’accès exclusif a été demandé, mais n’a pas pu être accordé, ou si une autre session a déjà ouvert la base de données en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="6a32f-146">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-147">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="6a32f-147">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="6a32f-148">Retourné lorsque <em>cpgDatabaseSizeMax</em> est plus grand que le nombre maximal de pages autorisées dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="6a32f-148">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="6a32f-149">La valeur maximale actuelle est 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="6a32f-149">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-150">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6a32f-150">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="6a32f-151">Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="6a32f-151">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="6a32f-152"><em>szFilename</em> doit être non null.</span><span class="sxs-lookup"><span data-stu-id="6a32f-152"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="6a32f-153">Par défaut, <em>szFilename</em> doit pointer vers un répertoire existant.</span><span class="sxs-lookup"><span data-stu-id="6a32f-153">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="6a32f-154">Le chemin d’accès est créé si <em>JET_paramCreatePathIfNotExist</em> est défini (voir <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="6a32f-154">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-155">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="6a32f-155">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="6a32f-156">Indique qu’une autre session a déjà ouvert la base de données en mode exclusif (à l’aide de JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="6a32f-156">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-157">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="6a32f-157">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="6a32f-158">La base de données n’a pas été attachée précédemment (voir <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="6a32f-158">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-159">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6a32f-159">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6a32f-160">Le fichier de base de données a déjà été attaché par une autre session.</span><span class="sxs-lookup"><span data-stu-id="6a32f-160">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-161">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="6a32f-161">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6a32f-162">Une tentative a été effectuée pour créer une base de données dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="6a32f-162">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-163">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="6a32f-163">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="6a32f-164">Une tentative a été effectuée pour ouvrir un fichier qui n’est pas un fichier de base de données valide.</span><span class="sxs-lookup"><span data-stu-id="6a32f-164">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-165">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="6a32f-165">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="6a32f-166">Une tentative a été effectuée pour ouvrir plus d’une base de données et JET_paramOneDatabasePerSession a été définie.</span><span class="sxs-lookup"><span data-stu-id="6a32f-166">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="6a32f-167">Consultez <a href="gg294139(v=exchg.10).md">paramètres système</a>.</span><span class="sxs-lookup"><span data-stu-id="6a32f-167">See <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-168">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6a32f-168">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="6a32f-169">Les ressources du système sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="6a32f-169">The system ran low on resources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-170">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="6a32f-170">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="6a32f-171">Seul un nombre fini de bases de données peut être attaché par instance.</span><span class="sxs-lookup"><span data-stu-id="6a32f-171">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="6a32f-172">La limite est actuellement de sept bases de données par instance.</span><span class="sxs-lookup"><span data-stu-id="6a32f-172">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-173">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="6a32f-173">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="6a32f-174">AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</span><span class="sxs-lookup"><span data-stu-id="6a32f-174">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-175">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="6a32f-175">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6a32f-176">JET_wrnFileOpenReadOnly indique que le fichier a été attaché en lecture seule, mais <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> n’a pas réussi JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="6a32f-176">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="6a32f-177">La base de données est toujours ouverte avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a32f-177">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6a32f-178">Notes</span><span class="sxs-lookup"><span data-stu-id="6a32f-178">Remarks</span></span>

<span data-ttu-id="6a32f-179">Si la base de données spécifiée dans *szFilename* existe et que JET_bitDbOverwriteExisting n’a pas été transmis, l’appel de l’API échoue.</span><span class="sxs-lookup"><span data-stu-id="6a32f-179">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="6a32f-180">Si JET_bitDbOverwriteExisting a été transmis, l’ancien fichier de base de données sera d’abord supprimé.</span><span class="sxs-lookup"><span data-stu-id="6a32f-180">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="6a32f-181">Si l’API crée un fichier de base de données, puis accède à une autre erreur, il nettoie et supprime le fichier.</span><span class="sxs-lookup"><span data-stu-id="6a32f-181">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="6a32f-182">**JetCreateDatabase2** ouvre implicitement la base de données.</span><span class="sxs-lookup"><span data-stu-id="6a32f-182">**JetCreateDatabase2** will implicitly open the database.</span></span> <span data-ttu-id="6a32f-183">Il n’est pas nécessaire d’appeler ensuite [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="6a32f-183">It is not necessary to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="6a32f-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a32f-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-185"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6a32f-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6a32f-186">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="6a32f-186">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-187"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6a32f-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6a32f-188">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6a32f-188">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-189"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6a32f-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6a32f-190">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6a32f-190">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-191"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="6a32f-191"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6a32f-192">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6a32f-192">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a32f-193"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6a32f-193"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6a32f-194">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6a32f-194">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a32f-195"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6a32f-195"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6a32f-196">Implémenté en tant que <strong>JetCreateDatabase2W</strong> (Unicode) et <strong>JetCreateDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6a32f-196">Implemented as <strong>JetCreateDatabase2W</strong> (Unicode) and <strong>JetCreateDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6a32f-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a32f-197">See Also</span></span>

[<span data-ttu-id="6a32f-198">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="6a32f-198">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="6a32f-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6a32f-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6a32f-200">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6a32f-200">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="6a32f-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6a32f-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6a32f-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6a32f-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6a32f-203">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="6a32f-203">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="6a32f-204">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="6a32f-204">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="6a32f-205">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="6a32f-205">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="6a32f-206">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="6a32f-206">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="6a32f-207">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6a32f-207">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6a32f-208">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="6a32f-208">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
