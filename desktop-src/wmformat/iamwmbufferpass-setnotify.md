---
title: Méthode IAMWMBufferPass SetNotify
description: La méthode SetNotify est utilisée par les applications pour fournir l’enregistreur ASF WM ou le filtre de lecteur ASF WM avec un pointeur vers l’interface IAMWMBufferPassCallback de l’application.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Méthode SetNotify format Windows Media
- Méthode SetNotify format Windows Media, interface IAMWMBufferPass
- Interface IAMWMBufferPass Windows Media format, méthode SetNotify
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382531"
---
# <a name="iamwmbufferpasssetnotify-method"></a><span data-ttu-id="e600f-106">IAMWMBufferPass :: SetNotify, méthode</span><span class="sxs-lookup"><span data-stu-id="e600f-106">IAMWMBufferPass::SetNotify method</span></span>

<span data-ttu-id="e600f-107">La méthode **SetNotify** est utilisée par les applications pour fournir l’enregistreur ASF WM ou le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) avec un pointeur vers l’interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) de l’application.</span><span class="sxs-lookup"><span data-stu-id="e600f-107">The **SetNotify** method is used by applications to provide the WM ASF Writer or [WM ASF Reader](wm-asf-reader-filter.md) filter with a pointer to the application's [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e600f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e600f-108">Syntax</span></span>


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="e600f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e600f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e600f-110">*pCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e600f-110">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e600f-111">Pointeur vers l’interface **IAMWMBufferPassCallback** de l’application.</span><span class="sxs-lookup"><span data-stu-id="e600f-111">Pointer to the application's **IAMWMBufferPassCallback** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e600f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e600f-112">Return value</span></span>

<span data-ttu-id="e600f-113">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e600f-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e600f-114">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e600f-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e600f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e600f-115">Remarks</span></span>

<span data-ttu-id="e600f-116">Appelez cette méthode avant de placer le graphique de filtre dans l’état d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e600f-116">Call this method before putting the filter graph into the run state.</span></span>

## <a name="see-also"></a><span data-ttu-id="e600f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e600f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e600f-118">**Interface IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="e600f-118">**IAMWMBufferPass Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 