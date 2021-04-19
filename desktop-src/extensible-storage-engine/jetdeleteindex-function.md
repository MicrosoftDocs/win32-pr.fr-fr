---
description: 'En savoir plus sur : fonction JetDeleteIndex'
title: JetDeleteIndex fonction)
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523693"
---
# <a name="jetdeleteindex-function"></a><span data-ttu-id="503ea-103">JetDeleteIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="503ea-103">JetDeleteIndex Function</span></span>


<span data-ttu-id="503ea-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="503ea-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeleteindex-function"></a><span data-ttu-id="503ea-105">JetDeleteIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="503ea-105">JetDeleteIndex Function</span></span>

<span data-ttu-id="503ea-106">La fonction **JetDeleteIndex** supprime un index d’une table.</span><span class="sxs-lookup"><span data-stu-id="503ea-106">The **JetDeleteIndex** function deletes an index from a table.</span></span>

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="503ea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="503ea-107">Parameters</span></span>

<span data-ttu-id="503ea-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="503ea-108">*sesid*</span></span>

<span data-ttu-id="503ea-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="503ea-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="503ea-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="503ea-110">*tableid*</span></span>

<span data-ttu-id="503ea-111">Table qui contient la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="503ea-111">The table that contains the column that is to be deleted.</span></span>

<span data-ttu-id="503ea-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="503ea-112">*szIndexName*</span></span>

<span data-ttu-id="503ea-113">Nom de l’index à supprimer.</span><span class="sxs-lookup"><span data-stu-id="503ea-113">The name of the index to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="503ea-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="503ea-114">Return Value</span></span>

<span data-ttu-id="503ea-115">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="503ea-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="503ea-116">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="503ea-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="503ea-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="503ea-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="503ea-118">Description</span><span class="sxs-lookup"><span data-stu-id="503ea-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="503ea-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="503ea-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="503ea-120">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="503ea-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="503ea-121">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="503ea-121">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="503ea-122">Une tentative a été effectuée pour supprimer un index d’une table fixe (par exemple, un index créé avec JET_bitTableCreateFixedDDL).</span><span class="sxs-lookup"><span data-stu-id="503ea-122">An attempt was made to delete an index from a fixed table (for example, one created with JET_bitTableCreateFixedDDL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="503ea-123">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="503ea-123">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="503ea-124">Une tentative de suppression d’un index d’une table de modèle a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="503ea-124">An attempt was made to delete an index from a template table.</span></span> <span data-ttu-id="503ea-125">Une table de modèle a un DDL fixe.</span><span class="sxs-lookup"><span data-stu-id="503ea-125">A template table has fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="503ea-126">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="503ea-126">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="503ea-127">L’index nommé dans <em>szIndexName</em> est introuvable.</span><span class="sxs-lookup"><span data-stu-id="503ea-127">The index named in <em>szIndexName</em> was not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="503ea-128">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="503ea-128">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="503ea-129">La table ne peut pas être mise à jour parce qu’elle a été ouverte en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="503ea-129">The table cannot be updated because it was opened read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="503ea-130">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="503ea-130">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="503ea-131">Plusieurs threads ont tenté d’utiliser la même session de base de données.</span><span class="sxs-lookup"><span data-stu-id="503ea-131">Multiple threads attempted to use the same database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="503ea-132">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="503ea-132">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="503ea-133">La transaction a été ouverte en tant que transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="503ea-133">The transaction was opened as a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="503ea-134">Notes</span><span class="sxs-lookup"><span data-stu-id="503ea-134">Remarks</span></span>

<span data-ttu-id="503ea-135">En cas de réussite, l’index est supprimé et ne peut donc pas être utilisé par la suite.</span><span class="sxs-lookup"><span data-stu-id="503ea-135">When successful, the index is deleted and therefore cannot be used subsequently.</span></span> <span data-ttu-id="503ea-136">Il ne doit y avoir aucune transaction active utilisant l’index.</span><span class="sxs-lookup"><span data-stu-id="503ea-136">There must not be any active transaction using the index.</span></span>

<span data-ttu-id="503ea-137">En cas de réussite, la devise est définie avant le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="503ea-137">On success, the currency is set before the first record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="503ea-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="503ea-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="503ea-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="503ea-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="503ea-140">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="503ea-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="503ea-141"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="503ea-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="503ea-142">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="503ea-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="503ea-143"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="503ea-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="503ea-144">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="503ea-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="503ea-145"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="503ea-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="503ea-146">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="503ea-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="503ea-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="503ea-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="503ea-148">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="503ea-148">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="503ea-149"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="503ea-149"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="503ea-150">Implémenté en tant que <strong>JetDeleteIndexW</strong> (Unicode) et <strong>JetDeleteIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="503ea-150">Implemented as <strong>JetDeleteIndexW</strong> (Unicode) and <strong>JetDeleteIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="503ea-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="503ea-151">See Also</span></span>

[<span data-ttu-id="503ea-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="503ea-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="503ea-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="503ea-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="503ea-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="503ea-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="503ea-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="503ea-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="503ea-156">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="503ea-156">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="503ea-157">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="503ea-157">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)
