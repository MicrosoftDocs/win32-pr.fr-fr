---
description: Fonction proxy pour la méthode GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210287"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a><span data-ttu-id="b3590-103">IWICPixelFormatInfo \_ \_ fonction proxy GetChannelMask</span><span class="sxs-lookup"><span data-stu-id="b3590-103">IWICPixelFormatInfo\_GetChannelMask\_Proxy function</span></span>

<span data-ttu-id="b3590-104">Fonction proxy pour la méthode [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) .</span><span class="sxs-lookup"><span data-stu-id="b3590-104">Proxy function for the [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3590-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3590-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a><span data-ttu-id="b3590-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3590-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3590-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3590-108">Tapez : \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="b3590-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="b3590-109">Pointeur vers cet objet [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="b3590-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="b3590-110">*uiChannelIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3590-110">*uiChannelIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3590-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b3590-111">Type: **UINT**</span></span>

<span data-ttu-id="b3590-112">Index du masque de canal à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b3590-112">The index to the channel mask to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b3590-113">*cbMaskBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3590-113">*cbMaskBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3590-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b3590-114">Type: **UINT**</span></span>

<span data-ttu-id="b3590-115">Taille de la mémoire tampon *pbMaskBuffer* .</span><span class="sxs-lookup"><span data-stu-id="b3590-115">The size of the *pbMaskBuffer* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b3590-116">*pbMaskBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3590-116">*pbMaskBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3590-117">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="b3590-117">Type: \**BYTE\** _</span></span>

<span data-ttu-id="b3590-118">Pointeur vers la mémoire tampon du masque.</span><span class="sxs-lookup"><span data-stu-id="b3590-118">Pointer to the mask buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b3590-119">_pcbActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3590-119">_pcbActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3590-120">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="b3590-120">Type: \**UINT\** _</span></span>

<span data-ttu-id="b3590-121">Taille réelle de la mémoire tampon nécessaire pour obtenir le masque de canal.</span><span class="sxs-lookup"><span data-stu-id="b3590-121">The actual buffer size needed to obtain the channel mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3590-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3590-122">Return value</span></span>

<span data-ttu-id="b3590-123">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b3590-123">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b3590-124">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b3590-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3590-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3590-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3590-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b3590-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b3590-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b3590-127">Requirements</span></span>



| <span data-ttu-id="b3590-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3590-128">Requirement</span></span> | <span data-ttu-id="b3590-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3590-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3590-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3590-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b3590-131">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3590-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b3590-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3590-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b3590-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3590-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b3590-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b3590-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3590-135"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3590-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




