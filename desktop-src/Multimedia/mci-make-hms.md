---
title: Macro MCI_MAKE_HMS (Mciapi. h)
description: La \_ macro MCI make \_ HMS crée une valeur d’heure sous forme d’heures/minutes/secondes (HMS) à partir des valeurs d’heures, de minutes et de secondes fournies.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743141"
---
# <a name="mci_make_hms-macro"></a><span data-ttu-id="72d77-104">MCI \_ Make \_ HMS macro</span><span class="sxs-lookup"><span data-stu-id="72d77-104">MCI\_MAKE\_HMS macro</span></span>

<span data-ttu-id="72d77-105">La macro **MCI \_ Make \_ HMS** crée une valeur d’heure sous forme d’heures/minutes/secondes (HMS) à partir des valeurs d’heures, de minutes et de secondes fournies.</span><span class="sxs-lookup"><span data-stu-id="72d77-105">The **MCI\_MAKE\_HMS** macro creates a time value in packed hours/minutes/seconds (HMS) format from the given hours, minutes, and seconds values.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d77-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72d77-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a><span data-ttu-id="72d77-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d77-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d77-108">*hours*</span><span class="sxs-lookup"><span data-stu-id="72d77-108">*hours*</span></span> 
</dt> <dd>

<span data-ttu-id="72d77-109">Nombre d'heures.</span><span class="sxs-lookup"><span data-stu-id="72d77-109">Number of hours.</span></span>

</dd> <dt>

<span data-ttu-id="72d77-110">*minutes*</span><span class="sxs-lookup"><span data-stu-id="72d77-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="72d77-111">Nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="72d77-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="72d77-112">*secondes*</span><span class="sxs-lookup"><span data-stu-id="72d77-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="72d77-113">Nombre de secondes.</span><span class="sxs-lookup"><span data-stu-id="72d77-113">Number of seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d77-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72d77-114">Return value</span></span>

<span data-ttu-id="72d77-115">Retourne l’heure au format compressé HMS.</span><span class="sxs-lookup"><span data-stu-id="72d77-115">Returns the time in packed HMS format.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d77-116">Notes</span><span class="sxs-lookup"><span data-stu-id="72d77-116">Remarks</span></span>

<span data-ttu-id="72d77-117">L’heure au format HMS est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les heures, le prochain octet le moins significatif contenant les minutes et le prochain octet le moins significatif contenant les secondes.</span><span class="sxs-lookup"><span data-stu-id="72d77-117">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="72d77-118">L’octet le plus significatif n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="72d77-118">The most significant byte is unused.</span></span>

<span data-ttu-id="72d77-119">La macro **MCI \_ Make \_ HMS** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="72d77-119">The **MCI\_MAKE\_HMS** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="72d77-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d77-120">Requirements</span></span>



| <span data-ttu-id="72d77-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d77-121">Requirement</span></span> | <span data-ttu-id="72d77-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d77-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72d77-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d77-123">Minimum supported client</span></span><br/> | <span data-ttu-id="72d77-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d77-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="72d77-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d77-125">Minimum supported server</span></span><br/> | <span data-ttu-id="72d77-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d77-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="72d77-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="72d77-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d77-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d77-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d77-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d77-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d77-130">MCI</span><span class="sxs-lookup"><span data-stu-id="72d77-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="72d77-131">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="72d77-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





