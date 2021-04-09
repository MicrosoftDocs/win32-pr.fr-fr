---
description: Crée une surface compressée pour le décodage DXVA (DirectX Video Acceleration).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9 :: CreateSurface, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115211"
---
# <a name="idirect3dvideodevice9createsurface-method"></a><span data-ttu-id="bbafd-103">IDirect3DVideoDevice9 :: CreateSurface, méthode</span><span class="sxs-lookup"><span data-stu-id="bbafd-103">IDirect3DVideoDevice9::CreateSurface method</span></span>

<span data-ttu-id="bbafd-104">Crée une surface compressée pour le décodage DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="bbafd-104">Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.</span></span>

<span data-ttu-id="bbafd-105">Pour connaître les exigences de surface, appelez [**IDirect3DVideoDevice9 :: GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) et examinez les structures [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) retournées.</span><span class="sxs-lookup"><span data-stu-id="bbafd-105">To get the surface requirements, call [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) and examine the returned [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbafd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbafd-106">Syntax</span></span>


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a><span data-ttu-id="bbafd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbafd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbafd-108">*Width*</span><span class="sxs-lookup"><span data-stu-id="bbafd-108">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-109">Largeur de la surface, en pixels.</span><span class="sxs-lookup"><span data-stu-id="bbafd-109">The width of the surface, in pixels.</span></span> <span data-ttu-id="bbafd-110">Affectez à ce paramètre la valeur **DXVACompBufferInfo. WidthToCreate**.</span><span class="sxs-lookup"><span data-stu-id="bbafd-110">Set this parameter equal to **DXVACompBufferInfo.WidthToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="bbafd-111">*Height*</span><span class="sxs-lookup"><span data-stu-id="bbafd-111">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-112">Hauteur de la surface, en pixels.</span><span class="sxs-lookup"><span data-stu-id="bbafd-112">The height of the surface, in pixels.</span></span> <span data-ttu-id="bbafd-113">Affectez à ce paramètre la valeur **DXVACompBufferInfo. HeightToCreate**.</span><span class="sxs-lookup"><span data-stu-id="bbafd-113">Set this parameter equal to **DXVACompBufferInfo.HeightToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="bbafd-114">*Tous*</span><span class="sxs-lookup"><span data-stu-id="bbafd-114">*BackBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-115">Nombre de mémoires tampons d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="bbafd-115">The number of back buffers.</span></span> <span data-ttu-id="bbafd-116">Ce paramètre peut être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="bbafd-116">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bbafd-117">*Format*</span><span class="sxs-lookup"><span data-stu-id="bbafd-117">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-118">Format de pixel, spécifié en tant que valeur **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="bbafd-118">The pixel format, specified as a **D3DFORMAT** value.</span></span> <span data-ttu-id="bbafd-119">Affectez à ce paramètre la valeur **DXVACompBufferInfo. format**.</span><span class="sxs-lookup"><span data-stu-id="bbafd-119">Set this parameter equal to **DXVACompBufferInfo.Format**.</span></span>

</dd> <dt>

<span data-ttu-id="bbafd-120">*Pool*</span><span class="sxs-lookup"><span data-stu-id="bbafd-120">*Pool*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-121">Pool de mémoire dans lequel créer la surface, spécifié comme valeur **D3DPOOL** .</span><span class="sxs-lookup"><span data-stu-id="bbafd-121">The memory pool in which to create the surface, specified as a **D3DPOOL** value.</span></span> <span data-ttu-id="bbafd-122">Affectez à ce paramètre la valeur **DXVACompBufferInfo. pool**.</span><span class="sxs-lookup"><span data-stu-id="bbafd-122">Set this parameter equal to **DXVACompBufferInfo.Pool**.</span></span>

</dd> <dt>

<span data-ttu-id="bbafd-123">*Utilisation*</span><span class="sxs-lookup"><span data-stu-id="bbafd-123">*Usage*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-124">**Or au niveau du** bit d’une ou plusieurs constantes **D3DUSAGE** .</span><span class="sxs-lookup"><span data-stu-id="bbafd-124">A bitwise **OR** of one or more **D3DUSAGE** constants.</span></span> <span data-ttu-id="bbafd-125">Affectez à ce paramètre la valeur **DXVACompBufferInfo. usage**.</span><span class="sxs-lookup"><span data-stu-id="bbafd-125">Set this parameter equal to **DXVACompBufferInfo.Usage**.</span></span>

</dd> <dt>

<span data-ttu-id="bbafd-126">*ppSurface*</span><span class="sxs-lookup"><span data-stu-id="bbafd-126">*ppSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-127">Reçoit un pointeur vers l’interface **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="bbafd-127">Receives a pointer to the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="bbafd-128">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="bbafd-128">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="bbafd-129">*pSharedHandle*</span><span class="sxs-lookup"><span data-stu-id="bbafd-129">*pSharedHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="bbafd-130">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bbafd-130">Reserved.</span></span> <span data-ttu-id="bbafd-131">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="bbafd-131">Set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbafd-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbafd-132">Return value</span></span>

<span data-ttu-id="bbafd-133">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bbafd-133">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bbafd-134">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bbafd-134">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbafd-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbafd-135">Requirements</span></span>



| <span data-ttu-id="bbafd-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbafd-136">Requirement</span></span> | <span data-ttu-id="bbafd-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbafd-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bbafd-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbafd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bbafd-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbafd-139">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bbafd-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbafd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bbafd-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbafd-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bbafd-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbafd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbafd-143"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbafd-143"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbafd-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbafd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbafd-145">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="bbafd-145">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




