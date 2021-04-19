---
description: 'En savoir plus sur : fonction JetIntersectIndexes'
title: Fonction JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514383"
---
# <a name="jetintersectindexes-function"></a><span data-ttu-id="5411e-103">Fonction JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="5411e-103">JetIntersectIndexes Function</span></span>


<span data-ttu-id="5411e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="5411e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetintersectindexes-function"></a><span data-ttu-id="5411e-105">Fonction JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="5411e-105">JetIntersectIndexes Function</span></span>

<span data-ttu-id="5411e-106">La fonction **JetIntersectIndexes** calcule l’intersection entre plusieurs jeux d’entrées d’index à partir d’index secondaires différents sur la même table.</span><span class="sxs-lookup"><span data-stu-id="5411e-106">The **JetIntersectIndexes** function computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="5411e-107">Cette opération est utile pour Rechercher l’ensemble des enregistrements d’une table qui correspondent à plusieurs critères qui peuvent être exprimés à l’aide de plages d’index.</span><span class="sxs-lookup"><span data-stu-id="5411e-107">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span>

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5411e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5411e-108">Parameters</span></span>

<span data-ttu-id="5411e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5411e-109">*sesid*</span></span>

<span data-ttu-id="5411e-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="5411e-110">The session to use for this call.</span></span>

<span data-ttu-id="5411e-111">*rgindexrange*</span><span class="sxs-lookup"><span data-stu-id="5411e-111">*rgindexrange*</span></span>

<span data-ttu-id="5411e-112">Pointeur vers un tableau de structures [JET_IndexRange](./jet-indexrange-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="5411e-112">A pointer to an array of [JET_IndexRange](./jet-indexrange-structure.md) structures.</span></span> <span data-ttu-id="5411e-113">Chaque structure inclut une [JET_TABLEID](./jet-tableid.md) qui a été configurée pour contenir l’une des plages d’index à croiser.</span><span class="sxs-lookup"><span data-stu-id="5411e-113">Each structure includes a [JET_TABLEID](./jet-tableid.md) that has been set up to hold one of the index ranges to be intersected.</span></span> <span data-ttu-id="5411e-114">Pour plus d’informations, consultez [JET_IndexRange](./jet-indexrange-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5411e-114">For more information, see [JET_IndexRange](./jet-indexrange-structure.md).</span></span>

<span data-ttu-id="5411e-115">*cindexrange*</span><span class="sxs-lookup"><span data-stu-id="5411e-115">*cindexrange*</span></span>

<span data-ttu-id="5411e-116">Nombre de structures de [JET_IndexRange](./jet-indexrange-structure.md) dans le tableau contenues dans le paramètre *rgindexrange* .</span><span class="sxs-lookup"><span data-stu-id="5411e-116">The number of [JET_IndexRange](./jet-indexrange-structure.md) structures in the array that is contained in the *rgindexrange* parameter.</span></span>

<span data-ttu-id="5411e-117">*precordlist*</span><span class="sxs-lookup"><span data-stu-id="5411e-117">*precordlist*</span></span>

<span data-ttu-id="5411e-118">Pointeur vers une structure [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="5411e-118">Pointer to a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="5411e-119">Cette structure sera remplie avec suffisamment d’informations pour parcourir la table temporaire avec les résultats de **JetIntersectIndexes**.</span><span class="sxs-lookup"><span data-stu-id="5411e-119">This structure will be populated with enough information to traverse the temporary table with the results from **JetIntersectIndexes**.</span></span>

<span data-ttu-id="5411e-120">Mémoire tampon de sortie qui reçoit une structure [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="5411e-120">The output buffer that receives a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="5411e-121">La structure contient une description du jeu de résultats de l’intersection.</span><span class="sxs-lookup"><span data-stu-id="5411e-121">The structure contains a description of the result set of the intersection.</span></span>

<span data-ttu-id="5411e-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5411e-122">*grbit*</span></span>

<span data-ttu-id="5411e-123">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="5411e-123">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="5411e-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5411e-124">Return Value</span></span>

<span data-ttu-id="5411e-125">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="5411e-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5411e-126">Pour plus d’informations sur les erreurs ESE, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5411e-126">For more information about ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5411e-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5411e-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="5411e-128">Description</span><span class="sxs-lookup"><span data-stu-id="5411e-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5411e-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5411e-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5411e-130">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5411e-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5411e-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5411e-132">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5411e-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5411e-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5411e-134">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="5411e-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5411e-135"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5411e-135"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-136">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="5411e-136">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="5411e-137">L’une des options demandées n’est pas valide, a été utilisée de manière incorrecte ou n’a pas été implémentée.</span><span class="sxs-lookup"><span data-stu-id="5411e-137">One of the options requested was invalid, used incorrectly, or not implemented.</span></span></p>
<p><span data-ttu-id="5411e-138">Cette erreur est retournée par <strong>JetIntersectIndexes</strong> quand :</span><span class="sxs-lookup"><span data-stu-id="5411e-138">This error is returned by <strong>JetIntersectIndexes</strong> when:</span></span></p>
<p><span data-ttu-id="5411e-139">Le <em>Grbit</em> contenu dans la structure <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> pointée par n’importe quel élément dans le tableau <em>rgindexrange</em> n’est pas égal à JET_bitRecordInIndex.</span><span class="sxs-lookup"><span data-stu-id="5411e-139">The <em>grbit</em> contained in the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure pointed to by any element in the <em>rgindexrange</em> array is not equal to JET_bitRecordInIndex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-140">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5411e-140">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5411e-141">L’un des paramètres fournis contient une valeur inattendue ou une valeur qui n’est pas cohérente lorsqu’elle est associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="5411e-141">One of the parameters provided contains an unexpected value or a value that is inconsistent when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="5411e-142">Cette erreur est retournée par <strong>JetIntersectIndexes</strong> pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="5411e-142">This error is returned by <strong>JetIntersectIndexes</strong> for of the following reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="5411e-143">Le paramètre <em>precordlist</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="5411e-143">The <em>precordlist</em> parameter is NULL.</span></span></p></li>
<li><p><span data-ttu-id="5411e-144">Le membre <strong>cbStruct</strong> de la structure <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> spécifiée dans le paramètre <em>precordlist</em> n’est pas égal à la taille de la structure <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="5411e-144">The <strong>cbStruct</strong> member of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure specified in the <em>precordlist</em> parameter is not equal to size of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="5411e-145">Le paramètre <em>cindexrange</em> est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5411e-145">The <em>cindexrange</em> parameter is zero.</span></span></p></li>
<li><p><span data-ttu-id="5411e-146">Le paramètre <em>cindexrange</em> est supérieur à 64.</span><span class="sxs-lookup"><span data-stu-id="5411e-146">The <em>cindexrange</em> parameter is greater than 64.</span></span></p></li>
<li><p><span data-ttu-id="5411e-147">Le membre <strong>cbStruct</strong> pour tout élément du tableau spécifié par le paramètre <em>rgindexrange</em> n’est pas égal à la taille de la structure <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</span><span class="sxs-lookup"><span data-stu-id="5411e-147">The <strong>cbStruct</strong> member for any element in the array specified by the <em>rgindexrange</em> parameter is not equal to the size of the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="5411e-148">Les éléments du tableau <em>rgindexrange</em> contiennent <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s de tables différentes.</span><span class="sxs-lookup"><span data-stu-id="5411e-148">The elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s from different tables.</span></span></p></li>
<li><p><span data-ttu-id="5411e-149">Un élément du tableau <em>rgindexrange</em> contient un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> qui n’est pas positionné sur un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="5411e-149">An element in the <em>rgindexrange</em> array contains a <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> that is not positioned on a secondary index.</span></span></p></li>
<li><p><span data-ttu-id="5411e-150">Un ou plusieurs des éléments du tableau <em>rgindexrange</em> contiennent <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s placés sur le même index secondaire.</span><span class="sxs-lookup"><span data-stu-id="5411e-150">One or more of the elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s positioned on the same secondary index.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-151">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="5411e-151">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="5411e-152">Le descripteur de session n’est pas valide ou fait référence à une session fermée.</span><span class="sxs-lookup"><span data-stu-id="5411e-152">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="5411e-153">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="5411e-153">This error is not returned under all circumstances.</span></span> <span data-ttu-id="5411e-154">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="5411e-154">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-155">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5411e-155">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5411e-156">Impossible de terminer l’opération, car l’instance associée à la session n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="5411e-156">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-157">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="5411e-157">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="5411e-158">L’opération a échoué, car le moteur n’a pas pu allouer les ressources nécessaires à l’ouverture d’un nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="5411e-158">The operation failed because the engine could not allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="5411e-159">Les ressources de curseur sont configurées en appelant <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <em>JET_paramMaxCursors</em> spécifié dans le paramètre <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="5411e-159">Cursor resources are configured by calling <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxCursors</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="5411e-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="5411e-161">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="5411e-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="5411e-162"><strong>JetIntersectIndexes</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté.</span><span class="sxs-lookup"><span data-stu-id="5411e-162"><strong>JetIntersectIndexes</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="5411e-163">Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker.</span><span class="sxs-lookup"><span data-stu-id="5411e-163">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span> <span data-ttu-id="5411e-164"><strong>JetIntersectIndexes</strong> crée une table temporaire pour chaque <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> spécifiée dans le paramètre <em>rgindexrange</em> , et une table temporaire pour la sortie dans <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="5411e-164"><strong>JetIntersectIndexes</strong> will create one temporary table for each <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specified in the <em>rgindexrange</em> parameter, and one temporary table for the output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5411e-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5411e-166">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="5411e-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5411e-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5411e-168">Il n’est pas conforme d’utiliser la même session à partir de plusieurs threads en même temps.</span><span class="sxs-lookup"><span data-stu-id="5411e-168">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5411e-169"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5411e-169"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5411e-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5411e-171">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5411e-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-172">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="5411e-172">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="5411e-173">L’opération a échoué, car le moteur n’a pas pu allouer les ressources nécessaires pour mettre en cache les index de la table.</span><span class="sxs-lookup"><span data-stu-id="5411e-173">The operation failed because the engine could not allocate the resources required to cache the indices of the table.</span></span> <span data-ttu-id="5411e-174">Le nombre d’index dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <em>JET_paramMaxOpenTables</em> spécifié dans le paramètre <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="5411e-174">The number of indices whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-175">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="5411e-175">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="5411e-176">L’opération a échoué, car le moteur n’a pas pu allouer les ressources nécessaires pour mettre en cache le schéma de la table.</span><span class="sxs-lookup"><span data-stu-id="5411e-176">The operation failed because the engine could not allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="5411e-177">Le nombre de tables dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <em>JET_paramMaxOpenTables</em> spécifié dans le paramètre <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="5411e-177">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-178">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="5411e-178">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="5411e-179">L’opération a échoué, car le moteur n’a pas pu allouer les ressources requises pour créer une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="5411e-179">The operation failed because the engine could not allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="5411e-180">Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec JET_paramMaxTemporaryTables spécifié dans le paramètre <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="5411e-180">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with JET_paramMaxTemporaryTables specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5411e-181">En cas de réussite, une nouvelle table temporaire est retournée, qui contient les signets des enregistrements qui correspondent aux critères représentés par chacune des descriptions de la plage d’index d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5411e-181">On success, a new temporary table is returned that contains the bookmarks of the records that match the criteria represented by each of the input index range descriptions.</span></span>

<span data-ttu-id="5411e-182">En cas d’échec, la table temporaire contenant les résultats ne sera pas créée.</span><span class="sxs-lookup"><span data-stu-id="5411e-182">On failure, the temporary table containing the results will not be created.</span></span> <span data-ttu-id="5411e-183">L’état de la base de données temporaire peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="5411e-183">The state of the temporary database may be changed.</span></span> <span data-ttu-id="5411e-184">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="5411e-184">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span> <span data-ttu-id="5411e-185">La position actuelle du [JET_TABLEID](./jet-tableid.md)fourni à cette fonction peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="5411e-185">The current position of the [JET_TABLEID](./jet-tableid.md)s provided to this function may be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5411e-186">Notes</span><span class="sxs-lookup"><span data-stu-id="5411e-186">Remarks</span></span>

<span data-ttu-id="5411e-187">**JetIntersectIndexes** peut être utilisé pour filtrer efficacement les enregistrements d’une table selon plusieurs critères si ces critères peuvent être exprimés en termes d’index secondaires sur cette table.</span><span class="sxs-lookup"><span data-stu-id="5411e-187">**JetIntersectIndexes** can be used to efficiently filter the records in a table by multiple criteria if those criteria can be expressed in terms of the secondary indices over that table.</span></span> <span data-ttu-id="5411e-188">Par exemple, considérez que vous disposez d’une table très volumineuse contenant des personnes.</span><span class="sxs-lookup"><span data-stu-id="5411e-188">For example, consider that you have a very large table containing people.</span></span> <span data-ttu-id="5411e-189">La table peut comporter des colonnes pour son ID utilisateur, son prénom, son nom, etc.</span><span class="sxs-lookup"><span data-stu-id="5411e-189">The table can have columns for their user id, first name, last name, and so on.</span></span> <span data-ttu-id="5411e-190">Supposons que chacune de ces colonnes soit indexée séparément et que l’index primaire de la table soit sur l’ID d’utilisateur. Si vous souhaitez trouver tous les utilisateurs dont le prénom commence par un et dont le nom commence par G, vous devez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5411e-190">Suppose that each of these columns is indexed separately and that the primary index of the table is over user id. If you wanted to find everyone whose first name starts with an A and whose last name starts with G, you would perform the following steps:</span></span>

1.  <span data-ttu-id="5411e-191">Ouvrez un nouveau curseur sur la table et définissez ce curseur pour utiliser l’index sur la colonne « First Name ».</span><span class="sxs-lookup"><span data-stu-id="5411e-191">Open a new cursor on the table, and set that cursor to use the index over the "first name" column.</span></span> <span data-ttu-id="5411e-192">Configurez ensuite une plage d’index pour toutes les personnes dont le « prénom » a démarré avec « A », puis générez un [JET_IndexRange](./jet-indexrange-structure.md) struct contenant ce curseur.</span><span class="sxs-lookup"><span data-stu-id="5411e-192">Then setup an index range for all people whose "first name" started with 'A', and build a [JET_IndexRange](./jet-indexrange-structure.md) struct that contains this cursor.</span></span>

2.  <span data-ttu-id="5411e-193">Répétez l’étape 1 avec un nouveau curseur sur l’index « Last Name » pour toutes les personnes dont le « Last Name » a démarré avec « G ».</span><span class="sxs-lookup"><span data-stu-id="5411e-193">Repeat step 1 with a new cursor on the "last name" index for all people whose "last name" started with 'G'.</span></span>

3.  <span data-ttu-id="5411e-194">Transmettez ces critères à **JetIntersectIndexes** pour calculer le résultat dans une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="5411e-194">Pass these criteria to **JetIntersectIndexes** to compute the result into a temporary table.</span></span>

4.  <span data-ttu-id="5411e-195">Parcourez la table temporaire et récupérez chacun des enregistrements qui passent les critères par signet.</span><span class="sxs-lookup"><span data-stu-id="5411e-195">Traverse the temporary table and retrieve each of the records that pass the criteria by bookmark.</span></span>

<span data-ttu-id="5411e-196">La table temporaire contenant le jeu de résultats est une table simple avec une colonne qui contient le signet de chaque enregistrement ayant passé tous les critères utilisés pour calculer l’intersection.</span><span class="sxs-lookup"><span data-stu-id="5411e-196">The temporary table containing the result set is a simple table with one column that contains the bookmark of each record that passed all the criteria used to compute the intersection.</span></span> <span data-ttu-id="5411e-197">Le jeu de résultats est trié dans le même ordre que l’index primaire et ne contient pas d’entrées en double.</span><span class="sxs-lookup"><span data-stu-id="5411e-197">The result set is sorted in the same order as the primary index and contains no duplicate entries.</span></span> <span data-ttu-id="5411e-198">L’application peut énumérer les résultats de l’intersection en énumérant les lignes de la table temporaire, en extrayant le signet pour chaque résultat à l’aide de [JetRetrieveColumn](./jetretrievecolumn-function.md), puis en visitant l’enregistrement dans la base de données en appelant [JetGotoBookmark](./jetgotobookmark-function.md) avec ce signet sur un curseur positionné sur l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="5411e-198">The application can enumerate the results of the intersection by enumerating the rows in the temporary table, retrieving the bookmark for each result using [JetRetrieveColumn](./jetretrievecolumn-function.md), and then visiting the record in the database by calling [JetGotoBookmark](./jetgotobookmark-function.md) with that bookmark on a cursor positioned on the primary index.</span></span>

<span data-ttu-id="5411e-199">La table temporaire retournée par **JetIntersectIndexes** peut uniquement être analysée vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="5411e-199">The temporary table returned by **JetIntersectIndexes** can only be scanned in a forward direction.</span></span> <span data-ttu-id="5411e-200">Elle doit également être fermée via [JetCloseTable](./jetclosetable-function.md) lorsque l’analyse est terminée.</span><span class="sxs-lookup"><span data-stu-id="5411e-200">It should also be closed via [JetCloseTable](./jetclosetable-function.md) when the scan has been completed.</span></span> <span data-ttu-id="5411e-201">Pour plus d’informations sur les tables temporaires et leur fonctionnement, consultez [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="5411e-201">For more information about temporary tables and how they work, see [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

<span data-ttu-id="5411e-202">**JetIntersectIndexes** est généralement un moyen efficace et pratique de filtrer les enregistrements en fonction de plusieurs critères indexés.</span><span class="sxs-lookup"><span data-stu-id="5411e-202">**JetIntersectIndexes** is generally an efficient and convenient way to filter records based on multiple indexed criteria.</span></span> <span data-ttu-id="5411e-203">Toutefois, il existe des conseils importants qui doivent être suivis pour optimiser l’utilité de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5411e-203">However, there are some important tips that should be followed to maximize the usefulness of this feature.</span></span> <span data-ttu-id="5411e-204">Si vous savez que l’un des critères est tellement restrictif que la plage d’index résultante a très peu d’enregistrements, il est probablement préférable de simplement parcourir la plage d’index et de filtrer les enregistrements au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="5411e-204">If you know that one of the criteria is so restrictive that the resulting index range has very few records then it is probably better to simply walk that index range and filter the records at the application level.</span></span> <span data-ttu-id="5411e-205">En outre, si vous savez que vous avez des critères qui sont bien moins restrictifs que d’autres critères de votre intersection, vous pouvez envisager de supprimer ces critères de plus en moins restrictifs de l’intersection.</span><span class="sxs-lookup"><span data-stu-id="5411e-205">Further, if you know that you have criteria that are much less restrictive than other criteria in your intersection then you might consider dropping those much less restrictive criteria from the intersection.</span></span> <span data-ttu-id="5411e-206">Enfin, si vous savez que l’un des critères n’est pas tout à fait restrictif, de sorte que la plage d’index résultante est presque aussi importante que l’index primaire, il est peu probable que l’intersection avec cette plage d’index soit avantageuse (réduisez la taille de) l’ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="5411e-206">Finally, if you know that one of the criteria is not at all restrictive such that the resulting index range is almost as large as the primary index then it is unlikely that intersecting with that index range will benefit (reduce the size of) the result set.</span></span> <span data-ttu-id="5411e-207">Dans tous les cas, vous devez sélectionner des critères de manière à ce qu’ils prennent le moins d’entrées d’index possible en entrée et génèrent le jeu de signets le plus spécifique sur la sortie pour des performances maximales.</span><span class="sxs-lookup"><span data-stu-id="5411e-207">In all cases, you should be selecting criteria in a manner that will take the fewest possible index entries on input and generate the most specific set of bookmarks on output for maximum performance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5411e-208">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5411e-208">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5411e-209"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5411e-209"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5411e-210">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="5411e-210">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-211"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="5411e-211"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5411e-212">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5411e-212">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-213"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="5411e-213"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5411e-214">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="5411e-214">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5411e-215"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="5411e-215"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5411e-216">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5411e-216">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5411e-217"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5411e-217"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5411e-218">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5411e-218">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5411e-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5411e-219">See Also</span></span>

[<span data-ttu-id="5411e-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5411e-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5411e-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5411e-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5411e-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5411e-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5411e-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5411e-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5411e-224">JET_IndexRange</span><span class="sxs-lookup"><span data-stu-id="5411e-224">JET_IndexRange</span></span>](./jet-indexrange-structure.md)  
[<span data-ttu-id="5411e-225">JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="5411e-225">JET_RECORDLIST</span></span>](./jet-recordlist-structure.md)  
[<span data-ttu-id="5411e-226">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="5411e-226">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="5411e-227">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="5411e-227">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="5411e-228">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="5411e-228">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
