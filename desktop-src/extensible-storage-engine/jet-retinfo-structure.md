---
description: 'En savoir plus sur : structure JET_RETINFO'
title: Structure JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862966"
---
# <a name="jet_retinfo-structure"></a><span data-ttu-id="2b7a8-103">Structure JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="2b7a8-103">JET_RETINFO Structure</span></span>


<span data-ttu-id="2b7a8-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2b7a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retinfo-structure"></a><span data-ttu-id="2b7a8-105">Structure JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="2b7a8-105">JET_RETINFO Structure</span></span>

<span data-ttu-id="2b7a8-106">La structure **JET_RETINFO** contient des paramètres d’entrée et de sortie facultatifs pour [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b7a8-106">The **JET_RETINFO** structure contains optional input and output parameters for [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span> <span data-ttu-id="2b7a8-107">Un pointeur NULL peut être passé là où un pointeur vers cette structure serait autrement passé.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-107">A null pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="2b7a8-108">Le fait de passer un pointeur null est le même que si vous passez **JET_RETINFO** avec **cbStruct** défini sur sizeof (JET_RETINFO), **ibLongValue** défini sur 0 (zéro) et **itagSequence** défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-108">Passing a null pointer is the same as passing **JET_RETINFO** with **cbStruct** set to sizeof(JET_RETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a><span data-ttu-id="2b7a8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2b7a8-109">Members</span></span>

<span data-ttu-id="2b7a8-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="2b7a8-110">**cbStruct**</span></span>

<span data-ttu-id="2b7a8-111">Doit être défini sur la taille de la structure **JET_RETINFO** , en octets, et sert à confirmer la présence des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-111">Must be set to the size of the **JET_RETINFO** structure, in bytes, and serves to confirm the presence of the following fields.</span></span>

<span data-ttu-id="2b7a8-112">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="2b7a8-112">**ibLongValue**</span></span>

<span data-ttu-id="2b7a8-113">Offset au premier octet à récupérer d’une colonne de type [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="2b7a8-113">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span> <span data-ttu-id="2b7a8-114">Notez que la quantité de données récupérées à partir de ce décalage est inférieure à la taille de la mémoire tampon de sortie et à la taille des données dans la valeur réelle après cet offset.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-114">Note that the amount of data retrieved from this offset is the lower of the size of the output buffer and the size of data in the actual value after this offset.</span></span>

<span data-ttu-id="2b7a8-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="2b7a8-115">**itagSequence**</span></span>

<span data-ttu-id="2b7a8-116">Décrit le numéro de séquence de la valeur dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-116">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="2b7a8-117">Notez que le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-117">Note that the array of values is one-based.</span></span> <span data-ttu-id="2b7a8-118">La première valeur est séquence 1, et non 0.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-118">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="2b7a8-119">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé en tant que **itagSequence**</span><span class="sxs-lookup"><span data-stu-id="2b7a8-119">If the record column has only one value then 1 should be passed as the **itagSequence**</span></span>

<span data-ttu-id="2b7a8-120">Avec une colonne qui peut contenir plusieurs valeurs, il est possible d’utiliser un numéro de séquence supérieur à 1 dans [JetSetColumn](./jetsetcolumn-function.md) et [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 dans [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b7a8-120">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="2b7a8-121">Dans l’implémentation actuelle du moteur, toute colonne créée avec JET_bitColumnTagged peut contenir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-121">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="2b7a8-122">Les colonnes créées avec JET_bitColumnMultiValued différent des colonnes avec balises à valeurs multiples uniquement dans la manière dont elles sont indexées.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-122">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="2b7a8-123">Pour plus d’informations, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="2b7a8-123">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

<span data-ttu-id="2b7a8-124">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="2b7a8-124">**columnidNextTagged**</span></span>

<span data-ttu-id="2b7a8-125">Retourne la valeur columnID de la colonne balisée, à valeurs multiples ou fragmentées récupérées lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme ColumnID à [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b7a8-125">Returns the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="2b7a8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b7a8-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b7a8-127"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2b7a8-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2b7a8-128">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b7a8-129"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2b7a8-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2b7a8-130">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b7a8-131"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2b7a8-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2b7a8-132">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2b7a8-132">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2b7a8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b7a8-133">See Also</span></span>

[<span data-ttu-id="2b7a8-134">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="2b7a8-134">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="2b7a8-135">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2b7a8-135">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="2b7a8-136">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="2b7a8-136">JET_RETINFO</span></span>]()  
[<span data-ttu-id="2b7a8-137">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="2b7a8-137">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)
