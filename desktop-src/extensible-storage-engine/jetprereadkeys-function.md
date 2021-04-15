---
description: 'En savoir plus sur : fonction JetPrereadKeys'
title: JetPrereadKeys fonction)
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484873"
---
# <a name="jetprereadkeys-function"></a><span data-ttu-id="b27e1-103">JetPrereadKeys fonction)</span><span class="sxs-lookup"><span data-stu-id="b27e1-103">JetPrereadKeys Function</span></span>


<span data-ttu-id="b27e1-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b27e1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprereadkeys-function"></a><span data-ttu-id="b27e1-105">JetPrereadKeys fonction)</span><span class="sxs-lookup"><span data-stu-id="b27e1-105">JetPrereadKeys Function</span></span>

<span data-ttu-id="b27e1-106">La fonction **JetPrereadKeys** lit les valeurs clés pour améliorer les performances du nettoyage de la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="b27e1-106">The **JetPrereadKeys** function reads key values to improve the performance of version store cleanup.</span></span>

<span data-ttu-id="b27e1-107">**Windows 7 :** la fonction PrereadKeys est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b27e1-107">**Windows 7:  PrereadKeys** function is introduced in Windows 7.</span></span>

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a><span data-ttu-id="b27e1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b27e1-108">Parameters</span></span>

<span data-ttu-id="b27e1-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b27e1-109">*sesid*</span></span>

<span data-ttu-id="b27e1-110">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="b27e1-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="b27e1-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b27e1-111">*tableid*</span></span>

<span data-ttu-id="b27e1-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="b27e1-112">The cursor to use for this call.</span></span>

<span data-ttu-id="b27e1-113">*rgpvKeys*</span><span class="sxs-lookup"><span data-stu-id="b27e1-113">*rgpvKeys*</span></span>

<span data-ttu-id="b27e1-114">Tableau de pointeurs vers les clés.</span><span class="sxs-lookup"><span data-stu-id="b27e1-114">An array of pointers to keys.</span></span> <span data-ttu-id="b27e1-115">Les clés peuvent être créées avec [JetMakeKey](./jetmakekey-function.md) ou récupérées avec [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="b27e1-115">Keys can be made with [JetMakeKey](./jetmakekey-function.md) or retrieved with [JetGetBookmark](./jetgetbookmark-function.md).</span></span> <span data-ttu-id="b27e1-116">Les clés doivent être triées dans l’ordre croissant ou décroissant, selon le Grbit passé.</span><span class="sxs-lookup"><span data-stu-id="b27e1-116">The keys must be sorted in ascending or descending order, depending on the grbit passed.</span></span> <span data-ttu-id="b27e1-117">Les clés peuvent être triées avec memcmp.</span><span class="sxs-lookup"><span data-stu-id="b27e1-117">Keys can be sorted with memcmp.</span></span>

<span data-ttu-id="b27e1-118">*rgcbKeys*</span><span class="sxs-lookup"><span data-stu-id="b27e1-118">*rgcbKeys*</span></span>

<span data-ttu-id="b27e1-119">Tableau de longueurs de clé.</span><span class="sxs-lookup"><span data-stu-id="b27e1-119">An array of key lengths.</span></span> <span data-ttu-id="b27e1-120">rgpvKeys \[ n \] doit pointer vers une clé de longueur rgcbKeys \[ n\]</span><span class="sxs-lookup"><span data-stu-id="b27e1-120">rgpvKeys\[n\] should point to a key of length rgcbKeys\[n\]</span></span>

<span data-ttu-id="b27e1-121">*ckeys*</span><span class="sxs-lookup"><span data-stu-id="b27e1-121">*ckeys*</span></span>

<span data-ttu-id="b27e1-122">Nombre de clés.</span><span class="sxs-lookup"><span data-stu-id="b27e1-122">The number of keys.</span></span> <span data-ttu-id="b27e1-123">rgpvKeys et rgcbKeys doivent tous pointer vers un tableau avec au moins éléments ckeys.</span><span class="sxs-lookup"><span data-stu-id="b27e1-123">rgpvKeys and rgcbKeys must each point to an array with at least ckeys elements.</span></span>

<span data-ttu-id="b27e1-124">*pckeysPreread*</span><span class="sxs-lookup"><span data-stu-id="b27e1-124">*pckeysPreread*</span></span>

<span data-ttu-id="b27e1-125">Retourne le nombre de clés pour lesquelles des prélectures ont été émises.</span><span class="sxs-lookup"><span data-stu-id="b27e1-125">Returns the number of keys that prereads were actually issued for.</span></span> <span data-ttu-id="b27e1-126">Ce paramètre peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="b27e1-126">This parameter can be NULL.</span></span>

<span data-ttu-id="b27e1-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b27e1-127">*grbit*</span></span>

<span data-ttu-id="b27e1-128">Il doit s’agir d’JET_bitPrereadForward ou JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="b27e1-128">This must be either JET_bitPrereadForward or JET_bitPrereadBackward.</span></span> <span data-ttu-id="b27e1-129">Si Grbit est JET_bitPrereadForward, les clés doivent être triées dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="b27e1-129">If grbit is JET_bitPrereadForward, the keys must be sorted in ascending order.</span></span> <span data-ttu-id="b27e1-130">Si Grbit est JET_bitPrereadBackward, les clés doivent être triées dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="b27e1-130">If grbit is JET_bitPrereadBackward, the keys must be sorted in descending order.</span></span>

### <a name="return-value"></a><span data-ttu-id="b27e1-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b27e1-131">Return Value</span></span>

<span data-ttu-id="b27e1-132">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="b27e1-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b27e1-133">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b27e1-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="b27e1-134">Diverses erreurs d’e/s peuvent être retournées avec les erreurs d’utilisation de l’API suivantes :</span><span class="sxs-lookup"><span data-stu-id="b27e1-134">Various I/O errors can be returned along with these API usage errors:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b27e1-135">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b27e1-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="b27e1-136">Description</span><span class="sxs-lookup"><span data-stu-id="b27e1-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b27e1-137">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="b27e1-137">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="b27e1-138">Grbit n’était ni JET_bitPrereadForward ni JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="b27e1-138">Grbit was neither JET_bitPrereadForward nor JET_bitPrereadBackward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27e1-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="b27e1-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="b27e1-140">Une taille de clé incorrecte a été passée.</span><span class="sxs-lookup"><span data-stu-id="b27e1-140">An incorrect key size has been passed in.</span></span> <span data-ttu-id="b27e1-141">Les clés ne peuvent pas être égales à 0 ni supérieure à la longueur de clé maximale pour la table.</span><span class="sxs-lookup"><span data-stu-id="b27e1-141">Keys can neither be 0 nor longer than the maximum key length for the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27e1-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b27e1-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b27e1-143">Un paramètre non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="b27e1-143">An invalid parameter has been passed in.</span></span> <span data-ttu-id="b27e1-144">Cela peut être dû à une valeur null pour un paramètre obligatoire ou peut indiquer que le tableau de clés n’est pas correctement trié.</span><span class="sxs-lookup"><span data-stu-id="b27e1-144">This can be caused by a null value for a required parameter or can indicate that the key array is not sorted properly.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b27e1-145">**JetPrereadKeys** parcourt les pages internes de l’arbre b (b-Tree) pour déterminer quelles pages de feuille contiennent les clés spécifiées par RgpvKeys/rgcbKeys.</span><span class="sxs-lookup"><span data-stu-id="b27e1-145">**JetPrereadKeys** traverses the internal pages of the b-tree to determine which leaf pages contain the keys specified by rgpvKeys/rgcbKeys.</span></span> <span data-ttu-id="b27e1-146">La liste des pages feuille est triée, puis les prélectures sont émises pour les plages de pages.</span><span class="sxs-lookup"><span data-stu-id="b27e1-146">The list of leaf pages is sorted and then prereads are issued for the ranges of pages.</span></span> <span data-ttu-id="b27e1-147">Le nombre de pages pouvant être prélues est limité. il est donc possible que toutes les clés ne soient pas prélues.</span><span class="sxs-lookup"><span data-stu-id="b27e1-147">The number of pages that can be preread is limited so it is possible that not all keys may be preread.</span></span> <span data-ttu-id="b27e1-148">Dans ce cas, le nombre de clés réellement prélues est retourné dans pckeysPreread.</span><span class="sxs-lookup"><span data-stu-id="b27e1-148">In that case, the number of keys actually preread is returned in pckeysPreread.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b27e1-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b27e1-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b27e1-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b27e1-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b27e1-151">Requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b27e1-151">Requires Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27e1-152"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b27e1-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b27e1-153">Requiert Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b27e1-153">Requires Windows Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27e1-154"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b27e1-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b27e1-155">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b27e1-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b27e1-156"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="b27e1-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b27e1-157">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b27e1-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b27e1-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b27e1-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b27e1-159">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b27e1-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>
