---
description: 'En savoir plus sur : structure JET_RECSIZE'
title: Structure JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
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
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749853"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="fdfa0-103">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="fdfa0-103">JET_RECSIZE Structure</span></span>


<span data-ttu-id="fdfa0-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="fdfa0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize-structure"></a><span data-ttu-id="fdfa0-105">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="fdfa0-105">JET_RECSIZE Structure</span></span>

<span data-ttu-id="fdfa0-106">La structure **JET_RECSIZE** est utilisée par [JetGetRecordSize](./jetgetrecordsize-function.md) pour retourner des informations sur les conditions d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de la structure d’enregistrement ESE.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-106">The **JET_RECSIZE** structure is used by [JetGetRecordSize](./jetgetrecordsize-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="fdfa0-107">**Windows Vista :** La structure **JET_RECSIZE** est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-107">**Windows Vista:** The **JET_RECSIZE** structure is introduced in Windows Vista.</span></span>

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
    } JET_RECSIZE;
```

### <a name="members"></a><span data-ttu-id="fdfa0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fdfa0-108">Members</span></span>

<span data-ttu-id="fdfa0-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-109">**cbData**</span></span>

<span data-ttu-id="fdfa0-110">Jeu de données utilisateur dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-110">User data set in the record.</span></span>

<span data-ttu-id="fdfa0-111">**Remarque**  La taille de la clé n’est pas incluse dans ce.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="fdfa0-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-112">**cbLongValueData**</span></span>

<span data-ttu-id="fdfa0-113">Données utilisateur associées à l’enregistrement, mais stockées dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="fdfa0-114">**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="fdfa0-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-115">**cbOverhead**</span></span>

<span data-ttu-id="fdfa0-116">Surcharge de la structure d’enregistrement ESE pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="fdfa0-117">Cela comprend la taille de la clé de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-117">This includes the record's key size.</span></span>

<span data-ttu-id="fdfa0-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="fdfa0-119">Charge des données de valeur longue.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="fdfa0-120">**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="fdfa0-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="fdfa0-122">Nombre total de colonnes fixes et variables définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="fdfa0-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-123">**cTaggedColumns**</span></span>

<span data-ttu-id="fdfa0-124">Nombre total de colonnes avec balises définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="fdfa0-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-125">**cLongValues**</span></span>

<span data-ttu-id="fdfa0-126">Nombre total de valeurs longues stockées dans l’arborescence de valeurs longues pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="fdfa0-127">**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="fdfa0-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="fdfa0-128">**cMultiValues**</span></span>

<span data-ttu-id="fdfa0-129">Accumulation du nombre total de valeurs au-delà de la première pour toutes les colonnes de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

### <a name="remarks"></a><span data-ttu-id="fdfa0-130">Notes</span><span class="sxs-lookup"><span data-stu-id="fdfa0-130">Remarks</span></span>

<span data-ttu-id="fdfa0-131">Le nombre total de valeurs dans l’enregistrement serait **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-131">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

### <a name="requirements"></a><span data-ttu-id="fdfa0-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdfa0-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdfa0-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-134">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-134">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdfa0-135"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-136">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-136">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdfa0-137"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="fdfa0-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fdfa0-138">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-138">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fdfa0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdfa0-139">See Also</span></span>

[<span data-ttu-id="fdfa0-140">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="fdfa0-140">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)
