---
description: La fonction GetCaptureTimeStamp retourne la date et l’heure de début de l’enregistrement des trames par la capture.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: GetCaptureTimeStamp, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525138"
---
# <a name="getcapturetimestamp-function"></a><span data-ttu-id="998fa-103">GetCaptureTimeStamp fonction)</span><span class="sxs-lookup"><span data-stu-id="998fa-103">GetCaptureTimeStamp function</span></span>

<span data-ttu-id="998fa-104">La fonction **GetCaptureTimeStamp** retourne la date et l’heure de début de l’enregistrement des trames par la capture.</span><span class="sxs-lookup"><span data-stu-id="998fa-104">The **GetCaptureTimeStamp** function returns the time and date when the capture started recording frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="998fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="998fa-105">Syntax</span></span>


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="998fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="998fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998fa-107">*hCapture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="998fa-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="998fa-108">Handle de la capture.</span><span class="sxs-lookup"><span data-stu-id="998fa-108">Handle to the capture.</span></span> <span data-ttu-id="998fa-109">Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="998fa-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTimeStamp** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="998fa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="998fa-110">Return value</span></span>

<span data-ttu-id="998fa-111">Si la fonction réussit, la valeur de retour est un pointeur vers une structure [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="998fa-111">If the function is successful, the return value is a pointer to a [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

<span data-ttu-id="998fa-112">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="998fa-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="998fa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="998fa-113">Remarks</span></span>

<span data-ttu-id="998fa-114">La fonction **GetCaptureTimeStamp** retourne l’heure à laquelle le fournisseur de paquets réseau (NPP) commence à collecter des données, et non lorsque l’expert charge la capture pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="998fa-114">The **GetCaptureTimeStamp** function returns the time when the Network Packet Provider (NPP) starts collecting data, not when the expert loads the capture for analysis.</span></span>

<span data-ttu-id="998fa-115">Ne remplacez pas les données dans la structure **SystemTime** .</span><span class="sxs-lookup"><span data-stu-id="998fa-115">Do not overwrite the data in the **SYSTEMTIME** structure.</span></span> <span data-ttu-id="998fa-116">Les données font partie de la capture.</span><span class="sxs-lookup"><span data-stu-id="998fa-116">The data is part of the capture.</span></span> <span data-ttu-id="998fa-117">Toute tentative de modification des données entraîne une violation d’accès.</span><span class="sxs-lookup"><span data-stu-id="998fa-117">Trying to modify the data causes an access violation.</span></span>

<span data-ttu-id="998fa-118">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="998fa-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="998fa-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="998fa-119">Requirements</span></span>



| <span data-ttu-id="998fa-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="998fa-120">Requirement</span></span> | <span data-ttu-id="998fa-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="998fa-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="998fa-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="998fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="998fa-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="998fa-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="998fa-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="998fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="998fa-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="998fa-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="998fa-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="998fa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="998fa-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="998fa-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="998fa-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="998fa-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="998fa-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="998fa-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="998fa-130">DLL</span><span class="sxs-lookup"><span data-stu-id="998fa-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="998fa-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="998fa-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="998fa-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="998fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998fa-133">SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="998fa-133">SYSTEMTIME</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

