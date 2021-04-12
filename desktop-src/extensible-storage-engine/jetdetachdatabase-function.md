---
description: 'En savoir plus sur : fonction JetDetachDatabase'
title: Fonction JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320946"
---
# <a name="jetdetachdatabase-function"></a><span data-ttu-id="75091-103">Fonction JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="75091-103">JetDetachDatabase Function</span></span>


<span data-ttu-id="75091-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="75091-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase-function"></a><span data-ttu-id="75091-105">Fonction JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="75091-105">JetDetachDatabase Function</span></span>

<span data-ttu-id="75091-106">La fonction **JetDetachDatabase** libère un fichier de base de données qui était précédemment attaché à une session de base de données.</span><span class="sxs-lookup"><span data-stu-id="75091-106">The **JetDetachDatabase** function releases a database file that was previously attached to a database session.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a><span data-ttu-id="75091-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75091-107">Parameters</span></span>

<span data-ttu-id="75091-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="75091-108">*sesid*</span></span>

<span data-ttu-id="75091-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="75091-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="75091-110">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="75091-110">*szFilename*</span></span>

<span data-ttu-id="75091-111">Nom de la base de données à détacher.</span><span class="sxs-lookup"><span data-stu-id="75091-111">The name of the database to detach.</span></span> <span data-ttu-id="75091-112">Si *szFilename* a la **valeur null** ou est une chaîne vide, toutes les bases de données attachées à *sesid* seront détachées.</span><span class="sxs-lookup"><span data-stu-id="75091-112">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

### <a name="return-value"></a><span data-ttu-id="75091-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75091-113">Return Value</span></span>

<span data-ttu-id="75091-114">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="75091-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="75091-115">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="75091-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75091-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="75091-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="75091-117">Description</span><span class="sxs-lookup"><span data-stu-id="75091-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75091-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="75091-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="75091-119">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="75091-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75091-120">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="75091-120">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="75091-121">La base de données est en cours de sauvegarde et ne peut pas être détachée.</span><span class="sxs-lookup"><span data-stu-id="75091-121">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75091-122">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="75091-122">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="75091-123">La base de données a été ouverte par <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span><span class="sxs-lookup"><span data-stu-id="75091-123">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="75091-124">Les bases de données doivent être fermées avant le détachement.</span><span class="sxs-lookup"><span data-stu-id="75091-124">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75091-125">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="75091-125">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="75091-126">La base de données n’a pas été attachée précédemment (consultez <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="75091-126">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75091-127">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="75091-127">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="75091-128">Une tentative de détachement d’une base de données a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="75091-128">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="75091-129">Notes</span><span class="sxs-lookup"><span data-stu-id="75091-129">Remarks</span></span>

<span data-ttu-id="75091-130">Si une base de données attachée a été ouverte (avec [JetAttachDatabase](./jetattachdatabase-function.md)), elle doit être fermée avec [JetCloseDatabase](./jetclosedatabase-function.md) avant le détachement.</span><span class="sxs-lookup"><span data-stu-id="75091-130">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="75091-131">Windows 2000 uniquement : les bases de données qui n’ont pas été détachées avant l’appel de [JetTerm](./jetterm-function.md) sont automatiquement rattachées lorsque [JetInit](./jetinit-function.md) est appelé par la suite.</span><span class="sxs-lookup"><span data-stu-id="75091-131">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="75091-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75091-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75091-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="75091-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="75091-134">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="75091-134">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75091-135"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="75091-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="75091-136">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="75091-136">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75091-137"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="75091-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="75091-138">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="75091-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75091-139"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="75091-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="75091-140">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="75091-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75091-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="75091-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="75091-142">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="75091-142">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75091-143"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="75091-143"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="75091-144">Implémenté en tant que <strong>JetDetachDatabaseW</strong> (Unicode) et <strong>JetDetachDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="75091-144">Implemented as <strong>JetDetachDatabaseW</strong> (Unicode) and <strong>JetDetachDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="75091-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75091-145">See Also</span></span>

[<span data-ttu-id="75091-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="75091-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="75091-147">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="75091-147">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="75091-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="75091-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="75091-149">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="75091-149">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="75091-150">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="75091-150">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="75091-151">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="75091-151">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="75091-152">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="75091-152">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="75091-153">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="75091-153">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="75091-154">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="75091-154">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="75091-155">JetTerm</span><span class="sxs-lookup"><span data-stu-id="75091-155">JetTerm</span></span>](./jetterm-function.md)
