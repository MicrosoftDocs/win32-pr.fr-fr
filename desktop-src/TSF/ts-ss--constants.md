---
title: Constantes TS_SS_ (Textstor. h)
description: Les \_ \_ constantes TS SS \, définies avant l’exécution dans la \_ structure d’État TS, décrivent les États des documents statiques.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512545"
---
# <a name="ts_ss_-constants"></a><span data-ttu-id="79f0c-103">\_ \_ \* Constantes TS SS</span><span class="sxs-lookup"><span data-stu-id="79f0c-103">TS\_SS\_\* Constants</span></span>

<span data-ttu-id="79f0c-104">Les \_ \_ \* constantes TS SS, définies avant l’exécution dans la structure d' [**\_ État TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , décrivent les États des documents statiques.</span><span class="sxs-lookup"><span data-stu-id="79f0c-104">The TS\_SS\_\* constants, defined before run time in the [**TS\_STATUS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure, describe static document states.</span></span>



| <span data-ttu-id="79f0c-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="79f0c-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="79f0c-106">Description</span><span class="sxs-lookup"><span data-stu-id="79f0c-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <span data-ttu-id="79f0c-107"><dt>**TS \_ SS \_ DISJOINTSEL**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-107"><dt>**TS\_SS\_DISJOINTSEL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                             | <span data-ttu-id="79f0c-108">Le document prend en charge les sélections multiples.</span><span class="sxs-lookup"><span data-stu-id="79f0c-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <span data-ttu-id="79f0c-109"><dt>**TS \_ \_Zones SS**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-109"><dt>**TS\_SS\_REGIONS**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                         | <span data-ttu-id="79f0c-110">Le document peut contenir plusieurs régions.</span><span class="sxs-lookup"><span data-stu-id="79f0c-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <span data-ttu-id="79f0c-111"><dt>**TS \_ SS \_ transitoire**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-111"><dt>**TS\_SS\_TRANSITORY**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                | <span data-ttu-id="79f0c-112">Le document est supposé avoir un cycle d’utilisation courts.</span><span class="sxs-lookup"><span data-stu-id="79f0c-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <span data-ttu-id="79f0c-113"><dt>**TS \_ SS \_ NOHIDDENTEXT**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-113"><dt>**TS\_SS\_NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt></span></span> </dl>                          | <span data-ttu-id="79f0c-114">Le document ne contient jamais de texte masqué.</span><span class="sxs-lookup"><span data-stu-id="79f0c-114">The document will never contain hidden text.</span></span><br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="79f0c-115"><dt>**TS \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-115"><dt>**TS\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt></span></span> </dl> | <span data-ttu-id="79f0c-116">**À compter de Windows 8 :** Le document prend en charge la correction automatique fournie par le clavier tactile.</span><span class="sxs-lookup"><span data-stu-id="79f0c-116">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="79f0c-117"><dt>**TS \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-117"><dt>**TS\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt></span></span> </dl>    | <span data-ttu-id="79f0c-118">**À compter de Windows 8 :** Le document prend en charge les suggestions de texte fournies par le clavier tactile.</span><span class="sxs-lookup"><span data-stu-id="79f0c-118">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="79f0c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="79f0c-119">Remarks</span></span>

<span data-ttu-id="79f0c-120">Le membre **dwStaticFlags** de la structure d' **\_ État TS** utilise ces constantes.</span><span class="sxs-lookup"><span data-stu-id="79f0c-120">The **dwStaticFlags** member of the **TS\_STATUS** structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="79f0c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79f0c-121">Requirements</span></span>



| <span data-ttu-id="79f0c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79f0c-122">Requirement</span></span> | <span data-ttu-id="79f0c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="79f0c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79f0c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79f0c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79f0c-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79f0c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="79f0c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79f0c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79f0c-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79f0c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79f0c-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="79f0c-128">Redistributable</span></span><br/>          | <span data-ttu-id="79f0c-129">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="79f0c-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="79f0c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="79f0c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="79f0c-131"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-131"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="79f0c-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="79f0c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79f0c-133"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79f0c-133"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f0c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79f0c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f0c-135">**\_statut TS**</span><span class="sxs-lookup"><span data-stu-id="79f0c-135">**TS\_STATUS**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

<span data-ttu-id="79f0c-136">[**\_État TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79f0c-136">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

