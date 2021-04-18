---
description: 'En savoir plus sur : fonction JetAttachDatabase2'
title: Fonction JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526280"
---
# <a name="jetattachdatabase2-function"></a><span data-ttu-id="53a9f-103">Fonction JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="53a9f-103">JetAttachDatabase2 Function</span></span>


<span data-ttu-id="53a9f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="53a9f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase2-function"></a><span data-ttu-id="53a9f-105">Fonction JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="53a9f-105">JetAttachDatabase2 Function</span></span>

<span data-ttu-id="53a9f-106">La fonction **JetAttachDatabase2** attache un fichier de base de données pour une utilisation avec une instance de base de données et spécifie une taille maximale pour cette base de données.</span><span class="sxs-lookup"><span data-stu-id="53a9f-106">The **JetAttachDatabase2** function attaches a database file for use with a database instance and specifies a maximum size for that database.</span></span> <span data-ttu-id="53a9f-107">Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="53a9f-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="53a9f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53a9f-108">Parameters</span></span>

<span data-ttu-id="53a9f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="53a9f-109">*sesid*</span></span>

<span data-ttu-id="53a9f-110">Contexte de session de base de données qui sera utilisé pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="53a9f-110">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="53a9f-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="53a9f-111">*szFilename*</span></span>

<span data-ttu-id="53a9f-112">Nom de la base de données à attacher.</span><span class="sxs-lookup"><span data-stu-id="53a9f-112">The name of the database to attach.</span></span>

<span data-ttu-id="53a9f-113">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="53a9f-113">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="53a9f-114">Taille maximale, en pages de base de données, pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="53a9f-114">The maximum size, in database pages, for database.</span></span> <span data-ttu-id="53a9f-115">La taille de page de la base de données par défaut est de 4 kilo-octets, qui peut être modifiée à l’aide de la fonction [JetSetSystemParameter](./jetsetsystemparameter-function.md) avant de créer une base de données.</span><span class="sxs-lookup"><span data-stu-id="53a9f-115">The default database page size is 4 kilobytes, which can be changed using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function prior to creating a database.</span></span>

<span data-ttu-id="53a9f-116">Le fait de passer la valeur zéro signifie qu’il n’y a pas de valeur maximale appliquée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="53a9f-116">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="53a9f-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="53a9f-117">*grbit*</span></span>

<span data-ttu-id="53a9f-118">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="53a9f-118">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53a9f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="53a9f-119">Value</span></span></p></th>
<th><p><span data-ttu-id="53a9f-120">Signification</span><span class="sxs-lookup"><span data-stu-id="53a9f-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-121">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="53a9f-121">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="53a9f-122">Si <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> a été défini, tous les index sur les données Unicode seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="53a9f-122">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="53a9f-123">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="53a9f-123">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-124">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="53a9f-124">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="53a9f-125">Tous les index des données Unicode seront supprimés, quel que soit le paramètre de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="53a9f-125">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="53a9f-126">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="53a9f-126">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-127">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="53a9f-127">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="53a9f-128">Empêche toute modification de la base de données.</span><span class="sxs-lookup"><span data-stu-id="53a9f-128">Prevents modifications to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-129">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="53a9f-129">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="53a9f-130">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="53a9f-130">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="53a9f-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53a9f-131">Return Value</span></span>

<span data-ttu-id="53a9f-132">La fonction retourne l’un des codes d’erreur [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="53a9f-132">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="53a9f-133">Les éléments suivants sont les plus couramment renvoyés.</span><span class="sxs-lookup"><span data-stu-id="53a9f-133">The following are the most commonly returned.</span></span> <span data-ttu-id="53a9f-134">(Pour obtenir la liste complète des erreurs pour cette API, consultez [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="53a9f-134">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53a9f-135">Code de retour</span><span class="sxs-lookup"><span data-stu-id="53a9f-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="53a9f-136">Description</span><span class="sxs-lookup"><span data-stu-id="53a9f-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-137">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="53a9f-137">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="53a9f-138">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="53a9f-138">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-139">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="53a9f-139">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="53a9f-140">L’attachement d’une base de données n’est pas autorisé pendant une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="53a9f-140">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-141">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="53a9f-141">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="53a9f-142">Le fichier de base de données spécifié par <em>szFilename</em> doit être accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="53a9f-142">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="53a9f-143">L’attribut Read-Only ne doit pas être défini, et le processus en cours d’exécution doit disposer des privilèges suffisants pour écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="53a9f-143">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="53a9f-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="53a9f-145">Le fichier de base de données est déjà ouvert par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="53a9f-145">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-146">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="53a9f-146">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="53a9f-147">Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="53a9f-147">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="53a9f-148"><em>szFilename</em> doit être non null et faire référence à un chemin d’accès valide.</span><span class="sxs-lookup"><span data-stu-id="53a9f-148"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-149">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="53a9f-149">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="53a9f-150">Le fichier de base de données a déjà été attaché par une autre session.</span><span class="sxs-lookup"><span data-stu-id="53a9f-150">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-151">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="53a9f-151">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="53a9f-152">Le fichier spécifié dans <em>szFilename</em> n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="53a9f-152">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-153">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="53a9f-153">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="53a9f-154">Il y a une erreur avec l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="53a9f-154">There is an error with the primary index.</span></span> <span data-ttu-id="53a9f-155">Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire).</span><span class="sxs-lookup"><span data-stu-id="53a9f-155">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="53a9f-156">Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et l’index primaire sur une colonne avec des données Unicode.</span><span class="sxs-lookup"><span data-stu-id="53a9f-156">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="53a9f-157">Pour plus d’informations sur les index sur les données Unicode, consultez les notes.</span><span class="sxs-lookup"><span data-stu-id="53a9f-157">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-158">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="53a9f-158">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="53a9f-159">Il y a une erreur avec un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="53a9f-159">There is an error with a secondary index.</span></span> <span data-ttu-id="53a9f-160">Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire).</span><span class="sxs-lookup"><span data-stu-id="53a9f-160">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="53a9f-161">Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et un index secondaire sur une colonne avec des données Unicode.</span><span class="sxs-lookup"><span data-stu-id="53a9f-161">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="53a9f-162">Pour plus d’informations sur les index sur les données Unicode, consultez les notes.</span><span class="sxs-lookup"><span data-stu-id="53a9f-162">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="53a9f-163">Les index secondaires sont entièrement reconstruits lorsqu’une base de données est défragmentée à l’aide d’un utilitaire hors connexion à l’aide de la commande suivante : <strong>Esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="53a9f-163">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-164">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="53a9f-164">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="53a9f-165">Seul un nombre fini de bases de données peut être attaché par instance.</span><span class="sxs-lookup"><span data-stu-id="53a9f-165">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="53a9f-166">La limite est actuellement de sept bases de données par instance.</span><span class="sxs-lookup"><span data-stu-id="53a9f-166">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-167">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="53a9f-167">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="53a9f-168">AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</span><span class="sxs-lookup"><span data-stu-id="53a9f-168">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="53a9f-169">Notes</span><span class="sxs-lookup"><span data-stu-id="53a9f-169">Remarks</span></span>

<span data-ttu-id="53a9f-170">Le fichier de base de données est détaché à l’aide de [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="53a9f-170">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="53a9f-171">Consultez [JetAttachDatabase](./jetattachdatabase-function.md) pour les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a9f-171">See [JetAttachDatabase](./jetattachdatabase-function.md) for remarks.</span></span>

#### <a name="requirements"></a><span data-ttu-id="53a9f-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53a9f-172">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-173"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="53a9f-173"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="53a9f-174">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="53a9f-174">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-175"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="53a9f-175"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="53a9f-176">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="53a9f-176">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-177"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="53a9f-177"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="53a9f-178">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="53a9f-178">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-179"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="53a9f-179"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="53a9f-180">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="53a9f-180">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a9f-181"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="53a9f-181"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="53a9f-182">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="53a9f-182">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a9f-183"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="53a9f-183"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="53a9f-184">Implémenté en tant que <strong>JetAttachDatabase2W</strong> (Unicode) et <strong>JetAttachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="53a9f-184">Implemented as <strong>JetAttachDatabase2W</strong> (Unicode) and <strong>JetAttachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="53a9f-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53a9f-185">See Also</span></span>

[<span data-ttu-id="53a9f-186">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="53a9f-186">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="53a9f-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="53a9f-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="53a9f-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="53a9f-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="53a9f-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="53a9f-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="53a9f-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="53a9f-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="53a9f-191">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="53a9f-191">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="53a9f-192">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="53a9f-192">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="53a9f-193">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="53a9f-193">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="53a9f-194">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="53a9f-194">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
