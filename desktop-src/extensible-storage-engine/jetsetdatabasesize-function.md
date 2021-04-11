---
description: 'En savoir plus sur : fonction JetSetDatabaseSize'
title: JetSetDatabaseSize fonction)
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112035"
---
# <a name="jetsetdatabasesize-function"></a><span data-ttu-id="2f70e-103">JetSetDatabaseSize fonction)</span><span class="sxs-lookup"><span data-stu-id="2f70e-103">JetSetDatabaseSize Function</span></span>


<span data-ttu-id="2f70e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2f70e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetdatabasesize-function"></a><span data-ttu-id="2f70e-105">JetSetDatabaseSize fonction)</span><span class="sxs-lookup"><span data-stu-id="2f70e-105">JetSetDatabaseSize Function</span></span>

<span data-ttu-id="2f70e-106">La fonction **JetSetDatabaseSize** définit la taille d’un fichier de base de données non ouvert.</span><span class="sxs-lookup"><span data-stu-id="2f70e-106">The **JetSetDatabaseSize** function sets the size of an unopened database file.</span></span>

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="2f70e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f70e-107">Parameters</span></span>

<span data-ttu-id="2f70e-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2f70e-108">*sesid*</span></span>

<span data-ttu-id="2f70e-109">Identifie le contexte de session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="2f70e-109">Identifies the database session context to use for the API call.</span></span>

<span data-ttu-id="2f70e-110">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="2f70e-110">*szDatabaseName*</span></span>

<span data-ttu-id="2f70e-111">Identifie le nom du fichier de base de données dont la taille doit être modifiée.</span><span class="sxs-lookup"><span data-stu-id="2f70e-111">Identifies the name of the database file whose size is to be altered.</span></span>

<span data-ttu-id="2f70e-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="2f70e-112">*cpg*</span></span>

<span data-ttu-id="2f70e-113">Spécifie la taille souhaitée de la base de données, en pages.</span><span class="sxs-lookup"><span data-stu-id="2f70e-113">Specifies the desired size of the database, in pages.</span></span>

<span data-ttu-id="2f70e-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="2f70e-114">*pcpgReal*</span></span>

<span data-ttu-id="2f70e-115">Pointeur vers un nombre qui reçoit la taille de la base de données, en pages, après l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="2f70e-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="2f70e-116">Si l’appel d’API a échoué, le contenu de *pcpgReal* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="2f70e-116">If the API call was unsuccessful, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="2f70e-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2f70e-117">Return Value</span></span>

<span data-ttu-id="2f70e-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="2f70e-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2f70e-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2f70e-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f70e-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2f70e-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="2f70e-121">Description</span><span class="sxs-lookup"><span data-stu-id="2f70e-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f70e-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2f70e-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2f70e-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2f70e-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f70e-124">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="2f70e-124">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="2f70e-125">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="2f70e-125">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="2f70e-126">JET_errDatabaseInconsistent et JET_errDatabaseDirtyShutdown sont la même valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="2f70e-126">JET_errDatabaseInconsistent and JET_errDatabaseDirtyShutdown are the same numeric value.</span></span> <span data-ttu-id="2f70e-127">La base de données dont la taille doit être ajustée doit être dans un état d’arrêt normal, appelée état cohérent.</span><span class="sxs-lookup"><span data-stu-id="2f70e-127">The database whose size is to be adjusted must be in a clean shutdown, known as a consistent state.</span></span> <span data-ttu-id="2f70e-128">Une base de données incohérente n’est pas endommagée, mais elle nécessite la relecture des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="2f70e-128">An inconsistent database is not corrupted, but it requires log files to be replayed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f70e-129">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="2f70e-129">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="2f70e-130"><em>szDatabaseName</em> ne doit pas être une chaîne vide et non null.</span><span class="sxs-lookup"><span data-stu-id="2f70e-130"><em>szDatabaseName</em> must not be an empty, non-NULL string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f70e-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="2f70e-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="2f70e-132">L’espace libre est insuffisant sur le volume pour effectuer l’opération d’augmentation.</span><span class="sxs-lookup"><span data-stu-id="2f70e-132">There is insufficient free space on the volume to perform the grow operation.</span></span> <span data-ttu-id="2f70e-133"><strong>JetSetDatabaseSize</strong> peut également renvoyer de nombreuses erreurs liées aux fichiers, notamment, mais sans s’y limiter :</span><span class="sxs-lookup"><span data-stu-id="2f70e-133"><strong>JetSetDatabaseSize</strong> may also return many file-related errors, including, but not limited to:</span></span></p>
<ul>
<li><p><span data-ttu-id="2f70e-134">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="2f70e-134">JET_errDiskIO</span></span></p></li>
<li><p><span data-ttu-id="2f70e-135">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="2f70e-135">JET_errFileNotFound</span></span></p></li>
<li><p><span data-ttu-id="2f70e-136">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="2f70e-136">JET_errInvalidPath</span></span></p></li>
<li><p><span data-ttu-id="2f70e-137">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="2f70e-137">JET_errFileAccessDenied</span></span></p></li>
<li><p><span data-ttu-id="2f70e-138">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="2f70e-138">JET_errOutOfFileHandles</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f70e-139">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2f70e-139">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2f70e-140">L’une des raisons pour lesquelles cette erreur peut être retournée est si <em>CPG</em> ne respecte pas la taille de base de données minimale.</span><span class="sxs-lookup"><span data-stu-id="2f70e-140">One of the reasons this error may be returned is if <em>cpg</em> does meet the minimum database size.</span></span> <span data-ttu-id="2f70e-141">La taille de base de données minimale actuelle est de 256 pages.</span><span class="sxs-lookup"><span data-stu-id="2f70e-141">The current minimum database size is 256 pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f70e-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="2f70e-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="2f70e-143">Les ressources mémoire du système sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="2f70e-143">The system is low on memory resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="2f70e-144">Notes</span><span class="sxs-lookup"><span data-stu-id="2f70e-144">Remarks</span></span>

<span data-ttu-id="2f70e-145">Si **JetSetDatabaseSize** est appelé avant d’insérer de grandes quantités de données, le fichier de base de données sera augmenté en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="2f70e-145">If **JetSetDatabaseSize** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="2f70e-146">Cela permet de réduire la probabilité que le fichier de base de données soit fragmenté au niveau du système de fichiers et de réduire également le nombre de fois où le fichier de base de données doit être augmenté.</span><span class="sxs-lookup"><span data-stu-id="2f70e-146">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="2f70e-147">La croissance du fichier de base de données peut être plus rapide que la croissance à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="2f70e-147">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="2f70e-148">Seule la croissance du fichier est actuellement prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2f70e-148">Only growing the file is currently supported.</span></span> <span data-ttu-id="2f70e-149">Pour réduire un fichier, utilisez la fonctionnalité de défragmentation du programme utilitaire esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="2f70e-149">To shrink a file, use the defragmentation feature of the esentutl.exe utility program.</span></span>

<span data-ttu-id="2f70e-150">Si la valeur de *CPG* est inférieure à la taille actuelle de la base de données, l’opération sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="2f70e-150">If *cpg* is smaller than the current size of the database, the operation will be ignored.</span></span> <span data-ttu-id="2f70e-151">Si la valeur de *CPG* est inférieure à la taille minimale de la base de données (actuellement 256 pages), elle retournera JET_errInvalidParameter.</span><span class="sxs-lookup"><span data-stu-id="2f70e-151">If *cpg* is less than the minimum database size (currently 256 pages), it will return JET_errInvalidParameter.</span></span>

<span data-ttu-id="2f70e-152">Pour définir la taille d’une base de données ouverte, consultez [JetGrowDatabase](./jetgrowdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="2f70e-152">To set the size of a database that is opened, see [JetGrowDatabase](./jetgrowdatabase-function.md).</span></span>

<span data-ttu-id="2f70e-153">La taille du fichier peut ne pas correspondre au nombre de pages retournées dans *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="2f70e-153">The file size may not match the number of pages returned in *pcpgReal*.</span></span> <span data-ttu-id="2f70e-154">Il existe deux pages réservées supplémentaires qui peuvent ne pas être comptées dans *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="2f70e-154">There are two additional reserved pages that may not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2f70e-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f70e-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f70e-156"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2f70e-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2f70e-157">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2f70e-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f70e-158"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2f70e-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2f70e-159">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2f70e-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f70e-160"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2f70e-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2f70e-161">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2f70e-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f70e-162"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="2f70e-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2f70e-163">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2f70e-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f70e-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2f70e-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2f70e-165">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2f70e-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f70e-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2f70e-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2f70e-167">Implémenté en tant que <strong>JetSetDatabaseSizeW</strong> (Unicode) et <strong>JetSetDatabaseSizeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2f70e-167">Implemented as <strong>JetSetDatabaseSizeW</strong> (Unicode) and <strong>JetSetDatabaseSizeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2f70e-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f70e-168">See Also</span></span>

[<span data-ttu-id="2f70e-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2f70e-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2f70e-170">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2f70e-170">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2f70e-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2f70e-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2f70e-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2f70e-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2f70e-173">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="2f70e-173">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="2f70e-174">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="2f70e-174">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="2f70e-175">JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="2f70e-175">JetGrowDatabase</span></span>](./jetgrowdatabase-function.md)
