---
description: 'En savoir plus sur : fonction JetResizeDatabase'
title: JetResizeDatabase fonction)
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523692"
---
# <a name="jetresizedatabase-function"></a><span data-ttu-id="89186-103">JetResizeDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="89186-103">JetResizeDatabase Function</span></span>


<span data-ttu-id="89186-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="89186-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="89186-105">La fonction **JetResizeDatabase** étend ou réduit la taille d’une base de données qui est actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="89186-105">The **JetResizeDatabase** function extends or shrinks the size of a database that is currently open.</span></span>

<span data-ttu-id="89186-106">La fonction **JetResizeDatabase** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89186-106">The **JetResizeDatabase** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="89186-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89186-107">Parameters</span></span>

<span data-ttu-id="89186-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="89186-108">*sesid*</span></span>

<span data-ttu-id="89186-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="89186-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="89186-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="89186-110">*dbid*</span></span>

<span data-ttu-id="89186-111">Base de données qui sera étendue.</span><span class="sxs-lookup"><span data-stu-id="89186-111">The database that will be extended.</span></span>

<span data-ttu-id="89186-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="89186-112">*cpg*</span></span>

<span data-ttu-id="89186-113">Taille demandée de la base de données, en pages.</span><span class="sxs-lookup"><span data-stu-id="89186-113">The requested size of the database, in pages.</span></span>

<span data-ttu-id="89186-114">*pcpgActual*</span><span class="sxs-lookup"><span data-stu-id="89186-114">*pcpgActual*</span></span>

<span data-ttu-id="89186-115">Pointeur vers un nombre qui reçoit la taille de la base de données, en pages, après l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="89186-115">A pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="89186-116">Si l’appel d’API échoue, le contenu du paramètre *pcpgActual* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="89186-116">If the API call fails, the contents of *pcpgActual* parameter are undefined.</span></span>

<span data-ttu-id="89186-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="89186-117">*grbit*</span></span>

<span data-ttu-id="89186-118">Groupe de bits qui spécifie zéro, une ou plusieurs des valeurs énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="89186-118">A group of bits that specifies zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89186-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="89186-119">Value</span></span></p></th>
<th><p><span data-ttu-id="89186-120">Signification</span><span class="sxs-lookup"><span data-stu-id="89186-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89186-121">JET_bitResizeDatabaseOnlyGrow</span><span class="sxs-lookup"><span data-stu-id="89186-121">JET_bitResizeDatabaseOnlyGrow</span></span></p></td>
<td><p><span data-ttu-id="89186-122">Développez uniquement la base de données.</span><span class="sxs-lookup"><span data-stu-id="89186-122">Only grow the database.</span></span> <span data-ttu-id="89186-123">Si l’appel Resize réduit la base de données, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="89186-123">If the resize call would shrink the database, do nothing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="89186-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89186-124">Return value</span></span>

<span data-ttu-id="89186-125">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="89186-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="89186-126">Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="89186-126">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89186-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="89186-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="89186-128">Description</span><span class="sxs-lookup"><span data-stu-id="89186-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89186-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="89186-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="89186-130">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="89186-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89186-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="89186-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="89186-132">L’espace libre est insuffisant sur le volume pour effectuer l’opération d’augmentation.</span><span class="sxs-lookup"><span data-stu-id="89186-132">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89186-133">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="89186-133">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="89186-134">Une erreur liée à un fichier a été retournée par la fonction <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> .</span><span class="sxs-lookup"><span data-stu-id="89186-134">A file-related error was returned by the <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> function.</span></span> <span data-ttu-id="89186-135">Pour plus d’informations sur les autres erreurs liées aux fichiers qui peuvent être retournées, consultez <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="89186-135">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="89186-136">Notes</span><span class="sxs-lookup"><span data-stu-id="89186-136">Remarks</span></span>

<span data-ttu-id="89186-137">Si la fonction **JetResizeDatabase** est appelée avant l’insertion de grandes quantités de données, le fichier de base de données sera augmenté en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="89186-137">If the **JetResizeDatabase** function is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="89186-138">Cela permet de réduire la probabilité que le fichier de base de données soit fragmenté au niveau du système de fichiers et de réduire également le nombre de fois où le fichier de base de données doit être augmenté.</span><span class="sxs-lookup"><span data-stu-id="89186-138">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="89186-139">La croissance du fichier de base de données peut être plus rapide que la croissance à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="89186-139">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="89186-140">Pour définir la taille d’une base de données qui n’est pas ouverte, consultez [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="89186-140">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="89186-141">La taille du fichier peut ne pas correspondre au nombre de pages retournées dans le paramètre *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="89186-141">The file size might not match the number of pages that are returned in the *pcpgReal* parameter.</span></span> <span data-ttu-id="89186-142">Deux pages réservées supplémentaires peuvent ne pas être comptées dans le paramètre *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="89186-142">Two additional reserved pages might not be counted in the *pcpgReal* parameter.</span></span>

#### <a name="requirements"></a><span data-ttu-id="89186-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89186-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89186-144"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="89186-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="89186-145">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89186-145">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89186-146"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="89186-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="89186-147">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="89186-147">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89186-148"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="89186-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="89186-149">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="89186-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89186-150"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="89186-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="89186-151">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="89186-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89186-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="89186-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="89186-153">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="89186-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="89186-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89186-154">See also</span></span>

[<span data-ttu-id="89186-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="89186-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="89186-156">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="89186-156">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="89186-157">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="89186-157">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="89186-158">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="89186-158">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="89186-159">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="89186-159">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="89186-160">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="89186-160">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="89186-161">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="89186-161">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
