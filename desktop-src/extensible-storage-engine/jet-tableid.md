---
description: 'En savoir plus sur : JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536181"
---
# <a name="jet_tableid"></a><span data-ttu-id="07489-103">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="07489-103">JET_TABLEID</span></span>


<span data-ttu-id="07489-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="07489-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tableid"></a><span data-ttu-id="07489-105">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="07489-105">JET_TABLEID</span></span>

<span data-ttu-id="07489-106">Le type de données JET_TABLEID contient un handle vers le curseur de base de données à utiliser pour un appel à l’API JET.</span><span class="sxs-lookup"><span data-stu-id="07489-106">The JET_TABLEID data type contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="07489-107">Un curseur ne peut être utilisé qu’avec la session qui a été utilisée pour ouvrir ce curseur.</span><span class="sxs-lookup"><span data-stu-id="07489-107">A cursor can only be used with the session that was used to open that cursor.</span></span>

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a><span data-ttu-id="07489-108">Types de données</span><span class="sxs-lookup"><span data-stu-id="07489-108">Data Types</span></span>

<span data-ttu-id="07489-109">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="07489-109">JET_TABLEID</span></span>

<span data-ttu-id="07489-110">La **valeur null** ou [JET_tableidNil](./invalid-handle-constants.md) peut être utilisée pour indiquer un handle de curseur non valide.</span><span class="sxs-lookup"><span data-stu-id="07489-110">Either **NULL** or [JET_tableidNil](./invalid-handle-constants.md) can be used to indicate an invalid cursor handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="07489-111">Notes</span><span class="sxs-lookup"><span data-stu-id="07489-111">Remarks</span></span>

<span data-ttu-id="07489-112">Un curseur gère l’utilisation d’une table pour le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="07489-112">A cursor manages the use of a table for the database engine.</span></span> <span data-ttu-id="07489-113">Un curseur peut effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="07489-113">A cursor can do the following tasks:</span></span>

  - <span data-ttu-id="07489-114">Analyser les enregistrements</span><span class="sxs-lookup"><span data-stu-id="07489-114">Scan records</span></span>

  - <span data-ttu-id="07489-115">Rechercher des enregistrements</span><span class="sxs-lookup"><span data-stu-id="07489-115">Search for records</span></span>

  - <span data-ttu-id="07489-116">Choisir l’ordre de tri et la visibilité effectifs de ces enregistrements</span><span class="sxs-lookup"><span data-stu-id="07489-116">Choose the effective sort order and visibility of those records</span></span>

  - <span data-ttu-id="07489-117">Créer, mettre à jour ou supprimer des enregistrements</span><span class="sxs-lookup"><span data-stu-id="07489-117">Create, update, or delete records</span></span>

  - <span data-ttu-id="07489-118">Modifier le schéma de la table</span><span class="sxs-lookup"><span data-stu-id="07489-118">Modify the schema of the table</span></span>

<span data-ttu-id="07489-119">Les fonctionnalités prises en charge du curseur peuvent changer à mesure que l’État ou le type de la table sous-jacente change.</span><span class="sxs-lookup"><span data-stu-id="07489-119">The supported functionality of the cursor might change as the status or type of the underlying table changes.</span></span> <span data-ttu-id="07489-120">Par exemple, une table temporaire peut ne pas autoriser la recherche de données lorsqu’elle est ouverte avec certaines options.</span><span class="sxs-lookup"><span data-stu-id="07489-120">For example, a temporary table might disallow searching for data when it is opened with certain options.</span></span> <span data-ttu-id="07489-121">Le curseur est toujours entièrement connecté à la table sous-jacente et interagit directement avec ces données, sans aucune mise en cache.</span><span class="sxs-lookup"><span data-stu-id="07489-121">The cursor is always fully connected to the underlying table and interacts with that data directly without any caching.</span></span> <span data-ttu-id="07489-122">Presque toutes les fonctionnalités ISAM principales exposées par ce moteur de base de données fonctionnent par le biais du curseur.</span><span class="sxs-lookup"><span data-stu-id="07489-122">Almost all of the core ISAM functionality that is exposed by this database engine is works through the cursor.</span></span>

<span data-ttu-id="07489-123">Un curseur peut être créé à l’aide de [JetOpenTable](./jetopentable-function.md) ou [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="07489-123">A cursor can be created using [JetOpenTable](./jetopentable-function.md) or [JetOpenTempTable](./jetopentemptable-function.md).</span></span> <span data-ttu-id="07489-124">Un curseur peut être dupliqué à l’aide de [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="07489-124">A cursor can be duplicated using [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="07489-125">Un curseur peut être explicitement fermé à l’aide de [JetCloseTable](./jetclosetable-function.md) ou d’une fermeture implicite à l’aide de [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="07489-125">A cursor can be explicitly closed using [JetCloseTable](./jetclosetable-function.md) or implicitly closed using [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span> <span data-ttu-id="07489-126">Un curseur peut également être fermé implicitement par [JetRollback](./jetrollback-function.md) s’il a été ouvert dans la transaction qui a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="07489-126">A cursor can also be implicitly closed by [JetRollback](./jetrollback-function.md) if it was opened in the transaction that was aborted.</span></span> <span data-ttu-id="07489-127">Le nombre maximal de curseurs qui peuvent être créés à un moment donné est contrôlé par [JET_paramMaxCursors](./resource-parameters.md), qui peut être configuré à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="07489-127">The maximum number of cursors that can be created at any one time is controlled by [JET_paramMaxCursors](./resource-parameters.md), which can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="07489-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07489-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07489-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="07489-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="07489-130">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="07489-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07489-131"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="07489-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="07489-132">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="07489-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07489-133"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="07489-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="07489-134">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="07489-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="07489-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07489-135">See Also</span></span>

[<span data-ttu-id="07489-136">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="07489-136">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="07489-137">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="07489-137">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="07489-138">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="07489-138">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="07489-139">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="07489-139">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="07489-140">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="07489-140">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="07489-141">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="07489-141">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="07489-142">JetRollback</span><span class="sxs-lookup"><span data-stu-id="07489-142">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="07489-143">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="07489-143">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="07489-144">JetTerm</span><span class="sxs-lookup"><span data-stu-id="07489-144">JetTerm</span></span>](./jetterm-function.md)
