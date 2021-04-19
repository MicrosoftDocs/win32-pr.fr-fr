---
description: 'En savoir plus sur : fonction JetDeleteColumn2'
title: JetDeleteColumn2 fonction)
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522467"
---
# <a name="jetdeletecolumn2-function"></a><span data-ttu-id="06918-103">JetDeleteColumn2 fonction)</span><span class="sxs-lookup"><span data-stu-id="06918-103">JetDeleteColumn2 Function</span></span>


<span data-ttu-id="06918-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="06918-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn2-function"></a><span data-ttu-id="06918-105">JetDeleteColumn2 fonction)</span><span class="sxs-lookup"><span data-stu-id="06918-105">JetDeleteColumn2 Function</span></span>

<span data-ttu-id="06918-106">La fonction **JetDeleteColumn2** supprime une colonne d’une table de base de données ESE et permet de définir une option *Grbit* .</span><span class="sxs-lookup"><span data-stu-id="06918-106">The **JetDeleteColumn2** function deletes a column from an ESE database table and enables a *grbit* option to be set.</span></span>

<span data-ttu-id="06918-107">**Windows XP : JetDeleteColumn2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06918-107">**Windows XP:  JetDeleteColumn2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="06918-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06918-108">Parameters</span></span>

<span data-ttu-id="06918-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="06918-109">*sesid*</span></span>

<span data-ttu-id="06918-110">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="06918-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="06918-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="06918-111">*tableid*</span></span>

<span data-ttu-id="06918-112">Table qui contient la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="06918-112">The table that contains the column to be deleted.</span></span>

<span data-ttu-id="06918-113">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="06918-113">*szColumnName*</span></span>

<span data-ttu-id="06918-114">Nom de la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="06918-114">The name of the column to be deleted.</span></span>

<span data-ttu-id="06918-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="06918-115">*grbit*</span></span>

<span data-ttu-id="06918-116">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="06918-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06918-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="06918-117">Value</span></span></p></th>
<th><p><span data-ttu-id="06918-118">Signification</span><span class="sxs-lookup"><span data-stu-id="06918-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06918-119">JET_bitDeleteColumnIgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="06918-119">JET_bitDeleteColumnIgnoreTemplateColumns</span></span></p></td>
<td><p><span data-ttu-id="06918-120">La définition de JET_bitDeleteColumIgnoreTemplateColumns oblige l’API à tenter uniquement de supprimer des colonnes dans la table dérivée.</span><span class="sxs-lookup"><span data-stu-id="06918-120">Setting JET_bitDeleteColumIgnoreTemplateColumns will cause the API to only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="06918-121">Si une colonne de ce nom existe dans la table de base, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="06918-121">If a column of that name exists in the base table it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="06918-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06918-122">Return Value</span></span>

<span data-ttu-id="06918-123">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="06918-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="06918-124">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="06918-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06918-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="06918-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="06918-126">Description</span><span class="sxs-lookup"><span data-stu-id="06918-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06918-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="06918-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="06918-128">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="06918-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06918-129">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="06918-129">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="06918-130">La colonne est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="06918-130">The column is currently in use.</span></span> <span data-ttu-id="06918-131">Il est peut-être actuellement utilisé par un index.</span><span class="sxs-lookup"><span data-stu-id="06918-131">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06918-132">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="06918-132">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="06918-133">Une tentative de modification du DDL fixe a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="06918-133">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06918-134">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="06918-134">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="06918-135">La colonne nommée dans <em>szColumnName</em> existe dans la table de modèle, et la DDL d’une table de modèle ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="06918-135">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06918-136">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="06918-136">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="06918-137">Cela peut être retourné si un nom incorrect pour <em>szColumnName</em> a été donné.</span><span class="sxs-lookup"><span data-stu-id="06918-137">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06918-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="06918-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="06918-139">La table n’est pas accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="06918-139">The table is not writable.</span></span> <span data-ttu-id="06918-140">Cela peut être retourné si la base de données a été ouverte en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="06918-140">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06918-141">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="06918-141">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="06918-142">La transaction est une transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="06918-142">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="06918-143">Notes</span><span class="sxs-lookup"><span data-stu-id="06918-143">Remarks</span></span>

<span data-ttu-id="06918-144">L’appel de [JetDeleteColumn](./jetdeletecolumn-function.md) est identique à l’appel de **JetDeleteColumn2** avec *Grbit* défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="06918-144">Calling [JetDeleteColumn](./jetdeletecolumn-function.md) is identical to calling **JetDeleteColumn2** with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="06918-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06918-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06918-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="06918-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="06918-147">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06918-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06918-148"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="06918-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="06918-149">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="06918-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06918-150"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="06918-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="06918-151">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="06918-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06918-152"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="06918-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="06918-153">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="06918-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06918-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="06918-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="06918-155">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="06918-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06918-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="06918-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="06918-157">Implémenté en tant que <strong>JetDeleteColumn2W</strong> (Unicode) et <strong>JetDeleteColumn2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="06918-157">Implemented as <strong>JetDeleteColumn2W</strong> (Unicode) and <strong>JetDeleteColumn2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="06918-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06918-158">See Also</span></span>

[<span data-ttu-id="06918-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="06918-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="06918-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="06918-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="06918-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="06918-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="06918-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="06918-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="06918-163">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="06918-163">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)
