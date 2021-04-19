---
description: 'En savoir plus sur : fonction JetGrowDatabase'
title: JetGrowDatabase fonction)
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539098"
---
# <a name="jetgrowdatabase-function"></a><span data-ttu-id="a20db-103">JetGrowDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="a20db-103">JetGrowDatabase Function</span></span>


<span data-ttu-id="a20db-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a20db-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgrowdatabase-function"></a><span data-ttu-id="a20db-105">JetGrowDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="a20db-105">JetGrowDatabase Function</span></span>

<span data-ttu-id="a20db-106">La fonction **JetGrowDatabase** étend la taille d’une base de données qui est actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="a20db-106">The **JetGrowDatabase** function extends the size of a database that is currently open.</span></span>

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="a20db-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a20db-107">Parameters</span></span>

<span data-ttu-id="a20db-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a20db-108">*sesid*</span></span>

<span data-ttu-id="a20db-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="a20db-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="a20db-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="a20db-110">*dbid*</span></span>

<span data-ttu-id="a20db-111">Base de données qui sera étendue.</span><span class="sxs-lookup"><span data-stu-id="a20db-111">The database that will be extended.</span></span>

<span data-ttu-id="a20db-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="a20db-112">*cpg*</span></span>

<span data-ttu-id="a20db-113">Taille souhaitée de la base de données, en pages.</span><span class="sxs-lookup"><span data-stu-id="a20db-113">The desired size of the database, in pages.</span></span>

<span data-ttu-id="a20db-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="a20db-114">*pcpgReal*</span></span>

<span data-ttu-id="a20db-115">Pointeur vers un nombre qui reçoit la taille de la base de données, en pages, après l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="a20db-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="a20db-116">Si l’appel d’API échoue, le contenu de *pcpgReal* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="a20db-116">If the API call fails, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="a20db-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a20db-117">Return Value</span></span>

<span data-ttu-id="a20db-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="a20db-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a20db-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a20db-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a20db-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a20db-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="a20db-121">Description</span><span class="sxs-lookup"><span data-stu-id="a20db-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a20db-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a20db-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a20db-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a20db-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a20db-124">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="a20db-124">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="a20db-125">L’espace libre est insuffisant sur le volume pour effectuer l’opération d’augmentation.</span><span class="sxs-lookup"><span data-stu-id="a20db-125">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a20db-126">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="a20db-126">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="a20db-127">Une erreur liée à un fichier a été retournée par <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="a20db-127">A file-related error was returned by <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span> <span data-ttu-id="a20db-128">Pour plus d’informations sur les autres erreurs liées aux fichiers qui peuvent être retournées, consultez <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="a20db-128">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="a20db-129">Notes</span><span class="sxs-lookup"><span data-stu-id="a20db-129">Remarks</span></span>

<span data-ttu-id="a20db-130">Si **JetGrowDatabase** est appelé avant d’insérer de grandes quantités de données, le fichier de base de données sera augmenté en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="a20db-130">If **JetGrowDatabase** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="a20db-131">Cela permet de réduire la probabilité que le fichier de base de données soit fragmenté au niveau du système de fichiers et de réduire également le nombre de fois où le fichier de base de données doit être augmenté.</span><span class="sxs-lookup"><span data-stu-id="a20db-131">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="a20db-132">La croissance du fichier de base de données peut être plus rapide que la croissance à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="a20db-132">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="a20db-133">Seule la croissance du fichier est actuellement prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a20db-133">Only growing the file is currently supported.</span></span> <span data-ttu-id="a20db-134">Pour réduire un fichier, utilisez la fonctionnalité de défragmentation du programme utilitaire **esentutl.exe** .</span><span class="sxs-lookup"><span data-stu-id="a20db-134">To shrink a file, use the defragmentation feature of the **esentutl.exe** utility program.</span></span>

<span data-ttu-id="a20db-135">Pour définir la taille d’une base de données qui n’est pas ouverte, consultez [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="a20db-135">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="a20db-136">La taille du fichier peut ne pas correspondre au nombre de pages retournées dans *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="a20db-136">The file size might not match the number of pages that are returned in *pcpgReal*.</span></span> <span data-ttu-id="a20db-137">Il existe deux pages réservées supplémentaires qui peuvent ne pas être comptées dans *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="a20db-137">There are two additional reserved pages that might not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a20db-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a20db-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a20db-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a20db-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a20db-140">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="a20db-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a20db-141"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a20db-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a20db-142">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a20db-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a20db-143"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a20db-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a20db-144">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a20db-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a20db-145"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="a20db-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a20db-146">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a20db-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a20db-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a20db-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a20db-148">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a20db-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a20db-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a20db-149">See Also</span></span>

[<span data-ttu-id="a20db-150">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a20db-150">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a20db-151">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a20db-151">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a20db-152">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a20db-152">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a20db-153">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a20db-153">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a20db-154">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="a20db-154">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="a20db-155">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="a20db-155">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="a20db-156">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="a20db-156">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
