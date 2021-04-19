---
description: 'En savoir plus sur : fonction JetDetachDatabase2'
title: Fonction JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545004"
---
# <a name="jetdetachdatabase2-function"></a><span data-ttu-id="f0d0e-103">Fonction JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="f0d0e-103">JetDetachDatabase2 Function</span></span>


<span data-ttu-id="f0d0e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f0d0e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase2-function"></a><span data-ttu-id="f0d0e-105">Fonction JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="f0d0e-105">JetDetachDatabase2 Function</span></span>

<span data-ttu-id="f0d0e-106">La fonction **JetDetachDatabase2** libère un fichier de base de données qui était précédemment attaché à une session de base de données.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-106">The **JetDetachDatabase2** function releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="f0d0e-107">**Windows XP :**  **JetDetachDatabase2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-107">**Windows XP:**  **JetDetachDatabase2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f0d0e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0d0e-108">Parameters</span></span>

<span data-ttu-id="f0d0e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f0d0e-109">*sesid*</span></span>

<span data-ttu-id="f0d0e-110">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="f0d0e-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="f0d0e-111">*szFilename*</span></span>

<span data-ttu-id="f0d0e-112">Nom de la base de données à détacher.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-112">The name of the database to detach.</span></span> <span data-ttu-id="f0d0e-113">Si *szFilename* a la **valeur null** ou est une chaîne vide, toutes les bases de données attachées à *sesid* seront détachées.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-113">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

<span data-ttu-id="f0d0e-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f0d0e-114">*grbit*</span></span>

<span data-ttu-id="f0d0e-115">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-115">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0d0e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0d0e-116">Value</span></span></p></th>
<th><p><span data-ttu-id="f0d0e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="f0d0e-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0d0e-118">JET_bitForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="f0d0e-118">JET_bitForceCloseAndDetach</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-119">Force la fermeture et le détachement de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-119">Forces the database to be closed and detached.</span></span> <span data-ttu-id="f0d0e-120">Si JET_bitForceCloseAndDetach n’est pas pris en charge, JET_errForceDetachNotAllowed sera retourné.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-120">If JET_bitForceCloseAndDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0d0e-121">JET_bitForceDetach</span><span class="sxs-lookup"><span data-stu-id="f0d0e-121">JET_bitForceDetach</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-122">Force le détachement de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-122">Forces the database to be detached.</span></span> <span data-ttu-id="f0d0e-123">Si JET_bitForceDetach n’est pas pris en charge, JET_errForceDetachNotAllowed sera retourné.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-123">If JET_bitForceDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f0d0e-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f0d0e-124">Return Value</span></span>

<span data-ttu-id="f0d0e-125">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f0d0e-126">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f0d0e-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0d0e-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f0d0e-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="f0d0e-128">Description</span><span class="sxs-lookup"><span data-stu-id="f0d0e-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0d0e-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f0d0e-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-130">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0d0e-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="f0d0e-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-132">La base de données est en cours de sauvegarde et ne peut pas être détachée.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-132">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0d0e-133">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="f0d0e-133">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-134">La base de données a été ouverte par <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-134">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="f0d0e-135">Les bases de données doivent être fermées avant le détachement.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-135">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0d0e-136">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="f0d0e-136">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-137">La base de données n’a pas été attachée précédemment (consultez <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="f0d0e-137">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0d0e-138">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="f0d0e-138">JET_errForceDetachNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-139">JET_bitForceDetach n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-139">JET_bitForceDetach is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0d0e-140">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="f0d0e-140">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f0d0e-141">Une tentative de détachement d’une base de données a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-141">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f0d0e-142">Notes</span><span class="sxs-lookup"><span data-stu-id="f0d0e-142">Remarks</span></span>

<span data-ttu-id="f0d0e-143">Si une base de données attachée a été ouverte (avec [JetAttachDatabase](./jetattachdatabase-function.md)), elle doit être fermée avec [JetCloseDatabase](./jetclosedatabase-function.md) avant le détachement.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-143">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="f0d0e-144">Windows 2000 uniquement : les bases de données qui n’ont pas été détachées avant l’appel de [JetTerm](./jetterm-function.md) sont automatiquement rattachées lorsque [JetInit](./jetinit-function.md) est appelé par la suite.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-144">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f0d0e-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0d0e-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0d0e-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f0d0e-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d0e-147">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0d0e-148"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f0d0e-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d0e-149">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0d0e-150"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f0d0e-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d0e-151">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0d0e-152"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f0d0e-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d0e-153">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0d0e-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f0d0e-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d0e-155">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f0d0e-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0d0e-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f0d0e-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f0d0e-157">Implémenté en tant que <strong>JetDetachDatabase2W</strong> (Unicode) et <strong>JetDetachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f0d0e-157">Implemented as <strong>JetDetachDatabase2W</strong> (Unicode) and <strong>JetDetachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f0d0e-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0d0e-158">See Also</span></span>

[<span data-ttu-id="f0d0e-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f0d0e-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f0d0e-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f0d0e-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f0d0e-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f0d0e-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f0d0e-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f0d0e-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f0d0e-163">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="f0d0e-163">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="f0d0e-164">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="f0d0e-164">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="f0d0e-165">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="f0d0e-165">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="f0d0e-166">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="f0d0e-166">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="f0d0e-167">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="f0d0e-167">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="f0d0e-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="f0d0e-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="f0d0e-169">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="f0d0e-169">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="f0d0e-170">JetTerm</span><span class="sxs-lookup"><span data-stu-id="f0d0e-170">JetTerm</span></span>](./jetterm-function.md)
