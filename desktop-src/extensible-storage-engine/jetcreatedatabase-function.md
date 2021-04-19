---
description: 'En savoir plus sur : fonction JetCreateDatabase'
title: Fonction JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529870"
---
# <a name="jetcreatedatabase-function"></a><span data-ttu-id="9dffe-103">Fonction JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="9dffe-103">JetCreateDatabase Function</span></span>


<span data-ttu-id="9dffe-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9dffe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase-function"></a><span data-ttu-id="9dffe-105">Fonction JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="9dffe-105">JetCreateDatabase Function</span></span>

<span data-ttu-id="9dffe-106">La fonction **JetCreateDatabase** crée et attache un fichier de base de données à utiliser avec le moteur de base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="9dffe-106">The **JetCreateDatabase** function creates and attaches a database file to be used with the ESE database engine.</span></span> <span data-ttu-id="9dffe-107">L’appel de [JetCreateDatabase2](./jetcreatedatabase2-function.md) avec *cpgDatabaseSizeMax* défini à zéro est identique à l’appel de **JETCREATEDATABASE** avec *szConnect* défini sur null.</span><span class="sxs-lookup"><span data-stu-id="9dffe-107">Calling [JetCreateDatabase2](./jetcreatedatabase2-function.md) with *cpgDatabaseSizeMax* set to zero is identical to calling **JetCreateDatabase** with *szConnect* set to NULL.</span></span> <span data-ttu-id="9dffe-108">Actuellement, jusqu’à sept bases de données peuvent être créées par instance.</span><span class="sxs-lookup"><span data-stu-id="9dffe-108">Currently, up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9dffe-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9dffe-109">Parameters</span></span>

<span data-ttu-id="9dffe-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9dffe-110">*sesid*</span></span>

<span data-ttu-id="9dffe-111">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="9dffe-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="9dffe-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="9dffe-112">*szFilename*</span></span>

<span data-ttu-id="9dffe-113">Nom de la base de données à créer.</span><span class="sxs-lookup"><span data-stu-id="9dffe-113">The name of the database to be created.</span></span>

<span data-ttu-id="9dffe-114">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="9dffe-114">*szConnect*</span></span>

<span data-ttu-id="9dffe-115">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="9dffe-115">Reserved for future use.</span></span> <span data-ttu-id="9dffe-116">valeur de l’en-tête définie sur Null.</span><span class="sxs-lookup"><span data-stu-id="9dffe-116">Set to NULL.</span></span>

<span data-ttu-id="9dffe-117">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="9dffe-117">*pdbid*</span></span>

<span data-ttu-id="9dffe-118">Pointeur vers une mémoire tampon qui, sur un appel réussi, contient l’identificateur de la base de données.</span><span class="sxs-lookup"><span data-stu-id="9dffe-118">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="9dffe-119">En cas d’échec, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="9dffe-119">On failure, the value is undefined.</span></span>

<span data-ttu-id="9dffe-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9dffe-120">*grbit*</span></span>

<span data-ttu-id="9dffe-121">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="9dffe-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9dffe-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dffe-122">Value</span></span></p></th>
<th><p><span data-ttu-id="9dffe-123">Signification</span><span class="sxs-lookup"><span data-stu-id="9dffe-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-124">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="9dffe-124">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="9dffe-125">Par défaut, si <strong>JetCreateDatabase</strong> est appelé et que la base de données existe déjà, l’appel d’API échoue et la base de données d’origine n’est pas remplacée.</span><span class="sxs-lookup"><span data-stu-id="9dffe-125">By default, if <strong>JetCreateDatabase</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="9dffe-126">JET_bitDbOverwriteExisting modifie ce comportement et l’ancienne base de données sera remplacée par une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="9dffe-126">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="9dffe-127">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9dffe-127">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-128">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="9dffe-128">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="9dffe-129">JET_bitDbRecoveryOff désactive la journalisation.</span><span class="sxs-lookup"><span data-stu-id="9dffe-129">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="9dffe-130">La définition de ce bit perd la possibilité de relire les fichiers journaux et de récupérer la base de données à un État utilisable cohérent après un événement catastrophique.</span><span class="sxs-lookup"><span data-stu-id="9dffe-130">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-131">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="9dffe-131">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="9dffe-132">La définition de JET_bitDbShadowingOff désactive la duplication de certaines structures de base de données internes (occultation).</span><span class="sxs-lookup"><span data-stu-id="9dffe-132">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="9dffe-133">La duplication de ces structures étant effectuée à des fins de résilience, la définition de JET_bitDbShadowingOff supprime cette résilience.</span><span class="sxs-lookup"><span data-stu-id="9dffe-133">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9dffe-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9dffe-134">Return Value</span></span>

<span data-ttu-id="9dffe-135">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="9dffe-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9dffe-136">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9dffe-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9dffe-137">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9dffe-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="9dffe-138">Description</span><span class="sxs-lookup"><span data-stu-id="9dffe-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9dffe-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9dffe-140">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="9dffe-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-141">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="9dffe-141">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="9dffe-142">La base de données nommée dans <em>szFilename</em> existe déjà.</span><span class="sxs-lookup"><span data-stu-id="9dffe-142">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="9dffe-143">Lorsque cette erreur est retournée, la base de données n’est pas attachée.</span><span class="sxs-lookup"><span data-stu-id="9dffe-143">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="9dffe-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="9dffe-145">Peut être retourné si l’accès exclusif a été demandé, mais n’a pas pu être accordé, ou si une autre session a déjà ouvert la base de données en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="9dffe-145">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-146">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="9dffe-146">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="9dffe-147">Retourné lorsque <em>cpgDatabaseSizeMax</em> est plus grand que le nombre maximal de pages autorisées dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="9dffe-147">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="9dffe-148">La valeur maximale actuelle est 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="9dffe-148">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-149">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="9dffe-149">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="9dffe-150">Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="9dffe-150">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="9dffe-151"><em>szFilename</em> doit être non null.</span><span class="sxs-lookup"><span data-stu-id="9dffe-151"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="9dffe-152">Par défaut, <em>szFilename</em> doit pointer vers un répertoire existant.</span><span class="sxs-lookup"><span data-stu-id="9dffe-152">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="9dffe-153">Le chemin d’accès est créé si <em>JET_paramCreatePathIfNotExist</em> est défini (voir <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="9dffe-153">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-154">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="9dffe-154">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="9dffe-155">Indique qu’une autre session a déjà ouvert la base de données en mode exclusif (à l’aide de JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="9dffe-155">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-156">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="9dffe-156">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="9dffe-157">La base de données n’a pas été attachée précédemment (voir <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="9dffe-157">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-158">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9dffe-158">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9dffe-159">Le fichier de base de données a déjà été attaché par une autre session.</span><span class="sxs-lookup"><span data-stu-id="9dffe-159">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-160">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="9dffe-160">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="9dffe-161">Une tentative a été effectuée pour créer une base de données dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="9dffe-161">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-162">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="9dffe-162">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="9dffe-163">Une tentative a été effectuée pour ouvrir un fichier qui n’est pas un fichier de base de données valide.</span><span class="sxs-lookup"><span data-stu-id="9dffe-163">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-164">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="9dffe-164">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="9dffe-165">Une tentative a été effectuée pour ouvrir plus d’une base de données et JET_paramOneDatabasePerSession a été définie.</span><span class="sxs-lookup"><span data-stu-id="9dffe-165">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="9dffe-166">Consultez <a href="gg269337(v=exchg.10).md">paramètres de la base de données</a>.</span><span class="sxs-lookup"><span data-stu-id="9dffe-166">See <a href="gg269337(v=exchg.10).md">Database Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-167">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="9dffe-167">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="9dffe-168">L’opération a échoué car la mémoire n’a pas pu être allouée.</span><span class="sxs-lookup"><span data-stu-id="9dffe-168">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-169">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="9dffe-169">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="9dffe-170">Seul un nombre fini de bases de données peut être attaché par instance.</span><span class="sxs-lookup"><span data-stu-id="9dffe-170">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="9dffe-171">La limite est actuellement de sept bases de données par instance.</span><span class="sxs-lookup"><span data-stu-id="9dffe-171">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-172">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="9dffe-172">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="9dffe-173">AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</span><span class="sxs-lookup"><span data-stu-id="9dffe-173">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-174">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="9dffe-174">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9dffe-175">JET_wrnFileOpenReadOnly indique que le fichier a été attaché en lecture seule, mais <strong>JetCreateDatabase</strong> n’a pas réussi JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="9dffe-175">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <strong>JetCreateDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="9dffe-176">La base de données est toujours ouverte avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9dffe-176">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="9dffe-177">Notes</span><span class="sxs-lookup"><span data-stu-id="9dffe-177">Remarks</span></span>

<span data-ttu-id="9dffe-178">Si la base de données spécifiée dans *szFilename* existe et que JET_bitDbOverwriteExisting n’a pas été transmis, l’appel de l’API échoue.</span><span class="sxs-lookup"><span data-stu-id="9dffe-178">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="9dffe-179">Si JET_bitDbOverwriteExisting a été transmis, l’ancien fichier de base de données sera d’abord supprimé.</span><span class="sxs-lookup"><span data-stu-id="9dffe-179">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="9dffe-180">Si l’API crée un fichier de base de données, puis accède à une autre erreur, il nettoie et supprime le fichier.</span><span class="sxs-lookup"><span data-stu-id="9dffe-180">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="9dffe-181">**JetCreateDatabase** ouvre implicitement la base de données.</span><span class="sxs-lookup"><span data-stu-id="9dffe-181">**JetCreateDatabase** will implicitly open the database.</span></span> <span data-ttu-id="9dffe-182">Il n’est pas nécessaire d’appeler par la suite [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="9dffe-182">It is not necessarily to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="9dffe-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dffe-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9dffe-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9dffe-185">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9dffe-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-186"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9dffe-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9dffe-187">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9dffe-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-188"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9dffe-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9dffe-189">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9dffe-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-190"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="9dffe-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9dffe-191">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9dffe-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dffe-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9dffe-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9dffe-193">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9dffe-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dffe-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9dffe-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9dffe-195">Implémenté en tant que <strong>JetCreateDatabaseW</strong> (Unicode) et <strong>JetCreateDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9dffe-195">Implemented as <strong>JetCreateDatabaseW</strong> (Unicode) and <strong>JetCreateDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9dffe-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dffe-196">See Also</span></span>

[<span data-ttu-id="9dffe-197">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="9dffe-197">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="9dffe-198">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9dffe-198">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9dffe-199">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="9dffe-199">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="9dffe-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9dffe-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9dffe-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9dffe-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9dffe-202">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="9dffe-202">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="9dffe-203">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="9dffe-203">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="9dffe-204">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="9dffe-204">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="9dffe-205">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="9dffe-205">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="9dffe-206">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9dffe-206">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9dffe-207">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="9dffe-207">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
