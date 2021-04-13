---
title: Macro MCI_TMSF_MINUTE (Mciapi. h)
description: La \_ macro MCI TMSF \_ minute récupère le composant minutes à partir d’un paramètre contenant les informations de pistes compressées/minutes/secondes/images (TMSF).
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- MCI_TMSF_MINUTE macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69a12c2622f3f97f04bdca89389c8ab9be7e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508601"
---
# <a name="mci_tmsf_minute-macro"></a><span data-ttu-id="c7302-104">\_Macro MCI TMSF \_ minute</span><span class="sxs-lookup"><span data-stu-id="c7302-104">MCI\_TMSF\_MINUTE macro</span></span>

<span data-ttu-id="c7302-105">La macro **MCI \_ TMSF \_ minute** récupère le composant minutes à partir d’un paramètre contenant les informations de pistes compressées/minutes/secondes/images (TMSF).</span><span class="sxs-lookup"><span data-stu-id="c7302-105">The **MCI\_TMSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7302-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7302-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_MINUTE(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="c7302-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7302-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7302-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="c7302-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="c7302-109">Heure au format TMSF.</span><span class="sxs-lookup"><span data-stu-id="c7302-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7302-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7302-110">Return value</span></span>

<span data-ttu-id="c7302-111">Retourne le composant « minutes » des informations de TMSF spécifiées.</span><span class="sxs-lookup"><span data-stu-id="c7302-111">Returns the minutes component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7302-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c7302-112">Remarks</span></span>

<span data-ttu-id="c7302-113">L’heure au format TMSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les pistes, le prochain octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et l’octet le plus significatif contenant les frames.</span><span class="sxs-lookup"><span data-stu-id="c7302-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="c7302-114">La macro **MCI \_ TMSF \_ minute** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="c7302-114">The **MCI\_TMSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="c7302-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7302-115">Requirements</span></span>



| <span data-ttu-id="c7302-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7302-116">Requirement</span></span> | <span data-ttu-id="c7302-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7302-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7302-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7302-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7302-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7302-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c7302-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7302-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7302-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7302-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c7302-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7302-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7302-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7302-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7302-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7302-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7302-125">MCI</span><span class="sxs-lookup"><span data-stu-id="c7302-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c7302-126">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="c7302-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





