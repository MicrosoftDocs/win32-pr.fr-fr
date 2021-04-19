---
UID: ''
title: CaptureStackBackTrace fonction)
description: Capture une trace arrière de la pile en parcourant la pile.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "106509828"
---
# <a name="capturestackbacktrace-function"></a><span data-ttu-id="5c71f-103">CaptureStackBackTrace fonction)</span><span class="sxs-lookup"><span data-stu-id="5c71f-103">CaptureStackBackTrace function</span></span>

## <a name="description"></a><span data-ttu-id="5c71f-104">Description</span><span class="sxs-lookup"><span data-stu-id="5c71f-104">Description</span></span>

<span data-ttu-id="5c71f-105">Capture une trace arrière de la pile en parcourant la pile et en enregistrant les informations pour chaque frame.</span><span class="sxs-lookup"><span data-stu-id="5c71f-105">Captures a stack back trace by walking up the stack and recording the information for each frame.</span></span>

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a><span data-ttu-id="5c71f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c71f-106">Parameters</span></span>

### <a name="framestoskip-in"></a><span data-ttu-id="5c71f-107">FramesToSkip [in]</span><span class="sxs-lookup"><span data-stu-id="5c71f-107">FramesToSkip [in]</span></span>

<span data-ttu-id="5c71f-108">Nombre de frames à ignorer à partir du début de la trace arrière.</span><span class="sxs-lookup"><span data-stu-id="5c71f-108">The number of frames to skip from the start of the back trace.</span></span>

### <a name="framestocapture-in"></a><span data-ttu-id="5c71f-109">FramesToCapture [in]</span><span class="sxs-lookup"><span data-stu-id="5c71f-109">FramesToCapture [in]</span></span>

<span data-ttu-id="5c71f-110">Nombre de frames à capturer.</span><span class="sxs-lookup"><span data-stu-id="5c71f-110">The number of frames to be captured.</span></span>
<span data-ttu-id="5c71f-111">Vous pouvez capturer jusqu’à **MAXUSHORT** frames.</span><span class="sxs-lookup"><span data-stu-id="5c71f-111">You can capture up to **MAXUSHORT** frames.</span></span>

<span data-ttu-id="5c71f-112">**Windows Server 2003 et Windows XP :**  La somme des paramètres *FramesToSkip* et *FramesToCapture* doit être inférieure à 63.</span><span class="sxs-lookup"><span data-stu-id="5c71f-112">**Windows Server 2003 and Windows XP:**  The sum of the *FramesToSkip* and *FramesToCapture* parameters must be less than 63.</span></span>

### <a name="backtrace-out"></a><span data-ttu-id="5c71f-113">Traces [out]</span><span class="sxs-lookup"><span data-stu-id="5c71f-113">BackTrace [out]</span></span>

<span data-ttu-id="5c71f-114">Tableau de pointeurs capturés à partir de la trace de la pile actuelle.</span><span class="sxs-lookup"><span data-stu-id="5c71f-114">An array of pointers captured from the current stack trace.</span></span>

### <a name="backtracehash-out-optional"></a><span data-ttu-id="5c71f-115">BackTraceHash [out, optional]</span><span class="sxs-lookup"><span data-stu-id="5c71f-115">BackTraceHash [out, optional]</span></span>

<span data-ttu-id="5c71f-116">Valeur qui peut être utilisée pour organiser des tables de hachage.</span><span class="sxs-lookup"><span data-stu-id="5c71f-116">A value that can be used to organize hash tables.</span></span>
<span data-ttu-id="5c71f-117">Si ce paramètre a la valeur **null**, aucune valeur de hachage n’est calculée.</span><span class="sxs-lookup"><span data-stu-id="5c71f-117">If this parameter is **NULL**, then no hash value is computed.</span></span>

<span data-ttu-id="5c71f-118">Cette valeur est calculée en fonction des valeurs des pointeurs retournés dans le tableau de suivi des traces.</span><span class="sxs-lookup"><span data-stu-id="5c71f-118">This value is calculated based on the values of the pointers returned in the BackTrace array.</span></span>
<span data-ttu-id="5c71f-119">Deux traces de pile identiques génèrent des valeurs de hachage identiques.</span><span class="sxs-lookup"><span data-stu-id="5c71f-119">Two identical stack traces will generate identical hash values.</span></span>

## <a name="returns"></a><span data-ttu-id="5c71f-120">Retours</span><span class="sxs-lookup"><span data-stu-id="5c71f-120">Returns</span></span>

<span data-ttu-id="5c71f-121">Nombre de frames capturés.</span><span class="sxs-lookup"><span data-stu-id="5c71f-121">The number of captured frames.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c71f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5c71f-122">Remarks</span></span>

<span data-ttu-id="5c71f-123">La fonction **CaptureStackBackTrace** est définie en tant que fonction **RtlCaptureStackBackTrace** (la définition est incluse dans le SDK Windows à partir de Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="5c71f-123">The **CaptureStackBackTrace** function is defined as the **RtlCaptureStackBackTrace** function (the definition is included in the Windows SDK beginning with Windows Vista).</span></span>
<span data-ttu-id="5c71f-124">Pour plus d’informations, consultez WinBase. h et Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="5c71f-124">For more information, see WinBase.h and WinNT.h.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c71f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c71f-125">See also</span></span>
