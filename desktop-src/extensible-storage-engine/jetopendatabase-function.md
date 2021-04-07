---
description: 'En savoir plus sur : fonction JetOpenDatabase'
title: Fonction JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760539"
---
# <a name="jetopendatabase-function"></a><span data-ttu-id="37360-103">Fonction JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="37360-103">JetOpenDatabase Function</span></span>


<span data-ttu-id="37360-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="37360-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopendatabase-function"></a><span data-ttu-id="37360-105">Fonction JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="37360-105">JetOpenDatabase Function</span></span>

<span data-ttu-id="37360-106">La fonction **JetOpenDatabase** ouvre une base de données précédemment attachée, à l’aide des fonctions [JetAttachDatabase](./jetattachdatabase-function.md) ou [JetAttachDatabase2](./jetattachdatabase2-function.md) , pour une utilisation avec une session de base de données.</span><span class="sxs-lookup"><span data-stu-id="37360-106">The **JetOpenDatabase** function opens a previously attached database, using the [JetAttachDatabase](./jetattachdatabase-function.md) or [JetAttachDatabase2](./jetattachdatabase2-function.md) functions, for use with a database session.</span></span> <span data-ttu-id="37360-107">Cette fonction peut être appelée plusieurs fois pour la même base de données.</span><span class="sxs-lookup"><span data-stu-id="37360-107">This function can be called multiple times for the same database.</span></span>

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="37360-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37360-108">Parameters</span></span>

<span data-ttu-id="37360-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="37360-109">*sesid*</span></span>

<span data-ttu-id="37360-110">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="37360-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="37360-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="37360-111">*szFilename*</span></span>

<span data-ttu-id="37360-112">Nom de la base de données à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="37360-112">The name of the database to open.</span></span>

<span data-ttu-id="37360-113">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="37360-113">*szConnect*</span></span>

<span data-ttu-id="37360-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="37360-114">Reserved.</span></span> <span data-ttu-id="37360-115">valeur de l’en-tête définie sur Null.</span><span class="sxs-lookup"><span data-stu-id="37360-115">Set to NULL.</span></span>

<span data-ttu-id="37360-116">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="37360-116">*pdbid*</span></span>

<span data-ttu-id="37360-117">Pointeur vers une mémoire tampon qui, sur un appel réussi, contient l’identificateur de la base de données.</span><span class="sxs-lookup"><span data-stu-id="37360-117">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="37360-118">Si l’appel échoue, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="37360-118">If the call fails, the value is undefined.</span></span>

<span data-ttu-id="37360-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="37360-119">*grbit*</span></span>

<span data-ttu-id="37360-120">Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="37360-120">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37360-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="37360-121">Value</span></span></p></th>
<th><p><span data-ttu-id="37360-122">Signification</span><span class="sxs-lookup"><span data-stu-id="37360-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37360-123">JET_bitDbExclusive</span><span class="sxs-lookup"><span data-stu-id="37360-123">JET_bitDbExclusive</span></span></p></td>
<td><p><span data-ttu-id="37360-124">Autorise une seule session à attacher une base de données.</span><span class="sxs-lookup"><span data-stu-id="37360-124">Allows only a single session to attach a database.</span></span> <span data-ttu-id="37360-125">En règle générale, plusieurs sessions peuvent ouvrir une base de données.</span><span class="sxs-lookup"><span data-stu-id="37360-125">Normally, several sessions can open a database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="37360-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="37360-127">Empêche toute modification de la base de données.</span><span class="sxs-lookup"><span data-stu-id="37360-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="37360-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37360-128">Return Value</span></span>

<span data-ttu-id="37360-129">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="37360-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="37360-130">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37360-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37360-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="37360-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="37360-132">Description</span><span class="sxs-lookup"><span data-stu-id="37360-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37360-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="37360-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="37360-134">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="37360-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-135">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="37360-135">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="37360-136">L’accès exclusif a été demandé, mais n’a pas pu être accordé.</span><span class="sxs-lookup"><span data-stu-id="37360-136">Exclusive access was requested, but could not be granted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37360-137">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="37360-137">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="37360-138">Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="37360-138">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="37360-139"><em>szFilename</em> doit être non null et faire référence à un fichier valide.</span><span class="sxs-lookup"><span data-stu-id="37360-139"><em>szFilename</em> must be non-NULL and refer to a valid file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-140">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="37360-140">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="37360-141">Une autre session a déjà ouvert la base de données en mode exclusif (à l’aide de JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="37360-141">Another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37360-142">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="37360-142">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="37360-143">La base de données n’a pas été attachée précédemment (voir <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="37360-143">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-144">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="37360-144">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="37360-145">Une tentative a été effectuée pour ouvrir un fichier qui n’est pas un fichier de base de données valide.</span><span class="sxs-lookup"><span data-stu-id="37360-145">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37360-146">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="37360-146">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="37360-147">Une tentative a été effectuée pour ouvrir plus d’une base de données et <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> a été définie.</span><span class="sxs-lookup"><span data-stu-id="37360-147">An attempt was made to open more than one database, and <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> was set.</span></span> <span data-ttu-id="37360-148">Pour plus d’informations, consultez <a href="gg294139(v=exchg.10).md">paramètres système</a>.</span><span class="sxs-lookup"><span data-stu-id="37360-148">For more information, see <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-149">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="37360-149">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="37360-150">Le fichier a été attaché en lecture seule, mais <strong>JetOpenDatabase</strong> n’a pas réussi JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="37360-150">The file was attached as read-only, but <strong>JetOpenDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="37360-151">La base de données est toujours ouverte avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="37360-151">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="37360-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37360-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37360-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="37360-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="37360-154">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="37360-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-155"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="37360-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="37360-156">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="37360-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37360-157"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="37360-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="37360-158">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="37360-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-159"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="37360-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="37360-160">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="37360-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37360-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="37360-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="37360-162">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="37360-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37360-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="37360-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="37360-164">Implémenté en tant que <strong>JetOpenDatabaseW</strong> (Unicode) et <strong>JetOpenDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="37360-164">Implemented as <strong>JetOpenDatabaseW</strong> (Unicode) and <strong>JetOpenDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="37360-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37360-165">See Also</span></span>

[<span data-ttu-id="37360-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="37360-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="37360-167">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="37360-167">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="37360-168">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="37360-168">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="37360-169">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="37360-169">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="37360-170">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="37360-170">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="37360-171">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="37360-171">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="37360-172">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="37360-172">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="37360-173">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="37360-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
