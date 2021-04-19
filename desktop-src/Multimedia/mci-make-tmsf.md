---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: La \_ macro MCI make \_ TMSF crée une valeur d’heure sous forme de pistes compressées/minutes/secondes/images (TMSF) à partir des valeurs de suivi, de minutes, de secondes et de frames données.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536080"
---
# <a name="mci_make_tmsf-macro"></a><span data-ttu-id="d7ea9-104">MCI \_ Make \_ TMSF macro</span><span class="sxs-lookup"><span data-stu-id="d7ea9-104">MCI\_MAKE\_TMSF macro</span></span>

<span data-ttu-id="d7ea9-105">La macro **MCI \_ Make \_ TMSF** crée une valeur d’heure sous forme de pistes compressées/minutes/secondes/images (TMSF) à partir des valeurs de suivi, de minutes, de secondes et de frames données.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-105">The **MCI\_MAKE\_TMSF** macro creates a time value in packed tracks/minutes/seconds/frames (TMSF) format from the given tracks, minutes, seconds, and frames values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ea9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7ea9-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="d7ea9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7ea9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ea9-108">*tracks*</span><span class="sxs-lookup"><span data-stu-id="d7ea9-108">*tracks*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ea9-109">Nombre de pistes.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-109">Number of tracks.</span></span>

</dd> <dt>

<span data-ttu-id="d7ea9-110">*minutes*</span><span class="sxs-lookup"><span data-stu-id="d7ea9-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ea9-111">Nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="d7ea9-112">*secondes*</span><span class="sxs-lookup"><span data-stu-id="d7ea9-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ea9-113">Nombre de secondes.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-113">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d7ea9-114">*cadres*</span><span class="sxs-lookup"><span data-stu-id="d7ea9-114">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ea9-115">Nombre de frames.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-115">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ea9-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7ea9-116">Return value</span></span>

<span data-ttu-id="d7ea9-117">Retourne l’heure au format compressé TMSF.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-117">Returns the time in packed TMSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ea9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d7ea9-118">Remarks</span></span>

<span data-ttu-id="d7ea9-119">L’heure au format TMSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les pistes, le prochain octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et l’octet le plus significatif contenant les frames.</span><span class="sxs-lookup"><span data-stu-id="d7ea9-119">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="d7ea9-120">La macro **MCI \_ Make \_ TMSF** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="d7ea9-120">The **MCI\_MAKE\_TMSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="d7ea9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7ea9-121">Requirements</span></span>



| <span data-ttu-id="d7ea9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7ea9-122">Requirement</span></span> | <span data-ttu-id="d7ea9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7ea9-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ea9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ea9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ea9-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7ea9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d7ea9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ea9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ea9-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7ea9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d7ea9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7ea9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ea9-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ea9-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ea9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7ea9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ea9-131">MCI</span><span class="sxs-lookup"><span data-stu-id="d7ea9-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d7ea9-132">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="d7ea9-132">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





