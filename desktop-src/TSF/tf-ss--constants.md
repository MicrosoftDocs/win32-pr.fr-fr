---
title: Constantes TF_SS_ (msctf. h)
description: Les \_ \_ constantes TF SS \, définies avant l’exécution dans la \_ structure d’État TF, décrivent les États des documents statiques.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032964"
---
# <a name="tf_ss_-constants"></a><span data-ttu-id="21680-103">\_ \_ \* Constantes TF SS</span><span class="sxs-lookup"><span data-stu-id="21680-103">TF\_SS\_\* Constants</span></span>

<span data-ttu-id="21680-104">Les \_ \_ \* constantes TF SS, définies avant l’exécution dans la structure d' [**\_ État TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , décrivent les États des documents statiques.</span><span class="sxs-lookup"><span data-stu-id="21680-104">The TF\_SS\_\* constants, defined before run time in the [**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure, describe static document states.</span></span>



| <span data-ttu-id="21680-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="21680-105">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="21680-106">Description</span><span class="sxs-lookup"><span data-stu-id="21680-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <span data-ttu-id="21680-107"><dt>**Tf \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt></span><span class="sxs-lookup"><span data-stu-id="21680-107"><dt>**TF\_SS\_DISJOINTSEL**</dt> <dt>( TS\_SS\_DISJOINTSEL )</dt></span></span> </dl>                                     | <span data-ttu-id="21680-108">Le document prend en charge les sélections multiples.</span><span class="sxs-lookup"><span data-stu-id="21680-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <span data-ttu-id="21680-109"><dt>**Tf \_ \_zones SS**</dt> <dt>(zones de sécurité Terminal Server \_ \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="21680-109"><dt>**TF\_SS\_REGIONS**</dt> <dt>( TS\_SS\_REGIONS )</dt></span></span> </dl>                                                     | <span data-ttu-id="21680-110">Le document peut contenir plusieurs régions.</span><span class="sxs-lookup"><span data-stu-id="21680-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <span data-ttu-id="21680-111"><dt>**Tf \_ SS \_ transitoire**</dt> <dt>(TS \_ SS \_ transitif)</dt></span><span class="sxs-lookup"><span data-stu-id="21680-111"><dt>**TF\_SS\_TRANSITORY**</dt> <dt>( TS\_SS\_TRANSITORY )</dt></span></span> </dl>                                         | <span data-ttu-id="21680-112">Le document est supposé avoir un cycle d’utilisation courts.</span><span class="sxs-lookup"><span data-stu-id="21680-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="21680-113"><dt>**Tf \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="21680-113"><dt>**TF\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( TS\_SS\_TKBAUTOCORRECTENABLE )</dt></span></span> </dl> | <span data-ttu-id="21680-114">**À compter de Windows 8 :** Le document prend en charge la correction automatique fournie par le clavier tactile.</span><span class="sxs-lookup"><span data-stu-id="21680-114">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="21680-115"><dt>**Tf \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="21680-115"><dt>**TF\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( TS\_SS\_TKBPREDICTIONENABLE )</dt></span></span> </dl>     | <span data-ttu-id="21680-116">**À compter de Windows 8 :** Le document prend en charge les suggestions de texte fournies par le clavier tactile.</span><span class="sxs-lookup"><span data-stu-id="21680-116">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="21680-117">Notes</span><span class="sxs-lookup"><span data-stu-id="21680-117">Remarks</span></span>

<span data-ttu-id="21680-118">Le membre **dwStaticFlags** de la \_ structure d’État TF utilise ces constantes.</span><span class="sxs-lookup"><span data-stu-id="21680-118">The **dwStaticFlags** member of the TF\_STATUS structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="21680-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21680-119">Requirements</span></span>



| <span data-ttu-id="21680-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21680-120">Requirement</span></span> | <span data-ttu-id="21680-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="21680-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21680-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21680-122">Minimum supported client</span></span><br/> | <span data-ttu-id="21680-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21680-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="21680-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21680-124">Minimum supported server</span></span><br/> | <span data-ttu-id="21680-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21680-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="21680-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="21680-126">Redistributable</span></span><br/>          | <span data-ttu-id="21680-127">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="21680-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="21680-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="21680-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="21680-129"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="21680-129"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="21680-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="21680-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21680-131"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21680-131"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21680-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21680-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="21680-133">[**\_État TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21680-133">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

