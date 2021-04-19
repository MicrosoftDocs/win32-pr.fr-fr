---
description: 'En savoir plus sur : fonction JetCreateIndex'
title: Fonction JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534564"
---
# <a name="jetcreateindex-function"></a><span data-ttu-id="d28e4-103">Fonction JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="d28e4-103">JetCreateIndex Function</span></span>


<span data-ttu-id="d28e4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d28e4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex-function"></a><span data-ttu-id="d28e4-105">Fonction JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="d28e4-105">JetCreateIndex Function</span></span>

<span data-ttu-id="d28e4-106">La fonction **JetCreateIndex** vous permet de créer un index de données dans une base de données ESE (Extensible Storage Engine), que vous pouvez utiliser pour rechercher rapidement des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d28e4-106">The **JetCreateIndex** function enables you to create an index of data in an Extensible Storage Engine (ESE) database, which you can use to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a><span data-ttu-id="d28e4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d28e4-107">Parameters</span></span>

<span data-ttu-id="d28e4-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d28e4-108">*sesid*</span></span>

<span data-ttu-id="d28e4-109">Contexte de la session de base de données à utiliser pour un appel d’API particulier.</span><span class="sxs-lookup"><span data-stu-id="d28e4-109">The database session context to use for a particular API call.</span></span>

<span data-ttu-id="d28e4-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d28e4-110">*tableid*</span></span>

<span data-ttu-id="d28e4-111">Table pour laquelle un index sera créé.</span><span class="sxs-lookup"><span data-stu-id="d28e4-111">The table that an index will be created for.</span></span>

<span data-ttu-id="d28e4-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="d28e4-112">*szIndexName*</span></span>

<span data-ttu-id="d28e4-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’index à créer.</span><span class="sxs-lookup"><span data-stu-id="d28e4-113">A pointer to a null-terminated string that specifies the name of the index to be created.</span></span>

<span data-ttu-id="d28e4-114">Le nom de l’index doit être conforme aux indications suivantes :</span><span class="sxs-lookup"><span data-stu-id="d28e4-114">The index name must conform to the following guidelines:</span></span>

  - <span data-ttu-id="d28e4-115">Il doit contenir moins de caractères que JET_cbNameMost, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="d28e4-115">It must contain fewer characters than JET_cbNameMost, not including the terminating null character.</span></span>

  - <span data-ttu-id="d28e4-116">Il doit contenir uniquement des caractères des catégories suivantes : 0 à 9, A à Z, a à z et tous les caractères de ponctuation, à l’exception de « \! »</span><span class="sxs-lookup"><span data-stu-id="d28e4-116">It must contain only characters from the following categories: 0 through 9, A through Z, a through z, and all punctuation characters except for "\!"</span></span> <span data-ttu-id="d28e4-117">(point d’exclamation), « , » (virgule), « \[ » (crochet ouvrant) et « \] » (crochet fermant), c’est-à-dire les caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F.</span><span class="sxs-lookup"><span data-stu-id="d28e4-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, the ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="d28e4-118">Il ne doit pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="d28e4-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="d28e4-119">Il doit contenir au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="d28e4-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="d28e4-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d28e4-120">*grbit*</span></span>

<span data-ttu-id="d28e4-121">Groupe de bits qui contient les options à utiliser pour un appel particulier.</span><span class="sxs-lookup"><span data-stu-id="d28e4-121">A group of bits that contains the options to be used for a particular call.</span></span> <span data-ttu-id="d28e4-122">Ce paramètre peut inclure zéro, une ou plusieurs des options figurant dans la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d28e4-122">This parameter can include zero or more of the options found in the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="d28e4-123">*szKey*</span><span class="sxs-lookup"><span data-stu-id="d28e4-123">*szKey*</span></span>

<span data-ttu-id="d28e4-124">Pointeur vers une chaîne double se terminant par un caractère null des jetons délimités par des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="d28e4-124">A pointer to a double null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="d28e4-125">Pour plus d’informations sur ce paramètre, consultez la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d28e4-125">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="d28e4-126">*cbKey*</span><span class="sxs-lookup"><span data-stu-id="d28e4-126">*cbKey*</span></span>

<span data-ttu-id="d28e4-127">Longueur, en octets, du paramètre *szKey* , y compris les deux caractères null de fin.</span><span class="sxs-lookup"><span data-stu-id="d28e4-127">The length, in bytes, of the *szKey* parameter, including the two terminating null characters.</span></span>

<span data-ttu-id="d28e4-128">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="d28e4-128">*lDensity*</span></span>

<span data-ttu-id="d28e4-129">Densité de pourcentage de l’index initial B +.</span><span class="sxs-lookup"><span data-stu-id="d28e4-129">The percentage density of the initial index B+ tree.</span></span>

<span data-ttu-id="d28e4-130">Pour plus d’informations sur ce paramètre, consultez la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d28e4-130">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

### <a name="return-value"></a><span data-ttu-id="d28e4-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d28e4-131">Return Value</span></span>

<span data-ttu-id="d28e4-132">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d28e4-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="d28e4-133">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d28e4-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d28e4-134">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d28e4-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="d28e4-135">Signification</span><span class="sxs-lookup"><span data-stu-id="d28e4-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d28e4-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d28e4-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d28e4-137">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d28e4-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d28e4-138">Pour obtenir la liste des erreurs supplémentaires qui peuvent être retournées par la fonction **JetCreateIndex** , consultez [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="d28e4-138">For a list of additional errors that can be returned by the **JetCreateIndex** function, see [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="d28e4-139">Notes</span><span class="sxs-lookup"><span data-stu-id="d28e4-139">Remarks</span></span>

<span data-ttu-id="d28e4-140">L’appel de la fonction **JetCreateIndex** est identique à l’appel de la fonction [JetCreateIndex2](./jetcreateindex2-function.md) avec une structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) contenant les mêmes paramètres que les paramètres de **JetCreateIndex** et un paramètre *cIndexCreate* égal à 1.</span><span class="sxs-lookup"><span data-stu-id="d28e4-140">Calling the **JetCreateIndex** function is identical to calling the [JetCreateIndex2](./jetcreateindex2-function.md) function with a [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure containing the same settings as the parameters of **JetCreateIndex**, and a *cIndexCreate* parameter equal to 1.</span></span> <span data-ttu-id="d28e4-141">Pour les champs de la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) qui n’ont pas de paramètres correspondants dans **JetCreateIndex**, la valeur 0 est utilisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d28e4-141">For the fields of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure that do not have corresponding parameters in **JetCreateIndex**, a value of 0 is assumed.</span></span>

<span data-ttu-id="d28e4-142">Notez que **JetCreateIndex** a été remplacé par [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="d28e4-142">Note that **JetCreateIndex** has been superseded by [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="d28e4-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d28e4-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d28e4-144">Client</span><span class="sxs-lookup"><span data-stu-id="d28e4-144">Client</span></span></p></td>
<td><p><span data-ttu-id="d28e4-145">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d28e4-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d28e4-146">Serveur</span><span class="sxs-lookup"><span data-stu-id="d28e4-146">Server</span></span></p></td>
<td><p><span data-ttu-id="d28e4-147">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d28e4-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d28e4-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="d28e4-148">Header</span></span></p></td>
<td><p><span data-ttu-id="d28e4-149">Est déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d28e4-149">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d28e4-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d28e4-150">Library</span></span></p></td>
<td><p><span data-ttu-id="d28e4-151">Utilise ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d28e4-151">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d28e4-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d28e4-152">DLL</span></span></p></td>
<td><p><span data-ttu-id="d28e4-153">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d28e4-153">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d28e4-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="d28e4-154">Unicode</span></span></p></td>
<td><p><span data-ttu-id="d28e4-155">Est implémenté en tant que <strong>JetCreateIndexW</strong> (Unicode) et <strong>JetCreateIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d28e4-155">Is implemented as <strong>JetCreateIndexW</strong> (Unicode) and <strong>JetCreateIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d28e4-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d28e4-156">See Also</span></span>

[<span data-ttu-id="d28e4-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d28e4-157">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d28e4-158">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d28e4-158">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d28e4-159">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d28e4-159">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d28e4-160">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d28e4-160">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d28e4-161">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="d28e4-161">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="d28e4-162">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="d28e4-162">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="d28e4-163">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="d28e4-163">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="d28e4-164">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="d28e4-164">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
