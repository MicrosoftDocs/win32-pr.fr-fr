---
description: La fonction GetFrame retourne un handle à un frame donné dans une capture.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: GetFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112226"
---
# <a name="getframe-function"></a><span data-ttu-id="cd103-103">GetFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="cd103-103">GetFrame function</span></span>

<span data-ttu-id="cd103-104">La fonction **GetFrame** retourne un handle à un frame donné dans une capture.</span><span class="sxs-lookup"><span data-stu-id="cd103-104">The **GetFrame** function returns a handle to a given frame within a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd103-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd103-105">Syntax</span></span>


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a><span data-ttu-id="cd103-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd103-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd103-107">*hCapture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd103-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd103-108">Handle vers une capture.</span><span class="sxs-lookup"><span data-stu-id="cd103-108">Handle to a capture.</span></span> <span data-ttu-id="cd103-109">Pour obtenir le handle de capture, appelez la fonction [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="cd103-109">To obtain the capture handle, call the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cd103-110">*FrameNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd103-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd103-111">Nombre (de base zéro) du frame.</span><span class="sxs-lookup"><span data-stu-id="cd103-111">Number (zero-based) of the frame.</span></span> <span data-ttu-id="cd103-112">Le numéro de la première trame dans une capture est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cd103-112">The number of the first frame in a capture is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd103-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd103-113">Return value</span></span>

<span data-ttu-id="cd103-114">Si la fonction réussit, la valeur de retour est un handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="cd103-114">If the function is successful, the return value is a handle to the frame.</span></span>

<span data-ttu-id="cd103-115">Si la fonction échoue (autrement dit, si *hCapture* n’est pas valide ou si le numéro de frame est hors limites), la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="cd103-115">If the function is unsuccessful (that is, if *hCapture* is invalid, or the frame number is out of range), the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd103-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cd103-116">Remarks</span></span>

<span data-ttu-id="cd103-117">Utilisez la fonction **GetFrame** pour obtenir le descripteur de frame nécessaire lors de la localisation des instances d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="cd103-117">Use the **GetFrame** function to obtain the frame handle needed when locating instances of a property.</span></span> <span data-ttu-id="cd103-118">Les fonctions utilisées pour localiser des instances de propriété sont des [FindPropertyInstance](findpropertyinstance.md) qui localisent la première instance et [FindPropertyInstanceRestart](findpropertyinstancerestart.md) qui localise l’instance suivante.</span><span class="sxs-lookup"><span data-stu-id="cd103-118">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) which locates the first instance, and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) which locates the next instance.</span></span>

<span data-ttu-id="cd103-119">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrame** .</span><span class="sxs-lookup"><span data-stu-id="cd103-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd103-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd103-120">Requirements</span></span>



| <span data-ttu-id="cd103-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd103-121">Requirement</span></span> | <span data-ttu-id="cd103-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd103-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd103-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd103-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cd103-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd103-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd103-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd103-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cd103-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd103-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd103-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd103-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd103-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd103-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cd103-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd103-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd103-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd103-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd103-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cd103-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd103-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd103-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd103-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd103-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd103-134">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="cd103-134">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="cd103-135">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="cd103-135">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




