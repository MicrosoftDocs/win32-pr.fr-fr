---
description: 'En savoir plus sur : fonction JetAttachDatabase'
title: Fonction JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201223"
---
# <a name="jetattachdatabase-function"></a><span data-ttu-id="0934b-103">Fonction JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="0934b-103">JetAttachDatabase Function</span></span>


<span data-ttu-id="0934b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="0934b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase-function"></a><span data-ttu-id="0934b-105">Fonction JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="0934b-105">JetAttachDatabase Function</span></span>

<span data-ttu-id="0934b-106">La fonction **JetAttachDatabase** attache un fichier de base de données à utiliser avec une instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="0934b-106">The **JetAttachDatabase** function attaches a database file for use with a database instance.</span></span> <span data-ttu-id="0934b-107">Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="0934b-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="0934b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0934b-108">Parameters</span></span>

<span data-ttu-id="0934b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0934b-109">*sesid*</span></span>

<span data-ttu-id="0934b-110">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="0934b-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="0934b-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="0934b-111">*szFilename*</span></span>

<span data-ttu-id="0934b-112">Nom de la base de données à attacher.</span><span class="sxs-lookup"><span data-stu-id="0934b-112">The name of the database to attach.</span></span>

<span data-ttu-id="0934b-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0934b-113">*grbit*</span></span>

<span data-ttu-id="0934b-114">Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="0934b-114">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0934b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0934b-115">Value</span></span></p></th>
<th><p><span data-ttu-id="0934b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0934b-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0934b-117">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="0934b-117">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="0934b-118">Si <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> a été défini, tous les index sur les données Unicode seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="0934b-118">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="0934b-119">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0934b-119">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-120">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="0934b-120">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="0934b-121">Tous les index des données Unicode seront supprimés, quel que soit le paramètre de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="0934b-121">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="0934b-122">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0934b-122">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-123">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="0934b-123">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="0934b-124">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="0934b-124">Obsolete.</span></span> <span data-ttu-id="0934b-125">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="0934b-125">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="0934b-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0934b-127">Empêche toute modification de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0934b-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0934b-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0934b-128">Return Value</span></span>

<span data-ttu-id="0934b-129">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="0934b-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0934b-130">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0934b-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0934b-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0934b-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="0934b-132">Description</span><span class="sxs-lookup"><span data-stu-id="0934b-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0934b-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0934b-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0934b-134">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0934b-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-135">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="0934b-135">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="0934b-136">L’attachement d’une base de données n’est pas autorisé pendant une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="0934b-136">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-137">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="0934b-137">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0934b-138">Le fichier de base de données spécifié par <em>szFilename</em> doit être accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="0934b-138">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="0934b-139">L’attribut Read-Only ne doit pas être défini, et le processus en cours d’exécution doit disposer des privilèges suffisants pour écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="0934b-139">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-140">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="0934b-140">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="0934b-141">Le fichier de base de données est déjà ouvert par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="0934b-141">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-142">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="0934b-142">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="0934b-143">Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="0934b-143">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="0934b-144"><em>szFilename</em> doit être non null et faire référence à un chemin d’accès valide.</span><span class="sxs-lookup"><span data-stu-id="0934b-144"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-145">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0934b-145">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="0934b-146">Le fichier de base de données a déjà été attaché par une autre session.</span><span class="sxs-lookup"><span data-stu-id="0934b-146">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-147">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="0934b-147">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="0934b-148">Le moteur de base de données ne peut pas ouvrir le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="0934b-148">The database engine cannot open the database file.</span></span> <span data-ttu-id="0934b-149">Le fichier est peut-être utilisé par un autre processus ou l’appelant peut ne pas disposer des privilèges suffisants pour ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="0934b-149">The file may be in use by another process or the caller may not have sufficient privileges to open the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="0934b-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="0934b-151">Le fichier spécifié dans <em>szFilename</em> n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0934b-151">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-152">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="0934b-152">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="0934b-153">Il y a une erreur avec l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="0934b-153">There is an error with the primary index.</span></span> <span data-ttu-id="0934b-154">Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire).</span><span class="sxs-lookup"><span data-stu-id="0934b-154">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="0934b-155">Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et l’index primaire sur une colonne avec des données Unicode.</span><span class="sxs-lookup"><span data-stu-id="0934b-155">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="0934b-156">Pour plus d’informations sur les index sur les données Unicode, consultez les notes.</span><span class="sxs-lookup"><span data-stu-id="0934b-156">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-157">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="0934b-157">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="0934b-158">Il y a une erreur avec un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="0934b-158">There is an error with a secondary index.</span></span> <span data-ttu-id="0934b-159">Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire).</span><span class="sxs-lookup"><span data-stu-id="0934b-159">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="0934b-160">Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et un index secondaire sur une colonne avec des données Unicode.</span><span class="sxs-lookup"><span data-stu-id="0934b-160">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="0934b-161">Pour plus d’informations sur les index sur les données Unicode, consultez les notes.</span><span class="sxs-lookup"><span data-stu-id="0934b-161">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="0934b-162">Les index secondaires sont entièrement reconstruits lorsqu’une base de données est défragmentée à l’aide d’un utilitaire hors connexion à l’aide de la commande suivante : <strong>Esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="0934b-162">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-163">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="0934b-163">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="0934b-164">Seul un nombre fini de bases de données peut être attaché par instance.</span><span class="sxs-lookup"><span data-stu-id="0934b-164">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="0934b-165">La limite est actuellement de sept bases de données par instance.</span><span class="sxs-lookup"><span data-stu-id="0934b-165">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-166">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="0934b-166">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="0934b-167">AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</span><span class="sxs-lookup"><span data-stu-id="0934b-167">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0934b-168">Notes</span><span class="sxs-lookup"><span data-stu-id="0934b-168">Remarks</span></span>

<span data-ttu-id="0934b-169">L’appel de **JetAttachDatabase** équivaut à appeler [JetAttachDatabase2](./jetattachdatabase2-function.md) et à passer une valeur de zéro, ce qui signifie qu’il n’y a aucune limite pour le paramètre *cpgDatabaseSizeMax* .</span><span class="sxs-lookup"><span data-stu-id="0934b-169">Calling **JetAttachDatabase** is equivalent to calling [JetAttachDatabase2](./jetattachdatabase2-function.md) and passing a value of zero, meaning there is no limit, for the *cpgDatabaseSizeMax* parameter.</span></span>

<span data-ttu-id="0934b-170">L’attachement d’une base de données accessible en écriture (autrement dit, si JET_bitDbReadOnly n’a pas été spécifié dans le paramètre *Grbit* ) ouvre le fichier exclusivement au niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0934b-170">Attaching a writable database (that is, if JET_bitDbReadOnly was not specified in the *grbit* parameter) will open the file exclusively at the operating system level.</span></span> <span data-ttu-id="0934b-171">Aucun autre processus ne peut ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="0934b-171">No other process will be able open the file.</span></span> <span data-ttu-id="0934b-172">Il est possible pour plusieurs processus d’attacher une base de données unique en les ouvrant en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0934b-172">It is possible for multiple processes to attach a single database by opening them in read-only mode.</span></span>

<span data-ttu-id="0934b-173">Le fichier de base de données est détaché à l’aide de [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="0934b-173">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="0934b-174">Paramètres de vérification d’index</span><span class="sxs-lookup"><span data-stu-id="0934b-174">Index-checking parameters</span></span>

<span data-ttu-id="0934b-175">Les différentes versions de Windows normalisent le texte Unicode de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="0934b-175">Different versions of Windows normalize Unicode text in different ways.</span></span> <span data-ttu-id="0934b-176">Cela signifie que les index créés sous une version de Windows peuvent ne pas fonctionner sur d’autres versions.</span><span class="sxs-lookup"><span data-stu-id="0934b-176">That means indexes built under one version of Windows may not work on other versions.</span></span>

<span data-ttu-id="0934b-177">Avant Windows Server 2003, lorsque la version du système d’exploitation était modifiée (y compris l’installation d’un service pack), chaque index sur les données Unicode était dans un État potentiellement endommagé.</span><span class="sxs-lookup"><span data-stu-id="0934b-177">Prior to Windows Server 2003, when the operating system version changed (including installation of a Service Pack), every index over Unicode data was in a potentially corrupt state.</span></span>

<span data-ttu-id="0934b-178">Les index créés dans Windows Server 2003 et versions ultérieures sont signalés par la version de la normalisation Unicode avec laquelle ils ont été générés.</span><span class="sxs-lookup"><span data-stu-id="0934b-178">Indexes created in Windows Server 2003 and later are flagged with the version of Unicode normalization with which they were built.</span></span> <span data-ttu-id="0934b-179">Les index plus anciens ne contiennent pas d’informations sur la version.</span><span class="sxs-lookup"><span data-stu-id="0934b-179">Older indexes contain no version information.</span></span> <span data-ttu-id="0934b-180">La plupart des modifications de normalisation Unicode consistent en l’ajout de nouveaux caractères, tandis que les points de code précédemment non définis sont maintenant définis et normalisés différemment.</span><span class="sxs-lookup"><span data-stu-id="0934b-180">Most Unicode normalization changes consist of adding new characters, code points which were previously undefined are now defined and normalize differently.</span></span> <span data-ttu-id="0934b-181">Par conséquent, si les données binaires sont stockées dans une colonne Unicode, elles se normalssent différemment à mesure que de nouveaux points de code sont définis.</span><span class="sxs-lookup"><span data-stu-id="0934b-181">Thus, if binary data is stored in a Unicode column, it will normalize differently as new code points are defined.</span></span>

<span data-ttu-id="0934b-182">À partir de Windows Server 2003, le moteur de base de données ESE effectue le suivi des entrées d’index Unicode qui contiennent des points de code non définis.</span><span class="sxs-lookup"><span data-stu-id="0934b-182">As of Windows Server 2003, the ESE database engine tracks Unicode index entries that contain undefined code points.</span></span> <span data-ttu-id="0934b-183">Elles peuvent être utilisées pour corriger un index lorsque l’ensemble de caractères Unicode définis change.</span><span class="sxs-lookup"><span data-stu-id="0934b-183">These can be used to fix an index when the set of defined Unicode characters changes.</span></span>

<span data-ttu-id="0934b-184">Ces paramètres contrôlent ce qui se produit lorsque le moteur de base de données ESE est attaché à une base de données qui a été utilisée pour la dernière fois sous une version différente du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0934b-184">These parameters control what happens when the ESE database engine attaches to a database that was last used under a different build of the operating system.</span></span> <span data-ttu-id="0934b-185">La version du système d’exploitation est marquée dans l’en-tête de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0934b-185">The operating system version is stamped in the database header.</span></span>

<span data-ttu-id="0934b-186">Si [JET_paramEnableIndexChecking](./database-parameters.md) a la valeur **true** et que la base de données contient des index potentiellement endommagés :</span><span class="sxs-lookup"><span data-stu-id="0934b-186">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **TRUE**, and the database contains potentially corrupt indexes:</span></span>

  - <span data-ttu-id="0934b-187">**JetAttachDatabase** supprimera les index potentiellement endommagés si *Grbit* contient JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="0934b-187">**JetAttachDatabase** will delete the potentially corrupt indexes if *grbit* contains JET_bitDbDeleteCorruptIndexes</span></span>

  - <span data-ttu-id="0934b-188">**JetAttachDatabase** renvoie une erreur si *Grbit* ne contient pas de JET_bitDbDeleteCorruptIndexes et si des index doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="0934b-188">**JetAttachDatabase** will return an error if *grbit* does not contain JET_bitDbDeleteCorruptIndexes and there are indexes which need deletion.</span></span>

<span data-ttu-id="0934b-189">Si [JET_paramEnableIndexChecking](./database-parameters.md) a la valeur **false**:</span><span class="sxs-lookup"><span data-stu-id="0934b-189">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **FALSE**:</span></span>

  - <span data-ttu-id="0934b-190">**JetAttachDatabase** ignore les index potentiellement endommagés et retourne JET_errSuccess (en supposant qu’il n’y avait pas d’autres erreurs).</span><span class="sxs-lookup"><span data-stu-id="0934b-190">**JetAttachDatabase** will ignore potentially corrupt indexes, and return JET_errSuccess (assuming there were no other errors).</span></span>

<span data-ttu-id="0934b-191">Windows Server 2003 et versions ultérieures : si [JET_paramEnableIndexChecking](./database-parameters.md) n’a pas été réinitialisée, la table de correction interne est utilisée pour corriger les entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="0934b-191">Windows Server 2003 and later: If [JET_paramEnableIndexChecking](./database-parameters.md) has not been reset, the internal fixup table will be used to fixup index entries.</span></span> <span data-ttu-id="0934b-192">Cela peut ne pas résoudre tous les endommagements d’index, mais est transparent pour l’application.</span><span class="sxs-lookup"><span data-stu-id="0934b-192">This may not fix all index corruptions but will be transparent to the application.</span></span>

<span data-ttu-id="0934b-193">Si la base de données a été attachée en lecture seule, l’index ne peut pas être fixe ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="0934b-193">If the database was attached as read-only the index cannot be fixed or deleted.</span></span> <span data-ttu-id="0934b-194">Dans ce cas, l’API retourne une erreur, par exemple JET_errSecondaryIndexCorrupted ou JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="0934b-194">In this case, the API will instead return an error, such as JET_errSecondaryIndexCorrupted or JET_errPrimaryIndexCorrupted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0934b-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0934b-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0934b-196"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0934b-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0934b-197">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="0934b-197">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-198"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="0934b-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0934b-199">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0934b-199">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-200"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="0934b-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0934b-201">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="0934b-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-202"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="0934b-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0934b-203">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0934b-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0934b-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0934b-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0934b-205">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0934b-205">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0934b-206"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0934b-206"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0934b-207">Implémenté en tant que <strong>JetAddColumnW</strong> (Unicode) et <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0934b-207">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0934b-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0934b-208">See Also</span></span>

[<span data-ttu-id="0934b-209">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="0934b-209">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="0934b-210">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0934b-210">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0934b-211">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0934b-211">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0934b-212">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0934b-212">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0934b-213">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0934b-213">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0934b-214">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="0934b-214">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="0934b-215">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="0934b-215">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="0934b-216">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="0934b-216">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="0934b-217">JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="0934b-217">JetDetachDatabase2</span></span>](./jetdetachdatabase2-function.md)  
[<span data-ttu-id="0934b-218">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="0934b-218">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="0934b-219">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0934b-219">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
