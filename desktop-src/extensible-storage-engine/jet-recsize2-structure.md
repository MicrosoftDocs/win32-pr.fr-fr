---
description: 'En savoir plus sur : structure JET_RECSIZE2'
title: Structure JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536510"
---
# <a name="jet_recsize2-structure"></a><span data-ttu-id="17277-103">Structure JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="17277-103">JET_RECSIZE2 Structure</span></span>


<span data-ttu-id="17277-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="17277-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize2-structure"></a><span data-ttu-id="17277-105">Structure JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="17277-105">JET_RECSIZE2 Structure</span></span>

<span data-ttu-id="17277-106">La structure **JET_RECSIZE2** est utilisée par [JetGetRecordSize2](./jetgetrecordsize2-function.md) pour retourner des informations sur les conditions d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de la structure d’enregistrement ESE.</span><span class="sxs-lookup"><span data-stu-id="17277-106">The **JET_RECSIZE2** structure is used by [JetGetRecordSize2](./jetgetrecordsize2-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="17277-107">**Windows 7 :** La structure **JET_RECSIZE2** est introduite dans le système d’exploitation Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17277-107">**Windows 7:** The **JET_RECSIZE2** structure is introduced in the Windows 7 operating system.</span></span>

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a><span data-ttu-id="17277-108">Membres</span><span class="sxs-lookup"><span data-stu-id="17277-108">Members</span></span>

<span data-ttu-id="17277-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="17277-109">**cbData**</span></span>

<span data-ttu-id="17277-110">Jeu de données utilisateur dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-110">User data set in the record.</span></span>

<span data-ttu-id="17277-111">**Remarque**  La taille de la clé n’est pas incluse dans ce.</span><span class="sxs-lookup"><span data-stu-id="17277-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="17277-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="17277-112">**cbLongValueData**</span></span>

<span data-ttu-id="17277-113">Données utilisateur associées à l’enregistrement, mais stockées dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="17277-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="17277-114">**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="17277-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="17277-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="17277-115">**cbOverhead**</span></span>

<span data-ttu-id="17277-116">Surcharge de la structure d’enregistrement ESE pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="17277-117">Cela comprend la taille de la clé de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-117">This includes the record's key size.</span></span>

<span data-ttu-id="17277-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="17277-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="17277-119">Charge des données de valeur longue.</span><span class="sxs-lookup"><span data-stu-id="17277-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="17277-120">**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="17277-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="17277-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="17277-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="17277-122">Nombre total de colonnes fixes et variables définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="17277-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="17277-123">**cTaggedColumns**</span></span>

<span data-ttu-id="17277-124">Nombre total de colonnes avec balises définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="17277-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="17277-125">**cLongValues**</span></span>

<span data-ttu-id="17277-126">Nombre total de valeurs longues stockées dans l’arborescence de valeurs longues pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="17277-127">**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="17277-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="17277-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="17277-128">**cMultiValues**</span></span>

<span data-ttu-id="17277-129">Accumulation du nombre total de valeurs au-delà de la première pour toutes les colonnes de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

<span data-ttu-id="17277-130">**cCompressedColumns**</span><span class="sxs-lookup"><span data-stu-id="17277-130">**cCompressedColumns**</span></span>

<span data-ttu-id="17277-131">Nombre total de colonnes compressées.</span><span class="sxs-lookup"><span data-stu-id="17277-131">The total number of compressed columns.</span></span>

<span data-ttu-id="17277-132">**cbDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="17277-132">**cbDataCompressed**</span></span>

<span data-ttu-id="17277-133">Taille compressée des données utilisateur dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="17277-133">The compressed size of user data in this record.</span></span> <span data-ttu-id="17277-134">C’est le même que cbData si aucune valeur long intrinsèque n’est compressée.</span><span class="sxs-lookup"><span data-stu-id="17277-134">This is the same as cbData if no intrinsic long-values are compressed.</span></span>

<span data-ttu-id="17277-135">**cbLongValueDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="17277-135">**cbLongValueDataCompressed**</span></span>

<span data-ttu-id="17277-136">Taille compressée des données utilisateur dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="17277-136">The compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="17277-137">Cela est identique à celui des données cbLongValue si aucune valeur longue séparée n’est compressée.</span><span class="sxs-lookup"><span data-stu-id="17277-137">This is the same as cbLongValue data if no separated long values are compressed.</span></span>

### <a name="remarks"></a><span data-ttu-id="17277-138">Notes</span><span class="sxs-lookup"><span data-stu-id="17277-138">Remarks</span></span>

<span data-ttu-id="17277-139">Le nombre total de valeurs dans l’enregistrement serait **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="17277-139">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

<span data-ttu-id="17277-140">Les données logiques de l’enregistrement sont (cbData + cbLongValueData) et la taille physique des données est (cbDataCompressed + cbLongValueDataCompressed).</span><span class="sxs-lookup"><span data-stu-id="17277-140">The logical data in the record is (cbData+cbLongValueData) and the physical size of the data is (cbDataCompressed+cbLongValueDataCompressed).</span></span> <span data-ttu-id="17277-141">Cela peut être utilisé pour calculer le taux de compression des données stockées.</span><span class="sxs-lookup"><span data-stu-id="17277-141">This can be used to calculate the compression ratio of stored data.</span></span>

### <a name="requirements"></a><span data-ttu-id="17277-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17277-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17277-143"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="17277-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="17277-144">Nécessite le système d’exploitation Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="17277-144">Requires Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17277-145"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="17277-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="17277-146">Nécessite le système d’exploitation Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="17277-146">Requires Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17277-147"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="17277-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="17277-148">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="17277-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="17277-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17277-149">See Also</span></span>

[<span data-ttu-id="17277-150">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="17277-150">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)  
[<span data-ttu-id="17277-151">JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="17277-151">JetGetRecordSize2</span></span>](./jetgetrecordsize2-function.md)
