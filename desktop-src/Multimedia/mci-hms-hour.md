---
title: Macro MCI_HMS_HOUR (Mciapi. h)
description: La \_ macro MCI HMS \_ Hour récupère le composant heures à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033239"
---
# <a name="mci_hms_hour-macro"></a><span data-ttu-id="7848f-104">HMS de la \_ \_ macro d’heure MCI</span><span class="sxs-lookup"><span data-stu-id="7848f-104">MCI\_HMS\_HOUR macro</span></span>

<span data-ttu-id="7848f-105">La macro **MCI \_ HMS \_ Hour** récupère le composant heures à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.</span><span class="sxs-lookup"><span data-stu-id="7848f-105">The **MCI\_HMS\_HOUR** macro retrieves the hours component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7848f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7848f-106">Syntax</span></span>


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="7848f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7848f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7848f-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="7848f-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="7848f-109">Heure au format HMS.</span><span class="sxs-lookup"><span data-stu-id="7848f-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7848f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7848f-110">Return value</span></span>

<span data-ttu-id="7848f-111">Retourne le composant « heures » des informations de HMS spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7848f-111">Returns the hours component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="7848f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7848f-112">Remarks</span></span>

<span data-ttu-id="7848f-113">L’heure au format HMS est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les heures, le prochain octet le moins significatif contenant les minutes et le prochain octet le moins significatif contenant les secondes.</span><span class="sxs-lookup"><span data-stu-id="7848f-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="7848f-114">L’octet le plus significatif n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7848f-114">The most significant byte is unused.</span></span>

<span data-ttu-id="7848f-115">La macro **MCI \_ HMS \_ Hour** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="7848f-115">The **MCI\_HMS\_HOUR** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a><span data-ttu-id="7848f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7848f-116">Requirements</span></span>



| <span data-ttu-id="7848f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7848f-117">Requirement</span></span> | <span data-ttu-id="7848f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7848f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7848f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7848f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7848f-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7848f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7848f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7848f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7848f-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7848f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7848f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7848f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7848f-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7848f-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7848f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7848f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7848f-126">MCI</span><span class="sxs-lookup"><span data-stu-id="7848f-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7848f-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="7848f-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





