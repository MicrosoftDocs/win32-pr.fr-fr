---
description: 'En savoir plus sur : fonction JetOpenTemporaryTable'
title: JetOpenTemporaryTable fonction)
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522122"
---
# <a name="jetopentemporarytable-function"></a><span data-ttu-id="b2432-103">JetOpenTemporaryTable fonction)</span><span class="sxs-lookup"><span data-stu-id="b2432-103">JetOpenTemporaryTable Function</span></span>


<span data-ttu-id="b2432-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b2432-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemporarytable-function"></a><span data-ttu-id="b2432-105">JetOpenTemporaryTable fonction)</span><span class="sxs-lookup"><span data-stu-id="b2432-105">JetOpenTemporaryTable Function</span></span>

<span data-ttu-id="b2432-106">La fonction **JetOpenTemporaryTable** crée une table volatile avec un index unique qui peut être utilisé pour stocker et récupérer des enregistrements, tout comme une table ordinaire créée via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="b2432-106">The **JetOpenTemporaryTable** function creates a volatile table with a single index that can be used to store and retrieve records, just like an ordinary table that is created via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

<span data-ttu-id="b2432-107">**Windows Vista :**  **JetOpenTemporaryTable** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2432-107">**Windows Vista:**  **JetOpenTemporaryTable** is introduced in Windows Vista.</span></span>

<span data-ttu-id="b2432-108">Les tables temporaires sont plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="b2432-108">Temporary tables are faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="b2432-109">Ils peuvent rapidement trier et effectuer la suppression des doublons sur les jeux d’enregistrements lorsqu’ils sont accessibles de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="b2432-109">They can quickly sort and perform duplicate removal on record sets when they are accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a><span data-ttu-id="b2432-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2432-110">Parameters</span></span>

<span data-ttu-id="b2432-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b2432-111">*sesid*</span></span>

<span data-ttu-id="b2432-112">Session qui sera utilisée pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="b2432-112">The session that will be used for this call.</span></span>

<span data-ttu-id="b2432-113">*popentemporarytable*</span><span class="sxs-lookup"><span data-stu-id="b2432-113">*popentemporarytable*</span></span>

<span data-ttu-id="b2432-114">Pointeur vers une structure [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) qui contient la description de la table temporaire à créer en entrée.</span><span class="sxs-lookup"><span data-stu-id="b2432-114">A pointer to a [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) structure that contains the description of the temporary table to create on input.</span></span> <span data-ttu-id="b2432-115">Après un appel réussi, la structure contient le handle vers les identifications de la table et de la colonne temporaires.</span><span class="sxs-lookup"><span data-stu-id="b2432-115">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span>

### <a name="return-value"></a><span data-ttu-id="b2432-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2432-116">Return Value</span></span>

<span data-ttu-id="b2432-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="b2432-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b2432-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b2432-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2432-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b2432-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="b2432-120">Description</span><span class="sxs-lookup"><span data-stu-id="b2432-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2432-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b2432-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b2432-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b2432-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-123">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b2432-123">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b2432-124">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="b2432-124">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="b2432-125"><strong>JetOpenTemporaryTable</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté.</span><span class="sxs-lookup"><span data-stu-id="b2432-125"><strong>JetOpenTemporaryTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="b2432-126">Le gestionnaire de tables temporaire alloue un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données stockées.</span><span class="sxs-lookup"><span data-stu-id="b2432-126">The temporary table manager will allocates a 1 MB chunk of address space for every temporary table created regardless of the amount of data is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b2432-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b2432-128">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a entraîné un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="b2432-128">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="b2432-129">Cette erreur est retournée par <strong>JetOpenTemporaryTable</strong> dans les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2432-129">This error is returned by <strong>JetOpenTemporaryTable</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2432-130">Le membre <strong>cbStruct</strong> de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> ne correspond pas à une version de cette structure qui est prise en charge par cette version du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="b2432-130">The <strong>cbStruct</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure does not correspond to a version of this structure that is supported by that version of the database engine</span></span></p></li>
<li><p><span data-ttu-id="b2432-131">Le membre <strong>cbKeyMost</strong> de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> est inférieur à JET_cbKeyMostMin.</span><span class="sxs-lookup"><span data-stu-id="b2432-131">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is less than JET_cbKeyMostMin.</span></span></p></li>
<li><p><span data-ttu-id="b2432-132">Le membre <strong>cbKeyMost</strong> de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> est plus grand que la plus grande valeur prise en charge pour la taille de page de la base de données de l’instance (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="b2432-132">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than the largest supported value for the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="b2432-133">Pour plus d’informations, consultez le paramètre JET_paramKeyMost dans la liste des <a href="gg269241(v=exchg.10).md">paramètres d’information</a> .</span><span class="sxs-lookup"><span data-stu-id="b2432-133">See the JET_paramKeyMost parameter in the list of <a href="gg269241(v=exchg.10).md">Informational Parameters</a> for more information.</span></span></p></li>
<li><p><span data-ttu-id="b2432-134">Le membre cbVarSegMac de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> est plus grand que le membre <strong>cbKeyMost</strong> .</span><span class="sxs-lookup"><span data-stu-id="b2432-134">The cbVarSegMac member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than The <strong>cbKeyMost</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b2432-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b2432-136">Impossible d’effectuer l’opération, car l’instance qui a été associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="b2432-136">The operation cannot complete because the instance that was associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b2432-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b2432-138">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b2432-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b2432-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b2432-140">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="b2432-140">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b2432-141"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b2432-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b2432-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b2432-143">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="b2432-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b2432-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b2432-145">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="b2432-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b2432-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b2432-147">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="b2432-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b2432-148"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b2432-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-149">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="b2432-149">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="b2432-150">Le descripteur de session n’est pas valide ou fait référence à une session fermée.</span><span class="sxs-lookup"><span data-stu-id="b2432-150">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="b2432-151"><strong>Remarque</strong>  Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="b2432-151"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="b2432-152">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="b2432-152">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-153">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="b2432-153">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="b2432-154">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="b2432-154">The operation failed because the engine cannot allocate the resources that are required to open a new cursor.</span></span> <span data-ttu-id="b2432-155">Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="b2432-155">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-156">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="b2432-156">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="b2432-157">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour créer une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-157">The operation failed because the engine cannot allocate the resources that are required to create a temporary table.</span></span> <span data-ttu-id="b2432-158">Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b2432-158">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-159">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="b2432-159">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="b2432-160"><strong>JetOpenTemporaryTable</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="b2432-160"><strong>JetOpenTemporaryTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table that was specified could not be created using the forward-only optimization.</span></span></p>
<p><span data-ttu-id="b2432-161"><strong>Windows Server 2003 :</strong>  Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b2432-161"><strong>Windows Server 2003:</strong>  This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-162">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="b2432-162">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="b2432-163">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b2432-163">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="b2432-164">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="b2432-164">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-165">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="b2432-165">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="b2432-166">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache le schéma de la table.</span><span class="sxs-lookup"><span data-stu-id="b2432-166">The operation failed because the engine cannot allocate the resources that are required to cache the schema of the table.</span></span> <span data-ttu-id="b2432-167">Pour configurer le nombre de tables qui ont des schémas pouvant être mis en cache, utilisez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b2432-167">To configure the number of tables that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-168">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="b2432-168">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="b2432-169">Le membre <strong>CP</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="b2432-169">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="b2432-170">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="b2432-170">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="b2432-171">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="b2432-171">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-172">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="b2432-172">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="b2432-173">Le membre <strong>coltyp</strong> de l' <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="b2432-173">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-174">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="b2432-174">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="b2432-175">Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b2432-175">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="b2432-176">L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</span><span class="sxs-lookup"><span data-stu-id="b2432-176">The locale ID might be either completely invalid or the associated language pack might not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-177">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="b2432-177">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="b2432-178">Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b2432-178">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span></p>
<p><span data-ttu-id="b2432-179"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b2432-179"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p>
<p><span data-ttu-id="b2432-180"><strong>Windows 2000 :</strong>  Sur Windows 2000, les indicateurs de normalisation non valides entraînent JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="b2432-180"><strong>Windows 2000:</strong>  On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-181">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="b2432-181">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="b2432-182">Impossible de créer l’index, car une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b2432-182">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="b2432-183"><strong>JetOpenTemporaryTable</strong> renvoie cette erreur dans les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2432-183"><strong>JetOpenTemporaryTable</strong> will return this error under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2432-184">Les paramètres régionaux de langue neutre sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b2432-184">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="b2432-185">Un ensemble non valide d’indicateurs de normalisation est spécifié.</span><span class="sxs-lookup"><span data-stu-id="b2432-185">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="b2432-186"><strong>Windows 2000 :</strong>  Cette erreur est renvoyée uniquement par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b2432-186"><strong>Windows 2000:</strong>  This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-187">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="b2432-187">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="b2432-188">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache les index de la table.</span><span class="sxs-lookup"><span data-stu-id="b2432-188">The operation failed because the engine cannot allocate the resources that are required to cache the indexes of the table.</span></span> <span data-ttu-id="b2432-189">Pour configurer le nombre d’index qui ont des schémas pouvant être mis en cache, utilisez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b2432-189">To configure the number of indexes that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b2432-190">En cas de réussite, un curseur ouvert sur la table temporaire nouvellement créée est retourné.</span><span class="sxs-lookup"><span data-stu-id="b2432-190">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="b2432-191">L’état de la base de données temporaire sera préparé à contenir la nouvelle table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-191">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="b2432-192">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="b2432-192">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="b2432-193">En cas d’échec, la table temporaire n’est pas créée et un curseur n’est pas renvoyé.</span><span class="sxs-lookup"><span data-stu-id="b2432-193">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="b2432-194">L’état de la base de données temporaire peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="b2432-194">The state of the temporary database can be changed.</span></span> <span data-ttu-id="b2432-195">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="b2432-195">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b2432-196">Notes</span><span class="sxs-lookup"><span data-stu-id="b2432-196">Remarks</span></span>

<span data-ttu-id="b2432-197">Les tables temporaires ne prennent pas en charge le complément complet des options de définition de colonne généralement prises en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="b2432-197">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="b2432-198">En fait, seuls les JET_bitColumnFixed et les JET_bitColumnTagged sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2432-198">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="b2432-199">Cela signifie qu’il n’est pas possible de créer une colonne à incrémentation automatique, une version ou une colonne à plusieurs valeurs dans une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-199">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="b2432-200">Enfin, les colonnes de mise à jour de tiers de confiance ne sont pas prises en charge, car elles ne peuvent être utilisées que par une seule session à la fois.</span><span class="sxs-lookup"><span data-stu-id="b2432-200">Finally, escrow update columns are not supported because they can only be used by one session at a time.</span></span> <span data-ttu-id="b2432-201">Si l’une de ces options est demandée, elles seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="b2432-201">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="b2432-202">Les tables temporaires ne prennent pas en charge les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="b2432-202">Temporary tables do not support default values.</span></span> <span data-ttu-id="b2432-203">Si une définition de colonne est fournie et contient une spécification de valeur par défaut, cette spécification sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="b2432-203">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="b2432-204">Les tables temporaires sont retournées à l’appelant à la suite de nombreuses fonctions ESE différentes.</span><span class="sxs-lookup"><span data-stu-id="b2432-204">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="b2432-205">Par exemple, [JetGetIndexInfo](./jetgetindexinfo-function.md) avec le groupe d’options JET_IdxInfo retourne une table temporaire contenant une liste de toutes les colonnes clés d’un index donné.</span><span class="sxs-lookup"><span data-stu-id="b2432-205">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="b2432-206">Les tables temporaires suivent les mêmes règles de cycle de vie que les tables temporaires ordinaires, comme décrit ici.</span><span class="sxs-lookup"><span data-stu-id="b2432-206">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="b2432-207">Les tables temporaires sont également utilisées en interne par le moteur de base de données pour de nombreuses tâches.</span><span class="sxs-lookup"><span data-stu-id="b2432-207">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="b2432-208">La plus importante de ces tâches est la création d’un index sur une table existante.</span><span class="sxs-lookup"><span data-stu-id="b2432-208">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="b2432-209">Une table temporaire sera utilisée pour trier les clés d’index utilisées pour construire cet index.</span><span class="sxs-lookup"><span data-stu-id="b2432-209">A temporary table will be used to sort the index keys that are used to construct that index.</span></span>

<span data-ttu-id="b2432-210">Toutes les tables temporaires sont stockées dans la base de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-210">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="b2432-211">La base de données temporaire est un fichier de base de données spécial qui est conservé pendant la durée de vie d’une instance ESE et qui est supprimé lorsque cette instance est arrêtée ou redémarrée.</span><span class="sxs-lookup"><span data-stu-id="b2432-211">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="b2432-212">L’emplacement de la base de données temporaire peut être configuré à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b2432-212">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="b2432-213">Le placement de la base de données temporaire sur le disque par rapport à vos fichiers journaux de transactions et vos fichiers de base de données peut être important si votre application utilise intensivement des tables temporaires ou crée fréquemment des index.</span><span class="sxs-lookup"><span data-stu-id="b2432-213">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="b2432-214">Le cycle de vie d’une table temporaire est lié aux curseurs qui la référencent.</span><span class="sxs-lookup"><span data-stu-id="b2432-214">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="b2432-215">Si tous les curseurs qui font référence à une table temporaire sont fermés, de manière implicite ou explicite, la table temporaire est supprimée.</span><span class="sxs-lookup"><span data-stu-id="b2432-215">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="b2432-216">Si une table temporaire est créée à l’intérieur d’une transaction et que la transaction est ensuite restaurée, la table temporaire est supprimée, car tous les curseurs qui y font référence sont implicitement fermés.</span><span class="sxs-lookup"><span data-stu-id="b2432-216">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="b2432-217">Les nouveaux curseurs peuvent référencer une table temporaire uniquement par le biais de l’utilisation de [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="b2432-217">New cursors can reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="b2432-218">Dans ce cas, les nouveaux curseurs sont positionnés sur la première entrée d’index de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-218">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="b2432-219">[JetDupCursor](./jetdupcursor-function.md) ne fonctionnera que pendant certaines phases d’utilisation de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-219">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="b2432-220">Pour plus d’informations, consultez les notes relatives aux fonctionnalités de curseur de table temporaires.</span><span class="sxs-lookup"><span data-stu-id="b2432-220">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="b2432-221">Il n’est pas possible de référencer une table temporaire à partir de plusieurs sessions à la fois.</span><span class="sxs-lookup"><span data-stu-id="b2432-221">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="b2432-222">**Attention**  Il existe un problème important dans [JetDupCursor](./jetdupcursor-function.md) qui affecte les tables temporaires.</span><span class="sxs-lookup"><span data-stu-id="b2432-222">**Caution**  There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="b2432-223">Si une tentative est faite pour dupliquer une table temporaire en mode avant uniquement, le curseur résultant ne sera pas créé correctement et fonctionnera correctement.</span><span class="sxs-lookup"><span data-stu-id="b2432-223">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="b2432-224">Il est toujours possible de dupliquer un curseur sur une table temporaire matérialisée.</span><span class="sxs-lookup"><span data-stu-id="b2432-224">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="b2432-225">Le gestionnaire de tables temporaire peut implémenter une table temporaire de trois manières.</span><span class="sxs-lookup"><span data-stu-id="b2432-225">The temporary table manager can implement a temporary table in three ways.</span></span> <span data-ttu-id="b2432-226">La première méthode consiste à conserver une table en mémoire.</span><span class="sxs-lookup"><span data-stu-id="b2432-226">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="b2432-227">Cette stratégie est la plus rapide, mais elle ne peut être utilisée que pour les tables temporaires, simples et de petite taille.</span><span class="sxs-lookup"><span data-stu-id="b2432-227">This strategy is the fastest but can only be used for small, simple, temporary tables.</span></span> <span data-ttu-id="b2432-228">La deuxième méthode consiste à créer un tri sur disque qui peut être piloté à l’aide d’un itérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="b2432-228">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="b2432-229">Cette stratégie ne peut être utilisée que dans certaines circonstances et est le moyen le plus rapide pour trier et supprimer les doublons d’un jeu de données très volumineux.</span><span class="sxs-lookup"><span data-stu-id="b2432-229">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="b2432-230">La troisième méthode consiste à créer une arborescence B + dans la base de données temporaire pour contenir la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-230">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="b2432-231">Cette stratégie est la plus lente, mais la plus polyvalente, appelée « table temporaire matérialisée ».</span><span class="sxs-lookup"><span data-stu-id="b2432-231">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="b2432-232">Ces stratégies peuvent être utilisées en association pour obtenir les fonctionnalités demandées par la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-232">These strategies can be used in combination to ultimately achieve the functionality that is requested of the temporary table.</span></span>

<span data-ttu-id="b2432-233">Lorsque la table temporaire n’est pas matérialisée, elle est principalement utilisée en deux phases principales.</span><span class="sxs-lookup"><span data-stu-id="b2432-233">When the temporary table is not materialized then it is used primarily in two major phases.</span></span> <span data-ttu-id="b2432-234">La première phase correspond à la phase d’insertion où la table est remplie avec son jeu de données initial.</span><span class="sxs-lookup"><span data-stu-id="b2432-234">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="b2432-235">Pendant cette phase, seule l’insertion de données est autorisée.</span><span class="sxs-lookup"><span data-stu-id="b2432-235">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="b2432-236">Cette phase se termine lorsqu’une tentative est effectuée pour déplacer le curseur à l’aide de [JetMove](./jetmove-function.md) ou [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="b2432-236">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="b2432-237">La deuxième phase est la phase d’extraction des données.</span><span class="sxs-lookup"><span data-stu-id="b2432-237">The second phase is the data extraction phase.</span></span> <span data-ttu-id="b2432-238">Au cours de cette phase, les données stockées dans la table temporaire peuvent être extraites en fonction des fonctionnalités qui ont été demandées lors de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="b2432-238">During this phase, the data that is stored in the temporary table can be extracted according to the capabilities that were requested when the temporary table was created.</span></span>

<span data-ttu-id="b2432-239">**Fonctionnalités de curseur de table temporaires**</span><span class="sxs-lookup"><span data-stu-id="b2432-239">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="b2432-240">Lorsque la table temporaire est matérialisée, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :</span><span class="sxs-lookup"><span data-stu-id="b2432-240">When the temporary table is materialized, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="b2432-241">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b2432-241">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b2432-242">JetDelete</span><span class="sxs-lookup"><span data-stu-id="b2432-242">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="b2432-243">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b2432-243">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="b2432-244">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="b2432-244">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="b2432-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="b2432-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="b2432-246">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="b2432-246">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="b2432-247">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="b2432-247">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="b2432-248">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="b2432-248">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="b2432-249">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="b2432-249">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="b2432-250">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="b2432-250">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="b2432-251">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="b2432-251">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="b2432-252">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b2432-252">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b2432-253">JetMove</span><span class="sxs-lookup"><span data-stu-id="b2432-253">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="b2432-254">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="b2432-254">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="b2432-255">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b2432-255">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="b2432-256">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="b2432-256">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="b2432-257">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b2432-257">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b2432-258">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b2432-258">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="b2432-259">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b2432-259">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="b2432-260">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="b2432-260">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="b2432-261">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b2432-261">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="b2432-262">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b2432-262">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="b2432-263">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="b2432-263">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="b2432-264">Lorsque la table temporaire n’est pas matérialisée et qu’elle est dans la phase d’insertion, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :</span><span class="sxs-lookup"><span data-stu-id="b2432-264">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="b2432-265">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b2432-265">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b2432-266">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="b2432-266">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="b2432-267">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b2432-267">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b2432-268">JetMove</span><span class="sxs-lookup"><span data-stu-id="b2432-268">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="b2432-269">**Remarque**  Provoque la transition vers la phase d’extraction.</span><span class="sxs-lookup"><span data-stu-id="b2432-269">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="b2432-270">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="b2432-270">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="b2432-271">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b2432-271">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b2432-272">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b2432-272">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="b2432-273">**Remarque**  Provoque la transition vers la phase d’extraction.</span><span class="sxs-lookup"><span data-stu-id="b2432-273">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="b2432-274">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b2432-274">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="b2432-275">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="b2432-275">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="b2432-276">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="b2432-276">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="b2432-277">Lorsque la table temporaire n’est pas matérialisée et qu’elle est dans la phase d’extraction, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :</span><span class="sxs-lookup"><span data-stu-id="b2432-277">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="b2432-278">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b2432-278">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b2432-279">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b2432-279">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="b2432-280">**Remarque**  Si une tentative est faite pour dupliquer une table temporaire en mode avant uniquement, le curseur résultant ne sera pas créé correctement et fonctionnera correctement.</span><span class="sxs-lookup"><span data-stu-id="b2432-280">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="b2432-281">Il est toujours possible de dupliquer un curseur sur une table temporaire matérialisée.</span><span class="sxs-lookup"><span data-stu-id="b2432-281">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="b2432-282">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="b2432-282">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="b2432-283">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="b2432-283">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="b2432-284">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="b2432-284">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="b2432-285">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="b2432-285">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="b2432-286">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="b2432-286">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="b2432-287">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="b2432-287">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="b2432-288">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b2432-288">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b2432-289">JetMove</span><span class="sxs-lookup"><span data-stu-id="b2432-289">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="b2432-290">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b2432-290">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="b2432-291">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="b2432-291">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="b2432-292">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b2432-292">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b2432-293">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b2432-293">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="b2432-294">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b2432-294">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="b2432-295">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b2432-295">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="b2432-296">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2432-296">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2432-297"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b2432-297"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b2432-298">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2432-298">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-299"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b2432-299"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b2432-300">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b2432-300">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-301"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b2432-301"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b2432-302">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b2432-302">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2432-303"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="b2432-303"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b2432-304">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b2432-304">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2432-305"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b2432-305"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b2432-306">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b2432-306">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b2432-307">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2432-307">See Also</span></span>

[<span data-ttu-id="b2432-308">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b2432-308">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b2432-309">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b2432-309">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b2432-310">JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="b2432-310">JET_OPENTEMPORARYTABLE</span></span>](./jet-opentemporarytable-structure.md)  
[<span data-ttu-id="b2432-311">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b2432-311">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="b2432-312">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="b2432-312">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="b2432-313">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b2432-313">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="b2432-314">JetMove</span><span class="sxs-lookup"><span data-stu-id="b2432-314">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="b2432-315">JetRollback</span><span class="sxs-lookup"><span data-stu-id="b2432-315">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="b2432-316">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b2432-316">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="b2432-317">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b2432-317">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="b2432-318">Paramètres d’information</span><span class="sxs-lookup"><span data-stu-id="b2432-318">Informational Parameters</span></span>](./informational-parameters.md)  
[<span data-ttu-id="b2432-319">Paramètres de base de données temporaires</span><span class="sxs-lookup"><span data-stu-id="b2432-319">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
