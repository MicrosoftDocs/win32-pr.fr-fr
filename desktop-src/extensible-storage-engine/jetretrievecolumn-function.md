---
description: 'En savoir plus sur : fonction JetRetrieveColumn'
title: Fonction JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529427"
---
# <a name="jetretrievecolumn-function"></a><span data-ttu-id="d8929-103">Fonction JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="d8929-103">JetRetrieveColumn Function</span></span>


<span data-ttu-id="d8929-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d8929-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumn-function"></a><span data-ttu-id="d8929-105">Fonction JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="d8929-105">JetRetrieveColumn Function</span></span>

<span data-ttu-id="d8929-106">La fonction **JetRetrieveColumn** récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="d8929-106">The **JetRetrieveColumn** function retrieves a single column value from the current record.</span></span> <span data-ttu-id="d8929-107">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="d8929-107">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="d8929-108">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="d8929-108">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="d8929-109">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="d8929-109">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="d8929-110">En plus de récupérer la valeur réelle de la colonne, **JetRetrieveColumn** peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="d8929-110">In addition to retrieving the actual column value, **JetRetrieveColumn** can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="d8929-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8929-111">Parameters</span></span>

<span data-ttu-id="d8929-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d8929-112">*sesid*</span></span>

<span data-ttu-id="d8929-113">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d8929-113">The session to use for this call.</span></span>

<span data-ttu-id="d8929-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d8929-114">*tableid*</span></span>

<span data-ttu-id="d8929-115">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d8929-115">The cursor to use for this call.</span></span>

<span data-ttu-id="d8929-116">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="d8929-116">*columnid*</span></span>

<span data-ttu-id="d8929-117">[JET_COLUMNID](./jet-columnid.md) de la colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d8929-117">The [JET_COLUMNID](./jet-columnid.md) of the column to retrieve.</span></span>

<span data-ttu-id="d8929-118">Une valeur *ColumnID* égale à 0 (zéro) peut être fournie, qui ne fait pas référence à une colonne individuelle.</span><span class="sxs-lookup"><span data-stu-id="d8929-118">A *columnid* value of 0 (zero) can be given which does not itself refer to any individual column.</span></span> <span data-ttu-id="d8929-119">Lorsque la valeur *ColumnID* 0 (zéro) est donnée, toutes les colonnes avec balises, éparses et les colonnes à valeurs multiples sont traitées comme une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-119">When *columnid* 0 (zero) is given, all tagged columns, sparse, and multi-valued columns are treated as a single column.</span></span> <span data-ttu-id="d8929-120">Cela facilite la récupération de toutes les colonnes éparses présentes dans un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d8929-120">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="d8929-121">*pvData*</span><span class="sxs-lookup"><span data-stu-id="d8929-121">*pvData*</span></span>

<span data-ttu-id="d8929-122">Mémoire tampon de sortie qui reçoit la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-122">The output buffer that receives the column value.</span></span>

<span data-ttu-id="d8929-123">*cbData*</span><span class="sxs-lookup"><span data-stu-id="d8929-123">*cbData*</span></span>

<span data-ttu-id="d8929-124">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="d8929-124">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="d8929-125">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="d8929-125">*pcbActual*</span></span>

<span data-ttu-id="d8929-126">Reçoit la taille réelle, en octets, de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-126">Receives the actual size, in bytes, of the column value.</span></span>

<span data-ttu-id="d8929-127">Si ce paramètre a la valeur **null**, la taille réelle de la valeur de colonne ne sera pas retournée.</span><span class="sxs-lookup"><span data-stu-id="d8929-127">If this parameter is **NULL**, then the actual size of the column value will not be returned.</span></span>

<span data-ttu-id="d8929-128">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d8929-128">*grbit*</span></span>

<span data-ttu-id="d8929-129">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8929-129">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8929-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8929-130">Value</span></span></p></th>
<th><p><span data-ttu-id="d8929-131">Signification</span><span class="sxs-lookup"><span data-stu-id="d8929-131">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8929-132">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="d8929-132">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="d8929-133">Cet indicateur force la récupération de la colonne à récupérer la valeur modifiée au lieu de la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="d8929-133">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="d8929-134">Si la valeur n’a pas été modifiée, la valeur d’origine est récupérée.</span><span class="sxs-lookup"><span data-stu-id="d8929-134">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="d8929-135">De cette façon, une valeur qui n’a pas encore été insérée ou mise à jour peut être récupérée pendant l’opération d’insertion ou de mise à jour d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d8929-135">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-136">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="d8929-136">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="d8929-137">Cette option permet de récupérer des valeurs de colonne à partir de l’index, si possible, sans accéder à l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d8929-137">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="d8929-138">De cette façon, le chargement inutile d’enregistrements peut être évité lorsque les données nécessaires sont disponibles à partir d’entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="d8929-138">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="d8929-139">Dans les cas où la valeur de colonne d’origine ne peut pas être récupérée à partir de l’index, en raison des transformations irréversibles ou de la troncation des données, l’enregistrement est accessible et les données sont récupérées comme normales.</span><span class="sxs-lookup"><span data-stu-id="d8929-139">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="d8929-140">Il s’agit d’une option de performance qui doit être spécifiée uniquement lorsqu’il est probable que la valeur de colonne puisse être récupérée à partir de l’index.</span><span class="sxs-lookup"><span data-stu-id="d8929-140">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="d8929-141">Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster, étant donné que les entrées d’index de l’index cluster ou principal sont les enregistrements eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="d8929-141">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="d8929-142">Ce bit ne peut pas être défini si JET_bitRetrieveFromPrimaryBookmark est également défini.</span><span class="sxs-lookup"><span data-stu-id="d8929-142">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-143">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="d8929-143">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="d8929-144">Cette option est utilisée pour extraire des valeurs de colonne du signet d’index et peut différer de la valeur d’index lorsqu’une colonne apparaît à la fois dans l’index primaire et dans l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="d8929-144">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="d8929-145">Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster ou principal.</span><span class="sxs-lookup"><span data-stu-id="d8929-145">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="d8929-146">Ce bit ne peut pas être défini si JET_bitRetrieveFromIndex est également défini.</span><span class="sxs-lookup"><span data-stu-id="d8929-146">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-147">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="d8929-147">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="d8929-148">Cette option permet de récupérer le numéro de séquence d’une valeur de colonne à valeurs multiples dans pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="d8929-148">This option is used to retrieve the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="d8929-149">Le champ itagSequence est généralement une entrée permettant de récupérer des valeurs de colonnes à valeurs multiples à partir d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d8929-149">The itagSequence field is commonly an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="d8929-150">Toutefois, lorsque vous récupérez des valeurs à partir d’un index, il est également possible d’associer l’entrée d’index à un numéro de séquence particulier et de récupérer également ce numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="d8929-150">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="d8929-151">La récupération du numéro de séquence peut être une opération coûteuse et ne doit être effectuée que si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d8929-151">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-152">JET_bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="d8929-152">JET_bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="d8929-153">Cette option permet de récupérer des valeurs <strong>null</strong> de colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d8929-153">This option is used to retrieve multi-valued column <strong>NULL</strong> values.</span></span> <span data-ttu-id="d8929-154">Si cette option n’est pas spécifiée, les valeurs <strong>null</strong> de la colonne à valeurs multiples sont automatiquement ignorées.</span><span class="sxs-lookup"><span data-stu-id="d8929-154">If this option is not specified, multi-valued column <strong>NULL</strong> values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-155">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="d8929-155">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="d8929-156">Cette option affecte uniquement les colonnes à valeurs multiples et entraîne le renvoi d’une valeur <strong>null</strong> lorsque le numéro de séquence demandé est 1 et qu’il n’existe aucune valeur définie pour la colonne dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d8929-156">This option affects only multi-valued columns and causes a <strong>NULL</strong> value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-157">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="d8929-157">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="d8929-158">Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="d8929-158">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-159">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="d8929-159">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="d8929-160">Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="d8929-160">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-161">JET_bitRetrieveTuple</span><span class="sxs-lookup"><span data-stu-id="d8929-161">JET_bitRetrieveTuple</span></span></p></td>
<td><p><span data-ttu-id="d8929-162">Cet indicateur permet la récupération d’un segment de tuple de l’index.</span><span class="sxs-lookup"><span data-stu-id="d8929-162">This flag will allow the retrieval of a tuple segment of the index.</span></span> <span data-ttu-id="d8929-163">Ce bit doit être spécifié avec JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="d8929-163">This bit must be specified with JET_bitRetrieveFromIndex.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8929-164">*pretinfo*</span><span class="sxs-lookup"><span data-stu-id="d8929-164">*pretinfo*</span></span>

<span data-ttu-id="d8929-165">Si *pretinfo* a la **valeur null** , la fonction se comporte comme si un *ItagSequence* de 1 et un *ibLongValue* de 0 (zéro) ont été donnés.</span><span class="sxs-lookup"><span data-stu-id="d8929-165">If *pretinfo* is give as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="d8929-166">Ainsi, la récupération de colonne récupère la première valeur d’une colonne à valeurs multiples et récupère les données de type long à l’offset 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d8929-166">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

<span data-ttu-id="d8929-167">Ce paramètre est utilisé pour fournir un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8929-167">This parameter is used to provide one or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8929-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8929-168">Value</span></span></p></th>
<th><p><span data-ttu-id="d8929-169">Signification</span><span class="sxs-lookup"><span data-stu-id="d8929-169">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8929-170">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="d8929-170">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="d8929-171">Donne un décalage binaire dans une valeur de colonne longue lors de l’extraction d’une partie d’une valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-171">Gives a binary offset into a long column value when retrieving a portion of a column value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-172">itagSequence</span><span class="sxs-lookup"><span data-stu-id="d8929-172">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="d8929-173">Indique le numéro de séquence de la valeur de colonne à valeurs multiples souhaitée.</span><span class="sxs-lookup"><span data-stu-id="d8929-173">Gives the sequence number of the desired multi-valued column value.</span></span> <span data-ttu-id="d8929-174">Notez que ce champ est défini uniquement si le JET_bitRetrieveTag est spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8929-174">Note that this field is only set if the JET_bitRetrieveTag is specified.</span></span> <span data-ttu-id="d8929-175">Dans le cas contraire, il n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="d8929-175">Otherwise, it is unmodified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-176">columnidNextTagged</span><span class="sxs-lookup"><span data-stu-id="d8929-176">columnidNextTagged</span></span></p></td>
<td><p><span data-ttu-id="d8929-177">Retourne l’ID de colonne de la valeur de colonne retournée lors de l’extraction de toutes les colonnes balisées, éparses et à valeurs multiples à l’aide du passage de <em>ColumnID</em> égal à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d8929-177">Returns the column ID of the returned column value when retrieving all tagged, sparse and multi-valued, columns using passing <em>columnid</em> of 0 (zero).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d8929-178">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d8929-178">Return Value</span></span>

<span data-ttu-id="d8929-179">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="d8929-179">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d8929-180">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d8929-180">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8929-181">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d8929-181">Return code</span></span></p></th>
<th><p><span data-ttu-id="d8929-182">Description</span><span class="sxs-lookup"><span data-stu-id="d8929-182">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8929-183">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d8929-183">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d8929-184">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d8929-184">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-185">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="d8929-185">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="d8929-186">L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-186">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-187">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="d8929-187">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="d8929-188">Une valeur de numéro de séquence de colonne à valeurs multiples non valide a été transmise dans pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="d8929-188">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="d8929-189">Les valeurs valides pour les numéros de séquence de valeur de colonne à valeurs multiples sont égales ou supérieures à 1.</span><span class="sxs-lookup"><span data-stu-id="d8929-189">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="d8929-190">La valeur 0 (zéro) n’est pas valide pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d8929-190">A value of 0 (zero) is invalid for this function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d8929-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d8929-192">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d8929-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-193">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="d8929-193">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="d8929-194">La colonne décrite par le <em>ColumnID</em> donné n’existe pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="d8929-194">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-195">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="d8929-195">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="d8929-196">Les colonnes indexées en tant que sous-chaînes ne peuvent pas être récupérées à partir de l’index, car seule une petite partie de la colonne est généralement présente dans chaque entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="d8929-196">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-197">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d8929-197">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d8929-198">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="d8929-198">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="d8929-199">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d8929-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-200">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="d8929-200">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="d8929-201">Dans certains cas, la mémoire tampon donnée pour la colonne de récupération doit être suffisamment dimensionnée pour pouvoir retourner n’importe quel volume de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-201">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="d8929-202">Par exemple, les colonnes pouvant être mises à jour par tiers de confiance sont ajustées pour être cohérentes pour le contexte transactionnel de la session appelante et cet ajustement requiert la mémoire tampon fournie par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d8929-202">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="d8929-203">Si un espace de mémoire tampon insuffisant est fourni, JET_errInvalidBufferSize est retourné et aucune donnée de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="d8929-203">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-204">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d8929-204">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d8929-205">Un ou plusieurs des paramètres spécifiés sont incorrects.</span><span class="sxs-lookup"><span data-stu-id="d8929-205">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="d8929-206">Cela peut se produire si retinfo. cbStruct est plus petit que la taille de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="d8929-206">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-207">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="d8929-207">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="d8929-208">Les options fournies sont inconnues ou une combinaison non conforme de paramètres de bits connus.</span><span class="sxs-lookup"><span data-stu-id="d8929-208">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-209">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d8929-209">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d8929-210">Le curseur n’est pas positionné sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d8929-210">The cursor is not positioned on a record.</span></span> <span data-ttu-id="d8929-211">Cela peut se produire pour de nombreuses raisons différentes.</span><span class="sxs-lookup"><span data-stu-id="d8929-211">This can happen for many different reasons.</span></span> <span data-ttu-id="d8929-212">Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="d8929-212">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-213">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d8929-213">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d8929-214">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="d8929-214">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-215">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d8929-215">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d8929-216">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="d8929-216">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-217">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d8929-217">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d8929-218">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="d8929-218">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d8929-219"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d8929-219"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-220">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d8929-220">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d8929-221">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="d8929-221">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-222">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="d8929-222">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="d8929-223">Impossible de récupérer la valeur de colonne entière, car la taille de la mémoire tampon donnée est inférieure à celle de la colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-223">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-224">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="d8929-224">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="d8929-225">La valeur de colonne Récupérée est <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8929-225">The column value retrieved is <strong>NULL</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8929-226">En cas de réussite, la valeur de colonne pour la colonne donnée, est copiée dans la mémoire tampon donnée.</span><span class="sxs-lookup"><span data-stu-id="d8929-226">On success, the column value for the given column, is copied into the given buffer.</span></span> <span data-ttu-id="d8929-227">Une valeur inférieure à toute la valeur de la colonne est copiée avec l’avertissement JET_wrnBufferTruncated est retourné.</span><span class="sxs-lookup"><span data-stu-id="d8929-227">Less than all of the column value is copied with the warning JET_wrnBufferTruncated is returned.</span></span> <span data-ttu-id="d8929-228">Si le *pcbActual* a été donné, la taille réelle de la valeur de colonne est retournée.</span><span class="sxs-lookup"><span data-stu-id="d8929-228">If the *pcbActual* was given, the actual size of the column value is returned.</span></span> <span data-ttu-id="d8929-229">Notez que les valeurs **null** ont une longueur de 0 (zéro) et, par conséquent, attribuez à la taille retournée la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d8929-229">Note that **NULL** values have 0 (zero) length and will thus set the returned size to 0 (zero).</span></span> <span data-ttu-id="d8929-230">Si la colonne Récupérée était une colonne à valeurs multiples et que la valeur de *pretinfo* a été spécifiée, et que JET_bitReturnTag a été défini en tant qu’option, le numéro de séquence de la valeur de colonne est retourné dans pretinfo- \> itagSequence.</span><span class="sxs-lookup"><span data-stu-id="d8929-230">If the column retrieved was a multi-valued column, and *pretinfo* was given, and JET_bitReturnTag was set as an option, then the sequence number of the column value is returned in pretinfo-\>itagSequence.</span></span>

<span data-ttu-id="d8929-231">En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée n’est copiée dans la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="d8929-231">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d8929-232">Notes</span><span class="sxs-lookup"><span data-stu-id="d8929-232">Remarks</span></span>

<span data-ttu-id="d8929-233">Cet appel est utilisé une seule fois pour récupérer des données de taille fixe ou connue pour des colonnes qui ne sont pas à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d8929-233">This call is used just once to retrieve data of fixed or known size for non-multi-valued columns.</span></span> <span data-ttu-id="d8929-234">Toutefois, lorsque les données de la colonne ont une taille inconnue, cet appel est généralement utilisé deux fois.</span><span class="sxs-lookup"><span data-stu-id="d8929-234">However, when column data is of unknown size, this call is typically used twice.</span></span> <span data-ttu-id="d8929-235">Elle est appelée en premier pour déterminer la taille des données afin de pouvoir allouer l’espace de stockage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d8929-235">It is called first to determine the size of the data so it can allocate the necessary storage space.</span></span> <span data-ttu-id="d8929-236">Le même appel est ensuite refait pour récupérer les données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="d8929-236">Then, the same call is made again to retrieve the column data.</span></span> <span data-ttu-id="d8929-237">Lorsque le nombre réel de valeurs est inconnu, car une colonne est à valeurs multiples, l’appel est généralement utilisé trois fois.</span><span class="sxs-lookup"><span data-stu-id="d8929-237">When the actual number of values is unknown, because a column is multi-valued, the call is typically used three times.</span></span> <span data-ttu-id="d8929-238">Commencez par obtenir le nombre de valeurs, puis deux fois plus pour allouer le stockage et récupérer les données réelles.</span><span class="sxs-lookup"><span data-stu-id="d8929-238">First to get the number of values and then twice more to allocate storage and retrieve the actual data.</span></span>

<span data-ttu-id="d8929-239">La récupération de toutes les valeurs d’une colonne à valeurs multiples peut être effectuée en appelant à plusieurs reprises cette fonction avec une \> valeur pretinfo-itagSequence à partir de 1 et en accroissant à chaque appel suivant.</span><span class="sxs-lookup"><span data-stu-id="d8929-239">Retrieving all the values for a multi-valued column can be done by repeatedly calling this function with a pretinfo-\>itagSequence value beginning at 1 and increasing on each subsequent call.</span></span> <span data-ttu-id="d8929-240">La dernière valeur de colonne est connue pour être récupérée quand une JET_wrnColumnNull est retournée à partir de la fonction.</span><span class="sxs-lookup"><span data-stu-id="d8929-240">The last column value is known to be retrieved when a JET_wrnColumnNull is returned from the function.</span></span> <span data-ttu-id="d8929-241">Notez que cette méthode ne peut pas être effectuée si la colonne à valeurs multiples contient des valeurs **null** explicites définies dans sa séquence de valeurs, car ces valeurs sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="d8929-241">Note that this method cannot be done if the multi-value column has explicit **NULL** values set in its value sequence, since these values would be skipped.</span></span> <span data-ttu-id="d8929-242">Si une application souhaite récupérer toutes les valeurs de colonne à valeurs multiples, y compris celles qui ont explicitement la valeur **null**, [JetRetrieveColumns](./jetretrievecolumns-function.md) doit être utilisé à la place de **JetRetrieveColumn**.</span><span class="sxs-lookup"><span data-stu-id="d8929-242">If an application desires to retrieve all multi-valued column values, including those explicitly set to **NULL**, then [JetRetrieveColumns](./jetretrievecolumns-function.md) must be used instead of **JetRetrieveColumn**.</span></span> <span data-ttu-id="d8929-243">Notez que cette fonction ne retourne pas le nombre de valeurs pour une fonction à valeurs multiples quand une valeur *itagSequence* égale à 0 (zéro) est donnée.</span><span class="sxs-lookup"><span data-stu-id="d8929-243">Note that this function does not return the number of values for a multi-valued function when an *itagSequence* value of 0 (zero) is given.</span></span> <span data-ttu-id="d8929-244">Seul [JetRetrieveColumns](./jetretrievecolumns-function.md) retourne le nombre de valeurs d’une valeur de colonne lorsqu’une valeur *itagSequence* égale à 0 (zéro) est passée.</span><span class="sxs-lookup"><span data-stu-id="d8929-244">Only [JetRetrieveColumns](./jetretrievecolumns-function.md) will return the number of values of a column value when an *itagSequence* value of 0 (zero) is passed.</span></span>

<span data-ttu-id="d8929-245">Si cette fonction est appelée au niveau de la transaction 0 (zéro), par exemple, la session appelante n’est pas elle-même dans une transaction, puis une transaction est ouverte et fermée dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="d8929-245">If this function is called at transaction level 0 (zero), for example, the calling session is not itself in a transaction, then a transaction is opened and closed within the function.</span></span> <span data-ttu-id="d8929-246">L’objectif est de retourner des résultats cohérents dans le cas où une valeur long s’étend sur des pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="d8929-246">The purpose of this is to return consistent results in the case that a long value spans database pages.</span></span> <span data-ttu-id="d8929-247">Notez que la transaction est libérée entre les appels de fonction et une série d’appels à cette fonction lorsque la session n’est pas dans une transaction peut retourner des données mises à jour après le premier appel à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d8929-247">Note that the transaction is released between function calls and a series of calls to this function when the session is not in a transaction may return data updated after the first call to this function.</span></span>

<span data-ttu-id="d8929-248">La valeur de colonne par défaut est récupérée lorsque la colonne n’a pas été définie explicitement sur une autre valeur, à moins que l’option JET_bitRetrieveIgnoreDefault soit définie.</span><span class="sxs-lookup"><span data-stu-id="d8929-248">The default column value will be retrieved when the column has not been set explicitly to another value, unless the JET_bitRetrieveIgnoreDefault option is set.</span></span>

<span data-ttu-id="d8929-249">La récupération de la valeur de colonne AutoIncrement à partir de la mémoire tampon de copie avant Insert est un moyen courant d’identifier un enregistrement de manière unique pour la liaison lors de l’insertion de données normalisées dans plusieurs tables.</span><span class="sxs-lookup"><span data-stu-id="d8929-249">Retrieving the autoincrement column value from the copy buffer prior to insert is a common means of identifying a record uniquely for linkage when inserting normalized data into multiple tables.</span></span> <span data-ttu-id="d8929-250">La valeur AUTOINCREMENT est allouée lorsque l’opération d’insertion commence et peut être récupérée à partir de la mémoire tampon de copie à tout moment jusqu’à ce que la mise à jour soit terminée.</span><span class="sxs-lookup"><span data-stu-id="d8929-250">The autoincrement value is allocated when the insert operation begins and can be retrieved from the copy buffer at any time until the update is complete.</span></span>

<span data-ttu-id="d8929-251">Lors de la récupération de toutes les colonnes avec balises, à valeurs multiples et éparses, en affectant à *ColumnID* la valeur 0 (zéro), les colonnes sont récupérées dans l’ordre *ColumnID* , de la *plus petite à la plus ancienne* à *ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="d8929-251">When retrieving all tagged, multi-valued, and sparse columns, by setting *columnid* to 0 (zero), columns are retrieved in *columnid* order from lowest *columnid* to highest *columnid*.</span></span> <span data-ttu-id="d8929-252">Le même ordre des valeurs de colonne est retourné chaque fois que les valeurs de colonne sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="d8929-252">The same order of column values is returned each time column values are retrieved.</span></span> <span data-ttu-id="d8929-253">L’ordre est déterministe.</span><span class="sxs-lookup"><span data-stu-id="d8929-253">The order is deterministic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d8929-254">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8929-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8929-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d8929-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d8929-256">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d8929-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-257"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d8929-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d8929-258">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d8929-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-259"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d8929-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d8929-260">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d8929-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8929-261"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="d8929-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d8929-262">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d8929-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8929-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d8929-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d8929-264">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d8929-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d8929-265">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8929-265">See Also</span></span>

[<span data-ttu-id="d8929-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d8929-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d8929-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d8929-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d8929-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d8929-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d8929-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d8929-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d8929-270">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="d8929-270">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="d8929-271">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="d8929-271">JetSetColumn</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="d8929-272">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="d8929-272">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
