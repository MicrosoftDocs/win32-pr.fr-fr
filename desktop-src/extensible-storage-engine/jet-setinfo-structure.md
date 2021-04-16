---
description: 'En savoir plus sur : structure JET_SETINFO'
title: Structure JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531119"
---
# <a name="jet_setinfo-structure"></a><span data-ttu-id="31200-103">Structure JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="31200-103">JET_SETINFO Structure</span></span>


<span data-ttu-id="31200-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="31200-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setinfo-structure"></a><span data-ttu-id="31200-105">Structure JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="31200-105">JET_SETINFO Structure</span></span>

<span data-ttu-id="31200-106">La structure **JET_SETINFO** contient des paramètres d’entrée facultatifs pour [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="31200-106">The **JET_SETINFO** structure contains optional input parameters for [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="31200-107">Un pointeur **null** peut être passé là où un pointeur vers cette structure serait autrement passé.</span><span class="sxs-lookup"><span data-stu-id="31200-107">A **NULL** pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="31200-108">La signification de la transmission d’une **valeur null** est la même que le passage de **JET_SETINFO** avec **cbStruct** défini sur sizeof (JET_SETINFO), **ibLongValue** défini sur 0 (zéro) et **itagSequence** défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="31200-108">The meaning of passing a **NULL** is the same as passing **JET_SETINFO** with **cbStruct** set to sizeof(JET_SETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a><span data-ttu-id="31200-109">Membres</span><span class="sxs-lookup"><span data-stu-id="31200-109">Members</span></span>

<span data-ttu-id="31200-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="31200-110">**cbStruct**</span></span>

<span data-ttu-id="31200-111">Taille, en octets, de la **JET_SETINFO**.</span><span class="sxs-lookup"><span data-stu-id="31200-111">The size, in bytes, of the **JET_SETINFO**.</span></span> <span data-ttu-id="31200-112">Cette valeur confirme la présence des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="31200-112">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="31200-113">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="31200-113">**ibLongValue**</span></span>

<span data-ttu-id="31200-114">Offset au premier octet à définir dans une colonne de type [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="31200-114">The offset to the first byte to be set in a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="31200-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="31200-115">**itagSequence**</span></span>

<span data-ttu-id="31200-116">Décrit le numéro de séquence de la valeur dans une colonne à valeurs multiples à définir.</span><span class="sxs-lookup"><span data-stu-id="31200-116">Describes the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="31200-117">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="31200-117">The array of values is one-based.</span></span> <span data-ttu-id="31200-118">La première valeur est Sequence 1, et non 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="31200-118">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="31200-119">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé comme **itagSequence** si cette valeur est remplacée.</span><span class="sxs-lookup"><span data-stu-id="31200-119">If the record column has only one value then 1 should be passed as the **itagSequence** if that value is being replaced.</span></span> <span data-ttu-id="31200-120">La valeur 0 (zéro) signifie que vous pouvez ajouter une nouvelle instance de valeur de colonne à la fin de la séquence de valeurs de colonne.</span><span class="sxs-lookup"><span data-stu-id="31200-120">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="31200-121">Avec une colonne qui peut contenir plusieurs valeurs, il est possible d’utiliser un numéro de séquence supérieur à 1 dans [JetSetColumn](./jetsetcolumn-function.md) et [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 dans [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="31200-121">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="31200-122">Dans l’implémentation actuelle du moteur, toute colonne créée avec JET_bitColumnTagged peut contenir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="31200-122">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="31200-123">Les colonnes créées avec JET_bitColumnMultiValued différent des colonnes avec balises à valeurs multiples uniquement dans la manière dont elles sont indexées.</span><span class="sxs-lookup"><span data-stu-id="31200-123">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="31200-124">Pour plus d’informations, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="31200-124">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

### <a name="requirements"></a><span data-ttu-id="31200-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31200-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31200-126"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="31200-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="31200-127">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="31200-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31200-128"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="31200-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="31200-129">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="31200-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31200-130"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="31200-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="31200-131">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="31200-131">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="31200-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31200-132">See Also</span></span>

[<span data-ttu-id="31200-133">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="31200-133">JetSetColumn</span></span>](./jetsetcolumn-function.md)
