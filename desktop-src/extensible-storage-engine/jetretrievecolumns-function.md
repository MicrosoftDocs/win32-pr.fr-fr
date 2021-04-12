---
description: 'En savoir plus sur : fonction JetRetrieveColumns'
title: Fonction JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210377"
---
# <a name="jetretrievecolumns-function"></a><span data-ttu-id="89f87-103">Fonction JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="89f87-103">JetRetrieveColumns Function</span></span>


<span data-ttu-id="89f87-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="89f87-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumns-function"></a><span data-ttu-id="89f87-105">Fonction JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="89f87-105">JetRetrieveColumns Function</span></span>

<span data-ttu-id="89f87-106">La fonction **JetRetrieveColumns** Récupère plusieurs valeurs de colonne de l’enregistrement actuel en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="89f87-106">The **JetRetrieveColumns** function retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="89f87-107">Un tableau de structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) est utilisé pour décrire l’ensemble des valeurs de colonne à récupérer et pour décrire les mémoires tampons de sortie pour chaque valeur de colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="89f87-107">An array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="89f87-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89f87-108">Parameters</span></span>

<span data-ttu-id="89f87-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="89f87-109">*sesid*</span></span>

<span data-ttu-id="89f87-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="89f87-110">The session to use for this call.</span></span>

<span data-ttu-id="89f87-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="89f87-111">*tableid*</span></span>

<span data-ttu-id="89f87-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="89f87-112">The cursor to use for this call.</span></span>

<span data-ttu-id="89f87-113">*pretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="89f87-113">*pretrievecolumn*</span></span>

<span data-ttu-id="89f87-114">Pointeur vers un tableau d’une ou plusieurs structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="89f87-114">A pointer to an array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="89f87-115">Chaque structure comprend des descriptions de la valeur de colonne à récupérer et de l’emplacement de stockage des données retournées.</span><span class="sxs-lookup"><span data-stu-id="89f87-115">Each structure includes descriptions of which column value to retrieve and where to store returned data.</span></span>

<span data-ttu-id="89f87-116">*cretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="89f87-116">*cretrievecolumn*</span></span>

<span data-ttu-id="89f87-117">Nombre de structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) dans le tableau donné par *pretrievecolumn*.</span><span class="sxs-lookup"><span data-stu-id="89f87-117">The number of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures in the array given by *pretrievecolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="89f87-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89f87-118">Return Value</span></span>

<span data-ttu-id="89f87-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="89f87-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="89f87-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="89f87-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89f87-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="89f87-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="89f87-122">Description</span><span class="sxs-lookup"><span data-stu-id="89f87-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f87-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="89f87-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="89f87-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="89f87-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-125">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="89f87-125">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="89f87-126">Une valeur de numéro de séquence de colonne à valeurs multiples non valide a été transmise dans pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="89f87-126">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="89f87-127">Les valeurs valides pour les numéros de séquence de valeur de colonne à valeurs multiples sont égales ou supérieures à 1.</span><span class="sxs-lookup"><span data-stu-id="89f87-127">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="89f87-128">La valeur 0 (zéro) est valide pour cette fonction, mais n’est pas valide pour <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="89f87-128">A value of 0 (zero) is valid for this function but is invalid for <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-129">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="89f87-129">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="89f87-130">L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="89f87-130">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="89f87-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="89f87-132">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="89f87-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="89f87-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="89f87-134">La colonne décrite par le <em>ColumnID</em> donné n’existe pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="89f87-134">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-135">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="89f87-135">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="89f87-136">Les colonnes indexées en tant que sous-chaînes ne peuvent pas être récupérées à partir de l’index, car seule une petite partie de la colonne est généralement présente dans chaque entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="89f87-136">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-137">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="89f87-137">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="89f87-138">Dans certains cas, la mémoire tampon donnée pour la colonne de récupération doit être suffisamment dimensionnée pour pouvoir retourner n’importe quel volume de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="89f87-138">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="89f87-139">Par exemple, les colonnes pouvant être mises à jour par tiers de confiance sont ajustées pour être cohérentes pour le contexte transactionnel de la session appelante et cet ajustement requiert la mémoire tampon fournie par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="89f87-139">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="89f87-140">Si un espace de mémoire tampon insuffisant est fourni, JET_errInvalidBufferSize est retourné et aucune donnée de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="89f87-140">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-141">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="89f87-141">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="89f87-142">Les options fournies sont inconnues ou une combinaison non conforme de paramètres de bits connus.</span><span class="sxs-lookup"><span data-stu-id="89f87-142">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="89f87-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="89f87-144">Un ou plusieurs des paramètres spécifiés sont incorrects.</span><span class="sxs-lookup"><span data-stu-id="89f87-144">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="89f87-145">Cela peut se produire si retinfo. cbStruct est plus petit que la taille de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="89f87-145">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="89f87-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="89f87-147">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="89f87-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="89f87-148"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="89f87-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-149">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="89f87-149">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="89f87-150">Le curseur n’est pas positionné sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="89f87-150">The cursor is not positioned on a record.</span></span> <span data-ttu-id="89f87-151">Cela peut se produire pour de nombreuses raisons différentes.</span><span class="sxs-lookup"><span data-stu-id="89f87-151">This can happen for many different reasons.</span></span> <span data-ttu-id="89f87-152">Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="89f87-152">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="89f87-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="89f87-154">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="89f87-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="89f87-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="89f87-156">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="89f87-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-157">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="89f87-157">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="89f87-158">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="89f87-158">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="89f87-159"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="89f87-159"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="89f87-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="89f87-161">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="89f87-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-162">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="89f87-162">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="89f87-163">Impossible de récupérer la valeur de colonne entière, car la taille de la mémoire tampon donnée est inférieure à celle de la colonne.</span><span class="sxs-lookup"><span data-stu-id="89f87-163">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89f87-164">En cas de réussite, les données de colonnes et la taille de colonne sont retournées dans les mémoires tampons fournies décrites dans tableau de structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="89f87-164">On success, columns data and column size are returned in provided buffers described in array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="89f87-165">Si un *itagSequence* a été défini sur 0 (zéro) pour indiquer que le nombre d’instances d’un champ à valeurs multiples était souhaité à la place des données de colonne, le nombre d’instances d’une colonne à valeurs multiples est retourné dans le champ *itagSequence* lui-même.</span><span class="sxs-lookup"><span data-stu-id="89f87-165">If an *itagSequence* was set to 0 (zero) to indicate that the number of instances of a multi-valued field was desired instead of column data, then the number of instances of a multi-valued column is returned in the *itagSequence* field itself.</span></span> <span data-ttu-id="89f87-166">Chaque structure de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) a un champ d’erreur qui contient des avertissements pour la colonne récupérée.</span><span class="sxs-lookup"><span data-stu-id="89f87-166">Each [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure has an error field that contains warnings for the column retrieved.</span></span> <span data-ttu-id="89f87-167">Si la colonne a une valeur **null** , le code d’erreur est défini sur JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="89f87-167">If the column was **NULL** valued, then the error code will be set to JET_wrnColumnNull.</span></span>

<span data-ttu-id="89f87-168">En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée n’est copiée dans la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="89f87-168">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89f87-169">Notes</span><span class="sxs-lookup"><span data-stu-id="89f87-169">Remarks</span></span>

<span data-ttu-id="89f87-170">**JetRetrieveColumns** prend en charge une fonctionnalité que [JetRetrieveColumn](./jetretrievecolumn-function.md) ne fait pas.</span><span class="sxs-lookup"><span data-stu-id="89f87-170">**JetRetrieveColumns** supports one feature that [JetRetrieveColumn](./jetretrievecolumn-function.md) does not.</span></span> <span data-ttu-id="89f87-171">Il s’agit de la possibilité de récupérer le nombre d’instances d’une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="89f87-171">This is the ability to retrieve the number of instances of a multi-valued column.</span></span> <span data-ttu-id="89f87-172">L’objectif de cette fonctionnalité est de permettre à une application de récupérer toutes les valeurs d’une colonne.</span><span class="sxs-lookup"><span data-stu-id="89f87-172">The purpose of this feature is to allow an application to retrieve all values of a column.</span></span> <span data-ttu-id="89f87-173">Pour ce faire, vous devez d’abord déterminer le nombre de valeurs d’une colonne.</span><span class="sxs-lookup"><span data-stu-id="89f87-173">This can be done by first determining the number of values that a column has.</span></span> <span data-ttu-id="89f87-174">Ensuite, leur longueur peut être déterminée en appelant à nouveau **JetRetrieveColumns** avec une structure [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) allouée pour chaque valeur afin de déterminer la longueur des données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="89f87-174">Next, their lengths can be determined by calling **JetRetrieveColumns** again with one [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure allocated for each value to determine the length of column data.</span></span> <span data-ttu-id="89f87-175">Pour ce faire, vous pouvez passer des pointeurs _PvData_ **null** avec *cbMax* de 0 (zéro) et récupérer la longueur de colonne dans *cbActual*.</span><span class="sxs-lookup"><span data-stu-id="89f87-175">This can be done by passing **NULL**_pvData_ pointers with *cbMax* of 0 (zero) and retrieving the column length in *cbActual*.</span></span> <span data-ttu-id="89f87-176">Le troisième et le dernier appel peuvent être effectués avec la mémoire allouée pour les données de valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="89f87-176">The third and last call can be made with allocated memory for the column value data.</span></span>

<span data-ttu-id="89f87-177">Si une colonne Récupérée est tronquée en raison d’une mémoire tampon de longueur insuffisante, l’API retourne JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="89f87-177">If any column retrieved is truncated due to an insufficient length buffer, then the API will return JET_wrnBufferTruncated.</span></span> <span data-ttu-id="89f87-178">Toutefois, d’autres erreurs, JET_wrnColumnNull sont retournées uniquement dans le champ d’erreur de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="89f87-178">However, other errors, JET_wrnColumnNull are returned only in the error field in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="89f87-179">Cela est dû au fait que les applications veulent souvent s’assurer que toutes les données ont été récupérées et que le retour de cette erreur à partir de **JetRetrieveColumns** facilite cette compréhension.</span><span class="sxs-lookup"><span data-stu-id="89f87-179">The reason for this is that applications often want to ensure that all data has been retrieved and returning this error from **JetRetrieveColumns** facilitates this understanding.</span></span>

#### <a name="requirements"></a><span data-ttu-id="89f87-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89f87-180">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f87-181"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="89f87-181"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="89f87-182">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="89f87-182">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-183"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="89f87-183"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="89f87-184">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="89f87-184">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-185"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="89f87-185"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="89f87-186">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="89f87-186">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f87-187"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="89f87-187"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="89f87-188">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="89f87-188">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f87-189"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="89f87-189"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="89f87-190">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="89f87-190">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="89f87-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89f87-191">See Also</span></span>

[<span data-ttu-id="89f87-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="89f87-192">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="89f87-193">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="89f87-193">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="89f87-194">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="89f87-194">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="89f87-195">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="89f87-195">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="89f87-196">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="89f87-196">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="89f87-197">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="89f87-197">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="89f87-198">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="89f87-198">JetSetColumns</span></span>](./jetsetcolumns-function.md)
