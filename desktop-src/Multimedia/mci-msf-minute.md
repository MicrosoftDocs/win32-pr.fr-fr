---
title: Macro MCI_MSF_MINUTE (Mciapi. h)
description: La \_ macro MCI MSF \_ minute récupère le composant minutes à partir d’un paramètre contenant les informations de minutes/secondes/frames (MSF) compressées.
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515482"
---
# <a name="mci_msf_minute-macro"></a><span data-ttu-id="36a7b-104">\_Macro MCI MSF \_ minute</span><span class="sxs-lookup"><span data-stu-id="36a7b-104">MCI\_MSF\_MINUTE macro</span></span>

<span data-ttu-id="36a7b-105">La macro **MCI \_ MSF \_ minute** récupère le composant minutes à partir d’un paramètre contenant les informations de minutes/secondes/frames (MSF) compressées.</span><span class="sxs-lookup"><span data-stu-id="36a7b-105">The **MCI\_MSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a7b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36a7b-106">Syntax</span></span>


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="36a7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36a7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a7b-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="36a7b-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="36a7b-109">Heure au format MSF.</span><span class="sxs-lookup"><span data-stu-id="36a7b-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36a7b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36a7b-110">Return value</span></span>

<span data-ttu-id="36a7b-111">Retourne le composant « minutes » des informations MSF spécifiées.</span><span class="sxs-lookup"><span data-stu-id="36a7b-111">Returns the minutes component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="36a7b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="36a7b-112">Remarks</span></span>

<span data-ttu-id="36a7b-113">L’heure au format MSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et le prochain octet le moins significatif contenant les frames.</span><span class="sxs-lookup"><span data-stu-id="36a7b-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="36a7b-114">L’octet le plus significatif n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="36a7b-114">The most significant byte is unused.</span></span>

<span data-ttu-id="36a7b-115">La macro **MCI \_ MSF \_ minute** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="36a7b-115">The **MCI\_MSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a><span data-ttu-id="36a7b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36a7b-116">Requirements</span></span>



| <span data-ttu-id="36a7b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36a7b-117">Requirement</span></span> | <span data-ttu-id="36a7b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="36a7b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36a7b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36a7b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36a7b-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36a7b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="36a7b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36a7b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36a7b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36a7b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36a7b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="36a7b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36a7b-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="36a7b-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a7b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36a7b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a7b-126">MCI</span><span class="sxs-lookup"><span data-stu-id="36a7b-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="36a7b-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="36a7b-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





