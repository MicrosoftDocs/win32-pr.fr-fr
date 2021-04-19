---
description: 'En savoir plus sur : fonction JetDeleteTable'
title: JetDeleteTable fonction)
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531213"
---
# <a name="jetdeletetable-function"></a><span data-ttu-id="d1d31-103">JetDeleteTable fonction)</span><span class="sxs-lookup"><span data-stu-id="d1d31-103">JetDeleteTable Function</span></span>


<span data-ttu-id="d1d31-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d1d31-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletetable-function"></a><span data-ttu-id="d1d31-105">JetDeleteTable fonction)</span><span class="sxs-lookup"><span data-stu-id="d1d31-105">JetDeleteTable Function</span></span>

<span data-ttu-id="d1d31-106">La fonction **JetDeleteTable** supprime une table dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="d1d31-106">The **JetDeleteTable** function deletes a table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a><span data-ttu-id="d1d31-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1d31-107">Parameters</span></span>

<span data-ttu-id="d1d31-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d1d31-108">*sesid*</span></span>

<span data-ttu-id="d1d31-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="d1d31-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="d1d31-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="d1d31-110">*dbid*</span></span>

<span data-ttu-id="d1d31-111">Identificateur de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="d1d31-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="d1d31-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="d1d31-112">*szTableName*</span></span>

<span data-ttu-id="d1d31-113">Nom de la table à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d1d31-113">The name of the table to delete.</span></span>

### <a name="return-value"></a><span data-ttu-id="d1d31-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d1d31-114">Return Value</span></span>

<span data-ttu-id="d1d31-115">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="d1d31-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d1d31-116">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d1d31-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d1d31-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d1d31-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="d1d31-118">Description</span><span class="sxs-lookup"><span data-stu-id="d1d31-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1d31-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d1d31-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d1d31-120">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d1d31-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1d31-121">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="d1d31-121">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="d1d31-122">Une tentative a été effectuée pour supprimer une table alors qu’une autre session a un ID de table ouvert (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) avec <a href="gg294118(v=exchg.10).md">JetOpenTable</a> ou <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span><span class="sxs-lookup"><span data-stu-id="d1d31-122">An attempt was made to delete a table while another session has an open table ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) with <a href="gg294118(v=exchg.10).md">JetOpenTable</a> or <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1d31-123">Table JET_errCannotDeletetemporary</span><span class="sxs-lookup"><span data-stu-id="d1d31-123">JET_errCannotDeletetemporary table</span></span></p></td>
<td><p><span data-ttu-id="d1d31-124">Une tentative de suppression d’une table temporaire a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="d1d31-124">An attempt was made to delete a temporary table.</span></span> <span data-ttu-id="d1d31-125">Une table temporaire est automatiquement supprimée lorsqu’elle est fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="d1d31-125">A temporary table is automatically deleted when it is closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1d31-126">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="d1d31-126">JET_errCannotDeleteTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="d1d31-127">Une tentative de suppression d’une table de modèle a été effectuée, autrement dit, une table à partir de laquelle la DDL peut être héritée.</span><span class="sxs-lookup"><span data-stu-id="d1d31-127">An attempt was made to delete a template table, that is, a table from which DDL can be inherited.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="d1d31-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1d31-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1d31-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d1d31-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d1d31-130">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d1d31-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1d31-131"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d1d31-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d1d31-132">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d1d31-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1d31-133"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d1d31-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d1d31-134">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d1d31-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1d31-135"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="d1d31-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d1d31-136">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d1d31-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1d31-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d1d31-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d1d31-138">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d1d31-138">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1d31-139"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d1d31-139"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d1d31-140">Implémenté en tant que <strong>JetDeleteTableW</strong> (Unicode) et <strong>JetDeleteTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d1d31-140">Implemented as <strong>JetDeleteTableW</strong> (Unicode) and <strong>JetDeleteTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d1d31-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1d31-141">See Also</span></span>

[<span data-ttu-id="d1d31-142">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="d1d31-142">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="d1d31-143">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d1d31-143">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d1d31-144">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d1d31-144">JetCloseTable</span></span>](./jetclosetable-function.md)
