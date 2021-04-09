---
description: 'En savoir plus sur : fonction JetDeleteColumn'
title: JetDeleteColumn fonction)
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954025"
---
# <a name="jetdeletecolumn-function"></a><span data-ttu-id="0f886-103">JetDeleteColumn fonction)</span><span class="sxs-lookup"><span data-stu-id="0f886-103">JetDeleteColumn Function</span></span>


<span data-ttu-id="0f886-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="0f886-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn-function"></a><span data-ttu-id="0f886-105">JetDeleteColumn fonction)</span><span class="sxs-lookup"><span data-stu-id="0f886-105">JetDeleteColumn Function</span></span>

<span data-ttu-id="0f886-106">La fonction **JetDeleteColumn** supprime une colonne d’une table de base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="0f886-106">The **JetDeleteColumn** function deletes a column from an ESE database table.</span></span>

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a><span data-ttu-id="0f886-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f886-107">Parameters</span></span>

<span data-ttu-id="0f886-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0f886-108">*sesid*</span></span>

<span data-ttu-id="0f886-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="0f886-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="0f886-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="0f886-110">*tableid*</span></span>

<span data-ttu-id="0f886-111">Table à partir de laquelle la colonne doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="0f886-111">The table from which to delete the column.</span></span>

<span data-ttu-id="0f886-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="0f886-112">*szColumnName*</span></span>

<span data-ttu-id="0f886-113">Nom de la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0f886-113">The name of the column to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="0f886-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f886-114">Return Value</span></span>

<span data-ttu-id="0f886-115">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="0f886-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0f886-116">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0f886-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f886-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0f886-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="0f886-118">Description</span><span class="sxs-lookup"><span data-stu-id="0f886-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f886-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0f886-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0f886-120">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0f886-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f886-121">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="0f886-121">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="0f886-122">La colonne est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0f886-122">The column is currently in use.</span></span> <span data-ttu-id="0f886-123">Il est peut-être actuellement utilisé par un index.</span><span class="sxs-lookup"><span data-stu-id="0f886-123">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f886-124">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="0f886-124">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="0f886-125">Une tentative de modification du DDL fixe a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="0f886-125">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f886-126">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="0f886-126">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="0f886-127">La colonne nommée dans <em>szColumnName</em> existe dans la table de modèle, et la DDL d’une table de modèle ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="0f886-127">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f886-128">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="0f886-128">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="0f886-129">Cela peut être retourné si un nom incorrect pour <em>szColumnName</em> a été donné.</span><span class="sxs-lookup"><span data-stu-id="0f886-129">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f886-130">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="0f886-130">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="0f886-131">La table n’est pas accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="0f886-131">The table is not writable.</span></span> <span data-ttu-id="0f886-132">Cela peut être retourné si la base de données a été ouverte en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0f886-132">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f886-133">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="0f886-133">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0f886-134">La transaction est une transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0f886-134">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0f886-135">Notes</span><span class="sxs-lookup"><span data-stu-id="0f886-135">Remarks</span></span>

<span data-ttu-id="0f886-136">L’appel de **JetDeleteColumn** est identique à l’appel de [JetDeleteColumn2](./jetdeletecolumn2-function.md) avec *Grbit* défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="0f886-136">Calling **JetDeleteColumn** is identical to calling [JetDeleteColumn2](./jetdeletecolumn2-function.md) with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="0f886-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f886-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f886-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0f886-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0f886-139">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="0f886-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f886-140"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="0f886-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0f886-141">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0f886-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f886-142"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="0f886-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0f886-143">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="0f886-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f886-144"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="0f886-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0f886-145">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0f886-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f886-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0f886-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0f886-147">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0f886-147">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f886-148"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0f886-148"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0f886-149">Implémenté en tant que <strong>JetDeleteColumnW</strong> (Unicode) et <strong>JetDeleteColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0f886-149">Implemented as <strong>JetDeleteColumnW</strong> (Unicode) and <strong>JetDeleteColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0f886-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f886-150">See Also</span></span>

[<span data-ttu-id="0f886-151">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0f886-151">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0f886-152">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0f886-152">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0f886-153">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0f886-153">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0f886-154">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0f886-154">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0f886-155">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="0f886-155">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
