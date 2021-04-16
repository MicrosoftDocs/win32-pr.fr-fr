---
description: 'En savoir plus sur : fonction JetCloseTable'
title: JetCloseTable fonction)
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531101"
---
# <a name="jetclosetable-function"></a><span data-ttu-id="0683e-103">JetCloseTable fonction)</span><span class="sxs-lookup"><span data-stu-id="0683e-103">JetCloseTable Function</span></span>


<span data-ttu-id="0683e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="0683e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosetable-function"></a><span data-ttu-id="0683e-105">JetCloseTable fonction)</span><span class="sxs-lookup"><span data-stu-id="0683e-105">JetCloseTable Function</span></span>

<span data-ttu-id="0683e-106">La fonction **JetCloseTable** ferme une table ouverte dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="0683e-106">The **JetCloseTable** function closes an open table in a database.</span></span> <span data-ttu-id="0683e-107">La table peut être une table temporaire ou une table normale.</span><span class="sxs-lookup"><span data-stu-id="0683e-107">The table may be a temporary table or a normal table.</span></span>

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a><span data-ttu-id="0683e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0683e-108">Parameters</span></span>

<span data-ttu-id="0683e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0683e-109">*sesid*</span></span>

<span data-ttu-id="0683e-110">Identifie le contexte de session de base de données qui sera utilisé pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="0683e-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="0683e-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="0683e-111">*tableid*</span></span>

<span data-ttu-id="0683e-112">Identifie la table à fermer.</span><span class="sxs-lookup"><span data-stu-id="0683e-112">Identifies the table to be closed.</span></span>

<span data-ttu-id="0683e-113">Définissez *TableID* sur JET_tableidNil pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0683e-113">Set *tableid* to JET_tableidNil to release memory.</span></span>

### <a name="return-value"></a><span data-ttu-id="0683e-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0683e-114">Return Value</span></span>

<span data-ttu-id="0683e-115">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="0683e-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0683e-116">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0683e-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0683e-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0683e-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="0683e-118">Description</span><span class="sxs-lookup"><span data-stu-id="0683e-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0683e-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0683e-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0683e-120">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0683e-120">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0683e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0683e-121">Remarks</span></span>

<span data-ttu-id="0683e-122">Cette fonction doit être appelée sur toutes les tables ouvertes avec [JetOpenTable](./jetopentable-function.md).</span><span class="sxs-lookup"><span data-stu-id="0683e-122">This function must be called on all tables opened with [JetOpenTable](./jetopentable-function.md).</span></span>

<span data-ttu-id="0683e-123">L’exception à cette règle se produit lorsque [JetOpenTable](./jetopentable-function.md) est appelé dans une transaction et que la transaction est restaurée (avec [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="0683e-123">The exception to this rule happens when [JetOpenTable](./jetopentable-function.md) is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="0683e-124">Lors de la restauration d’une transaction, la table est fermée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0683e-124">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="0683e-125">Dans ce cas, il s’agit d’une erreur de fermeture de la table avec **JetCloseTable**.</span><span class="sxs-lookup"><span data-stu-id="0683e-125">In this case, it is an error to close the table with **JetCloseTable**.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0683e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0683e-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0683e-127"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0683e-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0683e-128">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="0683e-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0683e-129"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="0683e-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0683e-130">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0683e-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0683e-131"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="0683e-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0683e-132">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="0683e-132">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0683e-133"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="0683e-133"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0683e-134">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0683e-134">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0683e-135"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0683e-135"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0683e-136">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0683e-136">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0683e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0683e-137">See Also</span></span>

[<span data-ttu-id="0683e-138">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0683e-138">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0683e-139">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0683e-139">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0683e-140">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0683e-140">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0683e-141">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0683e-141">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0683e-142">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="0683e-142">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="0683e-143">JetRollback</span><span class="sxs-lookup"><span data-stu-id="0683e-143">JetRollback</span></span>](./jetrollback-function.md)
