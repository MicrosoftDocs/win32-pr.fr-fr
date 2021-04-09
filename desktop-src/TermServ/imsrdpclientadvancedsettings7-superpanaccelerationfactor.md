---
title: IMsRdpClientAdvancedSettings7 propriété SuperPanAccelerationFactor
description: Spécifie ou récupère une valeur qui indique le facteur d’accélération SuperPan. Le facteur d’accélération SuperPan détermine la vitesse à laquelle l’écran effectue le panoramique en mode SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SuperPanAccelerationFactor
- Services Bureau à distance de la propriété SuperPanAccelerationFactor, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété SuperPanAccelerationFactor
- Services Bureau à distance de la propriété SuperPanAccelerationFactor, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942887"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a><span data-ttu-id="ef544-109">IMsRdpClientAdvancedSettings7 :: SuperPanAccelerationFactor, propriété</span><span class="sxs-lookup"><span data-stu-id="ef544-109">IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor property</span></span>

<span data-ttu-id="ef544-110">Spécifie ou récupère une valeur qui indique le facteur d’accélération SuperPan.</span><span class="sxs-lookup"><span data-stu-id="ef544-110">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span> <span data-ttu-id="ef544-111">Le facteur d’accélération SuperPan détermine la vitesse à laquelle l’écran effectue le panoramique en mode SuperPan.</span><span class="sxs-lookup"><span data-stu-id="ef544-111">The SuperPan acceleration factor determines how quickly the screen pans when in SuperPan mode.</span></span> <span data-ttu-id="ef544-112">Le facteur d’accélération est le nombre de pixels que l’affichage de l’écran défile dans une direction donnée pour chaque pixel de déplacement de la souris par le client.</span><span class="sxs-lookup"><span data-stu-id="ef544-112">The acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement by the client.</span></span>

<span data-ttu-id="ef544-113">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ef544-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef544-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef544-114">Syntax</span></span>


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a><span data-ttu-id="ef544-115">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ef544-115">Property value</span></span>

<span data-ttu-id="ef544-116">Facteur d’accélération SuperPan à définir.</span><span class="sxs-lookup"><span data-stu-id="ef544-116">The SuperPan acceleration factor to set.</span></span> <span data-ttu-id="ef544-117">Le facteur d’accélération SuperPan est le nombre de pixels que l’affichage de l’écran défile dans une direction donnée pour chaque pixel du mouvement de la souris.</span><span class="sxs-lookup"><span data-stu-id="ef544-117">The SuperPan acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef544-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ef544-118">Remarks</span></span>

<span data-ttu-id="ef544-119">Pour plus d’informations sur SuperPan, consultez [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span><span class="sxs-lookup"><span data-stu-id="ef544-119">For more information about SuperPan, see [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef544-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef544-120">Requirements</span></span>



| <span data-ttu-id="ef544-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef544-121">Requirement</span></span> | <span data-ttu-id="ef544-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef544-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef544-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef544-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef544-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef544-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ef544-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef544-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef544-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef544-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ef544-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ef544-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef544-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef544-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ef544-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ef544-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef544-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef544-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ef544-131">IID</span><span class="sxs-lookup"><span data-stu-id="ef544-131">IID</span></span><br/>                      | <span data-ttu-id="ef544-132">IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="ef544-132">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef544-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef544-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef544-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ef544-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ef544-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ef544-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ef544-136">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="ef544-136">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





