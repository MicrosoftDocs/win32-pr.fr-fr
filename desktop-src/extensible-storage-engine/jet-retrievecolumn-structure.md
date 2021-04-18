---
description: 'En savoir plus sur : structure JET_RETRIEVECOLUMN'
title: Structure JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519346"
---
# <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="6dd61-103">Structure JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6dd61-103">JET_RETRIEVECOLUMN Structure</span></span>


<span data-ttu-id="6dd61-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6dd61-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="6dd61-105">Structure JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6dd61-105">JET_RETRIEVECOLUMN Structure</span></span>

<span data-ttu-id="6dd61-106">La structure **JET_RETRIEVECOLUMN** contient des paramètres d’entrée et de sortie pour [JetRetrieveColumns](./jetretrievecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="6dd61-106">The **JET_RETRIEVECOLUMN** structure contains input and output parameters for [JetRetrieveColumns](./jetretrievecolumns-function.md).</span></span> <span data-ttu-id="6dd61-107">Les champs de la structure décrivent la valeur de colonne à récupérer, la méthode de récupération et l’emplacement d’enregistrement des résultats.</span><span class="sxs-lookup"><span data-stu-id="6dd61-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a><span data-ttu-id="6dd61-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6dd61-108">Members</span></span>

<span data-ttu-id="6dd61-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="6dd61-109">**columnid**</span></span>

<span data-ttu-id="6dd61-110">Identificateur de colonne pour la colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6dd61-110">The column identifier for the column to retrieve.</span></span>

<span data-ttu-id="6dd61-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="6dd61-111">**pvData**</span></span>

<span data-ttu-id="6dd61-112">Pointeur pour commencer à stocker des données récupérées à partir de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="6dd61-112">A pointer to begin storing data that is retrieved from the column value.</span></span>

<span data-ttu-id="6dd61-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="6dd61-113">**cbData**</span></span>

<span data-ttu-id="6dd61-114">Taille de l’allocation en commençant à **pvData**, en octets.</span><span class="sxs-lookup"><span data-stu-id="6dd61-114">The size of allocation beginning at **pvData**, in bytes.</span></span> <span data-ttu-id="6dd61-115">L’opération de récupération de colonne ne stocke pas plus de données sur **pvData** que **cbData**.</span><span class="sxs-lookup"><span data-stu-id="6dd61-115">The retrieve column operation will not store more data at **pvData** than **cbData**.</span></span>

<span data-ttu-id="6dd61-116">**cbActual**</span><span class="sxs-lookup"><span data-stu-id="6dd61-116">**cbActual**</span></span>

<span data-ttu-id="6dd61-117">Taille, en octets, des données récupérées par une opération de récupération de colonne.</span><span class="sxs-lookup"><span data-stu-id="6dd61-117">The size, in bytes, of data that is retrieved by a retrieve column operation.</span></span>

<span data-ttu-id="6dd61-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="6dd61-118">**grbit**</span></span>

<span data-ttu-id="6dd61-119">Groupe de bits qui contient les options de récupération de colonne, qui incluent zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6dd61-119">A group of bits that contain the options for column retrieval, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6dd61-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dd61-120">Value</span></span></p></th>
<th><p><span data-ttu-id="6dd61-121">Signification</span><span class="sxs-lookup"><span data-stu-id="6dd61-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dd61-122">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="6dd61-122">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="6dd61-123">Récupère la valeur modifiée au lieu de la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="6dd61-123">Retrieves the modified value instead of the original value.</span></span> <span data-ttu-id="6dd61-124">Si la valeur n’a pas été modifiée, la valeur d’origine est récupérée.</span><span class="sxs-lookup"><span data-stu-id="6dd61-124">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="6dd61-125">De cette façon, une valeur qui n’a pas encore été insérée ou mise à jour peut être récupérée lorsqu’un enregistrement est inséré ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6dd61-125">In this way, a value that has not yet been inserted or updated can be retrieved when a record is inserted or updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd61-126">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="6dd61-126">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="6dd61-127">Récupère les valeurs de colonne de l’index sans accéder à l’enregistrement, si possible.</span><span class="sxs-lookup"><span data-stu-id="6dd61-127">Retrieves column values from the index without accessing the record, if possible.</span></span> <span data-ttu-id="6dd61-128">De cette façon, le chargement inutile d’enregistrements peut être évité lorsque les données nécessaires sont disponibles à partir d’entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="6dd61-128">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="6dd61-129">Dans les cas où la valeur de colonne d’origine ne peut pas être récupérée à partir de l’index, en raison des transformations irréversibles ou de la troncation des données, l’enregistrement est accessible et les données sont récupérées comme normales.</span><span class="sxs-lookup"><span data-stu-id="6dd61-129">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="6dd61-130">Il s’agit d’une option de performance qui doit être spécifiée uniquement lorsqu’il est probable que la valeur de colonne puisse être récupérée à partir de l’index.</span><span class="sxs-lookup"><span data-stu-id="6dd61-130">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="6dd61-131">Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster, étant donné que les entrées d’index de l’index cluster ou principal sont les enregistrements eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="6dd61-131">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="6dd61-132">Ce bit ne peut pas être défini si JET_bitRetrieveFromPrimaryBookmark est également défini.</span><span class="sxs-lookup"><span data-stu-id="6dd61-132">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dd61-133">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="6dd61-133">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="6dd61-134">Récupère les valeurs de colonne du signet d’index et peut différer de la valeur d’index lorsqu’une colonne apparaît à la fois dans l’index primaire et dans l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="6dd61-134">Retrieves column values from the index bookmark, and can differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="6dd61-135">Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster ou principal.</span><span class="sxs-lookup"><span data-stu-id="6dd61-135">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="6dd61-136">Ce bit ne peut pas être défini si JET_bitRetrieveFromIndex est également défini.</span><span class="sxs-lookup"><span data-stu-id="6dd61-136">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd61-137">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="6dd61-137">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="6dd61-138">Récupère le numéro de séquence d’une valeur de colonne à valeurs multiples dans pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="6dd61-138">Retrieves the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="6dd61-139">Le champ itagSequence est souvent utilisé pour récupérer des valeurs de colonnes à valeurs multiples à partir d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6dd61-139">The itagSequence field is often used an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="6dd61-140">Toutefois, lorsque vous récupérez des valeurs à partir d’un index, il est également possible d’associer l’entrée d’index à un numéro de séquence particulier et de récupérer également ce numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="6dd61-140">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="6dd61-141">La récupération du numéro de séquence peut être une opération coûteuse et ne doit être effectuée que si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6dd61-141">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dd61-142">JET_ bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="6dd61-142">JET_ bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="6dd61-143">Récupère des valeurs NULL de colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="6dd61-143">Retrieves multi-valued column NULL values.</span></span> <span data-ttu-id="6dd61-144">Si cette option n’est pas spécifiée, les valeurs NULL de la colonne à valeurs multiples sont automatiquement ignorées.</span><span class="sxs-lookup"><span data-stu-id="6dd61-144">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd61-145">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="6dd61-145">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="6dd61-146">Entraîne le renvoi d’une valeur NULL lorsque le numéro de séquence demandé est 1 et qu’il n’y a aucune valeur définie pour la colonne dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6dd61-146">Causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span> <span data-ttu-id="6dd61-147">Cette option affecte uniquement les colonnes à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="6dd61-147">This option affects only multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dd61-148">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="6dd61-148">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="6dd61-149">Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="6dd61-149">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd61-150">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="6dd61-150">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="6dd61-151">Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="6dd61-151">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dd61-152">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="6dd61-152">**ibLongValue**</span></span>

<span data-ttu-id="6dd61-153">Offset au premier octet à récupérer d’une colonne de type [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="6dd61-153">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="6dd61-154">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="6dd61-154">**itagSequence**</span></span>

<span data-ttu-id="6dd61-155">Numéro de séquence des valeurs contenues dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="6dd61-155">The sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="6dd61-156">**itagSequence** ici dans le **JET_RETRIEVECOLUMN** peut avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="6dd61-156">**itagSequence** here in the **JET_RETRIEVECOLUMN** can be 0.</span></span> <span data-ttu-id="6dd61-157">Si **itagSequence** est égal à 0, le nombre d’instances d’une colonne à valeurs multiples est retourné à la place des données de colonne.</span><span class="sxs-lookup"><span data-stu-id="6dd61-157">If the **itagSequence** is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span> <span data-ttu-id="6dd61-158">Une valeur **itagSequence** de 0 ne peut pas être utilisée dans les appels à [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="6dd61-158">An **itagSequence** value of 0 cannot be used in calls to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="6dd61-159">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="6dd61-159">**columnidNextTagged**</span></span>

<span data-ttu-id="6dd61-160">**ColumnID** de la colonne balisée, à valeurs multiples ou épars lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme **ColumnID** à [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="6dd61-160">The **columnid** of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the **columnid** to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="6dd61-161">**Raise**</span><span class="sxs-lookup"><span data-stu-id="6dd61-161">**err**</span></span>

<span data-ttu-id="6dd61-162">Codes d’erreur et avertissements retournés par la récupération de la colonne.</span><span class="sxs-lookup"><span data-stu-id="6dd61-162">Error codes and warnings returned from the retrieval of the column.</span></span>

### <a name="requirements"></a><span data-ttu-id="6dd61-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dd61-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dd61-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6dd61-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd61-165">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="6dd61-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dd61-166"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6dd61-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd61-167">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6dd61-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dd61-168"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6dd61-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6dd61-169">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6dd61-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6dd61-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dd61-170">See Also</span></span>

[<span data-ttu-id="6dd61-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="6dd61-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="6dd61-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6dd61-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="6dd61-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6dd61-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6dd61-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6dd61-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6dd61-175">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6dd61-175">JET_RETRIEVECOLUMN</span></span>]()  
[<span data-ttu-id="6dd61-176">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="6dd61-176">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="6dd61-177">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="6dd61-177">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
