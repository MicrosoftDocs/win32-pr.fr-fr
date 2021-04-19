---
description: Effectue une opération de décodage DXVA (DirectX Video Acceleration).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9 :: Execute, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531894"
---
# <a name="idirect3ddxvadevice9execute-method"></a><span data-ttu-id="eb67c-103">IDirect3DDXVADevice9 :: Execute, méthode</span><span class="sxs-lookup"><span data-stu-id="eb67c-103">IDirect3DDXVADevice9::Execute method</span></span>

<span data-ttu-id="eb67c-104">Effectue une opération de décodage DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="eb67c-104">Performs a DirectX Video Acceleration (DXVA) decoding operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb67c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb67c-105">Syntax</span></span>


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="eb67c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb67c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb67c-107">*FunctionNum*</span><span class="sxs-lookup"><span data-stu-id="eb67c-107">*FunctionNum*</span></span> 
</dt> <dd>

<span data-ttu-id="eb67c-108">**Valeur DWORD** qui contient un ou plusieurs numéros de fonction DXVA.</span><span class="sxs-lookup"><span data-stu-id="eb67c-108">A **DWORD** that contains one or more DXVA function numbers.</span></span> <span data-ttu-id="eb67c-109">Pour plus d’informations, reportez-vous à la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="eb67c-109">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> <dt>

<span data-ttu-id="eb67c-110">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="eb67c-110">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="eb67c-111">Pointeur vers une mémoire tampon qui contient des données d’entrée pour l’opération de décodage.</span><span class="sxs-lookup"><span data-stu-id="eb67c-111">A pointer to a buffer that contains input data for the decoding operation.</span></span> <span data-ttu-id="eb67c-112">La signification de ces données dépend du type de surface et du numéro de fonction.</span><span class="sxs-lookup"><span data-stu-id="eb67c-112">The meaning of this data depends on the surface type and function number.</span></span>

</dd> <dt>

<span data-ttu-id="eb67c-113">*Inverser*</span><span class="sxs-lookup"><span data-stu-id="eb67c-113">*InputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="eb67c-114">Taille des données d’entrée, en octets.</span><span class="sxs-lookup"><span data-stu-id="eb67c-114">The size of the input data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eb67c-115">*OutputData*</span><span class="sxs-lookup"><span data-stu-id="eb67c-115">*OutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="eb67c-116">Pointeur vers une mémoire tampon dans laquelle l’accélérateur vidéo écrit des données de sortie.</span><span class="sxs-lookup"><span data-stu-id="eb67c-116">Pointer to a buffer where the video accelerator writes output data.</span></span>

</dd> <dt>

<span data-ttu-id="eb67c-117">*En-dessous*</span><span class="sxs-lookup"><span data-stu-id="eb67c-117">*OutputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="eb67c-118">Taille de la mémoire tampon *OutputData* , en octets.</span><span class="sxs-lookup"><span data-stu-id="eb67c-118">The size of the *OutputData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eb67c-119">*NumBuffers*</span><span class="sxs-lookup"><span data-stu-id="eb67c-119">*NumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="eb67c-120">Nombre d’éléments dans le tableau *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="eb67c-120">The number of elements in the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="eb67c-121">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="eb67c-121">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="eb67c-122">Pointeur vers un tableau de structures [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .</span><span class="sxs-lookup"><span data-stu-id="eb67c-122">A pointer to an array of [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb67c-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb67c-123">Return value</span></span>

<span data-ttu-id="eb67c-124">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb67c-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb67c-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb67c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb67c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb67c-126">Requirements</span></span>



| <span data-ttu-id="eb67c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb67c-127">Requirement</span></span> | <span data-ttu-id="eb67c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb67c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="eb67c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb67c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="eb67c-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb67c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb67c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb67c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="eb67c-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb67c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eb67c-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb67c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb67c-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb67c-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb67c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb67c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb67c-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="eb67c-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
