---
description: La structure CAPTUREFILTER contient des données de filtre de capture.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: CAPTUREFILTER, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529280"
---
# <a name="capturefilter-structure"></a><span data-ttu-id="f4cbb-103">CAPTUREFILTER, structure</span><span class="sxs-lookup"><span data-stu-id="f4cbb-103">CAPTUREFILTER structure</span></span>

<span data-ttu-id="f4cbb-104">La structure **capturefilter** contient des données de filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-104">The **CAPTUREFILTER** structure contains capture filter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4cbb-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a><span data-ttu-id="f4cbb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f4cbb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4cbb-107">**FilterFlags**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-107">**FilterFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-108">Indicateurs qui décrivent le contenu du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-108">Flags that describe the contents of the capture filter.</span></span>



| <span data-ttu-id="f4cbb-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4cbb-109">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="f4cbb-110">Signification</span><span class="sxs-lookup"><span data-stu-id="f4cbb-110">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <span data-ttu-id="f4cbb-111"><dt>**Capturefilter \_ \_Les indicateurs incluent \_ tous les \_ SAP**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f4cbb-111"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS**</dt> <dt>0x0001</dt></span></span> </dl>       | <span data-ttu-id="f4cbb-112">Comprend tous les SAP comme des trames acceptables.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-112">Includes all SAPs as acceptable frames.</span></span><br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <span data-ttu-id="f4cbb-113"><dt>**Capturefilter \_ \_Les indicateurs incluent \_ tous les \_ ETYPE**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f4cbb-113"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="f4cbb-114">Inclure tous les ETYPE comme trames acceptables.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-114">Include all Etypes as acceptable frames.</span></span><br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <span data-ttu-id="f4cbb-115"><dt>**Capturefilter \_ INDICATEURS \_ locaux \_ uniquement**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="f4cbb-115"><dt>**CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY**</dt> <dt>0x0008</dt></span></span> </dl>                          | <span data-ttu-id="f4cbb-116">Aucun mode P</span><span class="sxs-lookup"><span data-stu-id="f4cbb-116">No P-mode</span></span><br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <span data-ttu-id="f4cbb-117"><dt>**Capturefilter \_ INDICATEURS \_ Keep \_ RAW**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="f4cbb-117"><dt>**CAPTUREFILTER\_FLAGS\_KEEP\_RAW**</dt> <dt>0x0020</dt></span></span> </dl>                                | <span data-ttu-id="f4cbb-118">Conservez les trames SMT et Token Ring MAC.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-118">Keep SMT and token ring MAC frames.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="f4cbb-119">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-119">**lpSapTable**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-120">Pointeur vers un tableau de valeurs SAP.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-120">Pointer to an array of SAP values.</span></span> <span data-ttu-id="f4cbb-121">Ce membre indique les valeurs SAP qui sont valides pour passer au pilote.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-121">This member indicates the SAP values that are valid to pass to the driver.</span></span> <span data-ttu-id="f4cbb-122">Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ SAP sont définis, cela devient une liste d’exceptions (y compris tous les SAP sauf ceux-ci).</span><span class="sxs-lookup"><span data-stu-id="f4cbb-122">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (include all SAPS except these).</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-123">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-123">**lpEtypeTable**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-124">Pointeur vers un tableau de valeurs ETYPE.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-124">Pointer to an array of Etype values.</span></span> <span data-ttu-id="f4cbb-125">Cela indique les valeurs ETYPE qui sont valides pour passer au pilote.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-125">This indicates those Etype values that are valid to pass to the driver.</span></span> <span data-ttu-id="f4cbb-126">Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ ETYPE sont définis, cela devient une liste d’exceptions (y compris tous les ETYPE, sauf celles-ci).</span><span class="sxs-lookup"><span data-stu-id="f4cbb-126">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (include all Etypes except these).</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-127">**nSaps**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-127">**nSaps**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-128">Nombre de SAP dans la table SAP.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-128">Number of SAPs in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-129">**nEtypes**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-129">**nEtypes**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-130">Nombre de ETYPE dans la table ETYPE.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-130">Number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-131">**AddressTable**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-131">**AddressTable**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-132">Nom de la table d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-132">Name of the address table.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-133">**FilterExpression**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-133">**FilterExpression**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-134">Structure d’EXPRESSION.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-134">An EXPRESSION structure.</span></span> <span data-ttu-id="f4cbb-135">Contient la partie de correspondance de modèle du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-135">This contains the pattern match portion of the capture filter.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-136">**Déclencheur**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-136">**Trigger**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-137">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-137">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-138">**nFrameBytesToCopy**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-138">**nFrameBytesToCopy**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-139">Si ce membre n’est pas égal à 0, il spécifie le nombre d’octets à conserver pour chaque trame reçue.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-139">If this member is not 0, then it specifies how many bytes to keep of each frame received.</span></span> <span data-ttu-id="f4cbb-140">Si la valeur est 0, conservez la totalité du frame.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-140">If it is 0, then keep the whole frame.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbb-141">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f4cbb-141">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbb-142">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-142">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4cbb-143">Notes</span><span class="sxs-lookup"><span data-stu-id="f4cbb-143">Remarks</span></span>

<span data-ttu-id="f4cbb-144">La combinaison d’indicateurs, de valeurs et d’expressions détermine les frames qui seront transmis par le pilote qui utilise ces données de structure.</span><span class="sxs-lookup"><span data-stu-id="f4cbb-144">The combination of flags, values, and expressions determine which frames will be passed by the driver that uses this structure data.</span></span> <span data-ttu-id="f4cbb-145">Pour plus d’informations sur l’implémentation d’une structure **capturefilter** , consultez [filtres de capture](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="f4cbb-145">For more information about implementing a **CAPTUREFILTER** structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4cbb-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4cbb-146">Requirements</span></span>



| <span data-ttu-id="f4cbb-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4cbb-147">Requirement</span></span> | <span data-ttu-id="f4cbb-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4cbb-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cbb-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4cbb-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f4cbb-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4cbb-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f4cbb-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4cbb-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f4cbb-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4cbb-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f4cbb-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4cbb-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4cbb-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4cbb-154"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4cbb-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4cbb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4cbb-156">ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="f4cbb-156">ADDRESSTABLE</span></span>](addresstable.md)
</dt> <dt>

[<span data-ttu-id="f4cbb-157">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="f4cbb-157">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="f4cbb-158">FORMULE</span><span class="sxs-lookup"><span data-stu-id="f4cbb-158">EXPRESSION</span></span>](expression.md)
</dt> <dt>

[<span data-ttu-id="f4cbb-159">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="f4cbb-159">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="f4cbb-160">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="f4cbb-160">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




