---
description: La structure SET définit un ensemble de valeurs.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: DÉFINIR la structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202867"
---
# <a name="set-structure"></a><span data-ttu-id="5571b-103">DÉFINIR la structure</span><span class="sxs-lookup"><span data-stu-id="5571b-103">SET structure</span></span>

<span data-ttu-id="5571b-104">La structure **Set** définit un ensemble de valeurs.</span><span class="sxs-lookup"><span data-stu-id="5571b-104">The **SET** structure defines a set of values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5571b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5571b-105">Syntax</span></span>


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a><span data-ttu-id="5571b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5571b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5571b-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="5571b-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-108">Nombre total d’entrées dans un jeu.</span><span class="sxs-lookup"><span data-stu-id="5571b-108">Total number of entries in a set.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-109">**lpByteTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-109">**lpByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-110">Pointeur vers un tableau de valeurs d’octets.</span><span class="sxs-lookup"><span data-stu-id="5571b-110">Pointer to an array of BYTE values.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-111">**lpWordTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-111">**lpWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-112">Pointeur vers un tableau de valeurs de mot.</span><span class="sxs-lookup"><span data-stu-id="5571b-112">Pointer to an array of WORD values.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-113">**lpDwordTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-113">**lpDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-114">Pointeur vers un tableau de valeurs DWORD.</span><span class="sxs-lookup"><span data-stu-id="5571b-114">Pointer to an array of DWORD values.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-115">**lpLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-115">**lpLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-116">Pointeur vers un tableau de structures [LARGEINT](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="5571b-116">Pointer to an array of [LARGEINT](largeint.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-117">**lpSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-117">**lpSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-118">Pointeur vers un tableau de valeurs SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="5571b-118">Pointer to an array of SYSTEMTIME values.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-119">**lpLabeledByteTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-119">**lpLabeledByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-120">Pointeur vers un tableau de structures d' [ \_ octets étiquetées](labeled-byte.md) .</span><span class="sxs-lookup"><span data-stu-id="5571b-120">Pointer to an array of [LABELED\_BYTE](labeled-byte.md) structures.</span></span> <span data-ttu-id="5571b-121">Chaque structure d' **\_ octets étiquetée** définit une valeur et une étiquette.</span><span class="sxs-lookup"><span data-stu-id="5571b-121">Each **LABELED\_BYTE** structure defines a value and label.</span></span> <span data-ttu-id="5571b-122">Moniteur réseau affiche une étiquette s’il trouve une valeur correspondante dans le paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="5571b-122">Network Monitor displays a label if it finds a corresponding value in the protocol packet.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-123">**lpLabeledWordTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-123">**lpLabeledWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-124">Pointeur vers un tableau de structures de [ \_ mots étiquetées](labeled-word.md) qui définissent un ensemble de valeurs de mots et d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="5571b-124">Pointer to an array of [LABELED\_WORD](labeled-word.md) structures that define a set of WORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-125">**lpLabeledDwordTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-125">**lpLabeledDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-126">Pointeur vers un tableau de [structures \_ DWORD étiquetées](labeled-dword.md) qui définissent un ensemble de valeurs et d’étiquettes DWORD.</span><span class="sxs-lookup"><span data-stu-id="5571b-126">Pointer to an array of [LABELED\_DWORD](labeled-dword.md) structures that define a set of DWORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-127">**lpLabeledLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-127">**lpLabeledLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-128">Pointeur vers un tableau de [structures \_ LARGEINT étiquetées](labeled-largeint.md) qui définissent un ensemble de valeurs et d’étiquettes LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="5571b-128">Pointer to an array of [LABELED\_LARGEINT](labeled-largeint.md) structures that define a set of LARGEINT values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-129">**lpLabeledSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-129">**lpLabeledSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-130">Pointeur vers un tableau de [structures \_ SystemTime étiquetées](labeled-systemtime.md) qui définissent un ensemble de valeurs système et d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="5571b-130">Pointer to an array of [LABELED\_SYSTEMTIME](labeled-systemtime.md) structures that define a set of SYSTEM values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-131">**lpLabeledBit**</span><span class="sxs-lookup"><span data-stu-id="5571b-131">**lpLabeledBit**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-132">Pointeur vers un tableau de [structures \_ binaires étiquetées](labeled-bit.md) qui définissent un jeu de paires de bits étiquetées.</span><span class="sxs-lookup"><span data-stu-id="5571b-132">Pointer to an array of [LABELED\_BIT](labeled-bit.md) structures that define a set of labeled BIT pairs.</span></span> <span data-ttu-id="5571b-133">Chaque BIT peut spécifier deux étiquettes, une étiquette pour chaque État (0 ou 1) du BIT.</span><span class="sxs-lookup"><span data-stu-id="5571b-133">Each BIT can specify two labels   one label for each state (0 or 1) of the BIT.</span></span>

</dd> <dt>

<span data-ttu-id="5571b-134">**lpVoidTable**</span><span class="sxs-lookup"><span data-stu-id="5571b-134">**lpVoidTable**</span></span>
</dt> <dd>

<span data-ttu-id="5571b-135">Pointeur vers un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="5571b-135">Pointer to an array of values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5571b-136">Notes</span><span class="sxs-lookup"><span data-stu-id="5571b-136">Remarks</span></span>

<span data-ttu-id="5571b-137">La structure **Set** est utilisée pour définir un ensemble de données de comparaison que Moniteur réseau pouvez utiliser pour interpréter la valeur d’une propriété dans un paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="5571b-137">The **SET** structure is used to define a set of comparison data that Network Monitor can use to interpret the value of a property in a protocol packet.</span></span> <span data-ttu-id="5571b-138">Lorsqu’un jeu de données de comparaison est requis, un pointeur vers la structure **Set** est spécifié dans le membre **lpSet** de la structure [PROPERTYINFO](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5571b-138">When a set of comparison data is required, a pointer to the **SET** structure is specified in the **lpSet** member of the [PROPERTYINFO](propertyinfo.md) structure.</span></span>

<span data-ttu-id="5571b-139">La DLL de l’analyseur peut fournir un jeu de valeurs et un ensemble d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="5571b-139">The parser DLL can provide a value set and a label set.</span></span> <span data-ttu-id="5571b-140">Le membre de l' **Union** que vous sélectionnez dans une structure **Set** pointe vers un tableau de structures qui définissent chaque membre d’un jeu.</span><span class="sxs-lookup"><span data-stu-id="5571b-140">The member of the **UNION** that you select in a **SET** structure points to an array of structures that define each member of a set.</span></span>

-   <span data-ttu-id="5571b-141">Valeur définie</span><span class="sxs-lookup"><span data-stu-id="5571b-141">Value set</span></span>

    <span data-ttu-id="5571b-142">Un jeu de valeurs est utilisé lorsque vous souhaitez Moniteur réseau inclure un indicateur in-set ou not-in-set avec la valeur trouvée dans le paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="5571b-142">A value set is used when you want Network Monitor to include an in-set or not-in-set indicator with the value found in the protocol packet.</span></span> <span data-ttu-id="5571b-143">Par exemple, si un jeu de DWORDs est spécifié, Moniteur réseau affiche une étiquette pour chaque valeur DWORD trouvée dans le paquet de protocole, indiquant que la valeur DWORD est ou n’est pas spécifiée dans le jeu.</span><span class="sxs-lookup"><span data-stu-id="5571b-143">For example, if a DWORD set is specified, Network Monitor displays a label for each DWORD value found in the protocol packet, indicating that the DWORD is or is not specified in the set.</span></span>

    <span data-ttu-id="5571b-144">Un jeu de valeurs peut être basé sur des types de données BYTE, WORD, DWORD, LARGEINT et SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="5571b-144">A value set can be based on BYTE, WORD, DWORD, LARGEINT, and SYSTEMTIME data types.</span></span>

-   <span data-ttu-id="5571b-145">Ensemble d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="5571b-145">Label set</span></span>

    <span data-ttu-id="5571b-146">Un jeu d’étiquettes est utilisé lorsque vous souhaitez Moniteur réseau afficher une étiquette définie par l’utilisateur au lieu des valeurs de propriété spécifiées dans un jeu.</span><span class="sxs-lookup"><span data-stu-id="5571b-146">A label set is used when you want Network Monitor to display a user-defined label instead of the property values specified in a set.</span></span>

    <span data-ttu-id="5571b-147">Un jeu d’étiquettes peut être basé sur des paires d’étiquettes BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME et BIT.</span><span class="sxs-lookup"><span data-stu-id="5571b-147">A label set can be based on BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME and BIT label pairs.</span></span>

## <a name="requirements"></a><span data-ttu-id="5571b-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5571b-148">Requirements</span></span>



| <span data-ttu-id="5571b-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5571b-149">Requirement</span></span> | <span data-ttu-id="5571b-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="5571b-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5571b-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5571b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="5571b-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5571b-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5571b-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5571b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="5571b-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5571b-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5571b-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="5571b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="5571b-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5571b-156"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5571b-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5571b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5571b-158">\_bit étiqueté</span><span class="sxs-lookup"><span data-stu-id="5571b-158">LABELED\_BIT</span></span>](labeled-bit.md)
</dt> <dt>

[<span data-ttu-id="5571b-159">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="5571b-159">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




