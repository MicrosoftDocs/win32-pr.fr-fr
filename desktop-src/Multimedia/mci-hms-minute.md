---
title: Macro MCI_HMS_MINUTE (Mciapi. h)
description: La \_ macro MCI HMS \_ minute récupère le composant minutes à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106210"
---
# <a name="mci_hms_minute-macro"></a><span data-ttu-id="da74b-104">\_Macro MCI HMS \_ minute</span><span class="sxs-lookup"><span data-stu-id="da74b-104">MCI\_HMS\_MINUTE macro</span></span>

<span data-ttu-id="da74b-105">La macro **MCI \_ HMS \_ minute** récupère le composant minutes à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.</span><span class="sxs-lookup"><span data-stu-id="da74b-105">The **MCI\_HMS\_MINUTE** macro retrieves the minutes component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="da74b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da74b-106">Syntax</span></span>


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="da74b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da74b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da74b-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="da74b-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="da74b-109">Heure au format HMS.</span><span class="sxs-lookup"><span data-stu-id="da74b-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da74b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da74b-110">Return value</span></span>

<span data-ttu-id="da74b-111">Retourne le composant « minutes » des informations de HMS spécifiées.</span><span class="sxs-lookup"><span data-stu-id="da74b-111">Returns the minutes component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="da74b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="da74b-112">Remarks</span></span>

<span data-ttu-id="da74b-113">L’heure au format HMS est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les heures, le prochain octet le moins significatif contenant les minutes et le prochain octet le moins significatif contenant les secondes.</span><span class="sxs-lookup"><span data-stu-id="da74b-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="da74b-114">L’octet le plus significatif n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="da74b-114">The most significant byte is unused.</span></span>

<span data-ttu-id="da74b-115">La macro **MCI \_ HMS \_ minute** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="da74b-115">The **MCI\_HMS\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="da74b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da74b-116">Requirements</span></span>



| <span data-ttu-id="da74b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da74b-117">Requirement</span></span> | <span data-ttu-id="da74b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="da74b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da74b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da74b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da74b-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da74b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="da74b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da74b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da74b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da74b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="da74b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="da74b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="da74b-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da74b-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da74b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da74b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da74b-126">MCI</span><span class="sxs-lookup"><span data-stu-id="da74b-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="da74b-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="da74b-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





