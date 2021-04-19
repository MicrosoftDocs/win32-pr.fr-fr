---
description: Retourne un pointeur vers le commentaire d’une capture.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: GetCaptureComment, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513976"
---
# <a name="getcapturecomment-function"></a><span data-ttu-id="08a2b-103">GetCaptureComment fonction)</span><span class="sxs-lookup"><span data-stu-id="08a2b-103">GetCaptureComment function</span></span>

<span data-ttu-id="08a2b-104">La fonction **GetCaptureComment** retourne un pointeur vers le commentaire d’une capture.</span><span class="sxs-lookup"><span data-stu-id="08a2b-104">The **GetCaptureComment** function returns a pointer to the comment of a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08a2b-105">Syntax</span></span>


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="08a2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08a2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a2b-107">*hCapture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08a2b-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a2b-108">Handle de la capture.</span><span class="sxs-lookup"><span data-stu-id="08a2b-108">A handle to the capture.</span></span> <span data-ttu-id="08a2b-109">Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="08a2b-109">For more information about obtaining the capture handle, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a2b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08a2b-110">Return value</span></span>

<span data-ttu-id="08a2b-111">Si la fonction réussit (autrement dit, si la capture contient un commentaire), la valeur de retour est un pointeur vers la chaîne de commentaire.</span><span class="sxs-lookup"><span data-stu-id="08a2b-111">If the function is successful (that is, if the capture contains a comment), the return value is a pointer to the comment string.</span></span>

<span data-ttu-id="08a2b-112">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="08a2b-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a2b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="08a2b-113">Remarks</span></span>

<span data-ttu-id="08a2b-114">Ne modifiez pas la chaîne de commentaire retournée qui est la chaîne de commentaire réelle qui se trouve dans la capture chargée.</span><span class="sxs-lookup"><span data-stu-id="08a2b-114">Do not alter the returned comment string which is the actual comment string that is in the loaded capture.</span></span> <span data-ttu-id="08a2b-115">Toute modification peut endommager la capture.</span><span class="sxs-lookup"><span data-stu-id="08a2b-115">Any changes can corrupt the capture.</span></span> <span data-ttu-id="08a2b-116">Toute tentative de modification de la chaîne entraîne une violation d’accès.</span><span class="sxs-lookup"><span data-stu-id="08a2b-116">Attempts to modify the string result in an access violation.</span></span>

<span data-ttu-id="08a2b-117">Le descripteur de la capture peut être obtenu de plusieurs façons, en fonction de l’appel effectué par un expert ou un analyseur.</span><span class="sxs-lookup"><span data-stu-id="08a2b-117">The handle of the capture can be obtained in several ways, depending if the call is made by an expert or parser.</span></span> <span data-ttu-id="08a2b-118">Pour les experts, le descripteur est spécifié dans le membre **hCapture** de la structure [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="08a2b-118">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="08a2b-119">Pour les analyseurs, le handle de capture peut être obtenu en appelant la fonction [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="08a2b-119">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="08a2b-120">Pour récupérer le commentaire d’une capture à partir de son fichier de capture, appelez la fonction [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .</span><span class="sxs-lookup"><span data-stu-id="08a2b-120">To retrieve the comment of a capture from its capture file, call the [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) function.</span></span>

<span data-ttu-id="08a2b-121">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureComment** .</span><span class="sxs-lookup"><span data-stu-id="08a2b-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureComment** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a2b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08a2b-122">Requirements</span></span>



| <span data-ttu-id="08a2b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08a2b-123">Requirement</span></span> | <span data-ttu-id="08a2b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="08a2b-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08a2b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a2b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="08a2b-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a2b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="08a2b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a2b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="08a2b-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a2b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="08a2b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="08a2b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a2b-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="08a2b-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="08a2b-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08a2b-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="08a2b-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08a2b-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="08a2b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="08a2b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a2b-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a2b-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a2b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08a2b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a2b-136">EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="08a2b-136">EXPERTSTARTUPINFO</span></span>](expertstartupinfo.md)
</dt> <dt>

[<span data-ttu-id="08a2b-137">GetCaptureCommentFromFilename</span><span class="sxs-lookup"><span data-stu-id="08a2b-137">GetCaptureCommentFromFilename</span></span>](getcapturecommentfromfilename.md)
</dt> <dt>

[<span data-ttu-id="08a2b-138">GetFrameCaptureHandle</span><span class="sxs-lookup"><span data-stu-id="08a2b-138">GetFrameCaptureHandle</span></span>](getframecapturehandle.md)
</dt> </dl>

 

 




