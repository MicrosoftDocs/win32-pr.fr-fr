---
title: Macro MCI_MAKE_MSF (Mciapi. h)
description: La \_ macro MCI make \_ crée une valeur d’heure en minutes compactées/secondes/images (MSF) à partir des valeurs de minutes, de secondes et de frames données.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942821"
---
# <a name="mci_make_msf-macro"></a><span data-ttu-id="52289-104">\_Créer une \_ macro pour MCI</span><span class="sxs-lookup"><span data-stu-id="52289-104">MCI\_MAKE\_MSF macro</span></span>

<span data-ttu-id="52289-105">La macro **MCI make crée une \_ \_** valeur d’heure en minutes compactées/secondes/images (MSF) à partir des valeurs de minutes, de secondes et de frames données.</span><span class="sxs-lookup"><span data-stu-id="52289-105">The **MCI\_MAKE\_MSF** macro creates a time value in packed minutes/seconds/frames (MSF) format from the given minutes, seconds, and frame values.</span></span>

## <a name="syntax"></a><span data-ttu-id="52289-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52289-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="52289-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52289-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52289-108">*minutes*</span><span class="sxs-lookup"><span data-stu-id="52289-108">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="52289-109">Nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="52289-109">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="52289-110">*secondes*</span><span class="sxs-lookup"><span data-stu-id="52289-110">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="52289-111">Nombre de secondes.</span><span class="sxs-lookup"><span data-stu-id="52289-111">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="52289-112">*cadres*</span><span class="sxs-lookup"><span data-stu-id="52289-112">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="52289-113">Nombre de frames.</span><span class="sxs-lookup"><span data-stu-id="52289-113">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52289-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52289-114">Return value</span></span>

<span data-ttu-id="52289-115">Retourne l’heure au format MSF compressé.</span><span class="sxs-lookup"><span data-stu-id="52289-115">Returns the time in packed MSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="52289-116">Notes</span><span class="sxs-lookup"><span data-stu-id="52289-116">Remarks</span></span>

<span data-ttu-id="52289-117">L’heure au format MSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et le prochain octet le moins significatif contenant les frames.</span><span class="sxs-lookup"><span data-stu-id="52289-117">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="52289-118">L’octet le plus significatif n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="52289-118">The most significant byte is unused.</span></span>

<span data-ttu-id="52289-119">La **macro \_ MCI \_ Make** do est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="52289-119">The **MCI\_MAKE\_MSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="52289-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52289-120">Requirements</span></span>



| <span data-ttu-id="52289-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52289-121">Requirement</span></span> | <span data-ttu-id="52289-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="52289-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52289-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52289-123">Minimum supported client</span></span><br/> | <span data-ttu-id="52289-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52289-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="52289-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52289-125">Minimum supported server</span></span><br/> | <span data-ttu-id="52289-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52289-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52289-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="52289-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="52289-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52289-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52289-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52289-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52289-130">MCI</span><span class="sxs-lookup"><span data-stu-id="52289-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="52289-131">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="52289-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





