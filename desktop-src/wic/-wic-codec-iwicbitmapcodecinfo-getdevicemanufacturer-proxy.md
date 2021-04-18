---
description: Fonction proxy pour la méthode GetDeviceManufacturer.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515997"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a><span data-ttu-id="299c0-103">IWICBitmapCodecInfo \_ \_ fonction proxy GetDeviceManufacturer</span><span class="sxs-lookup"><span data-stu-id="299c0-103">IWICBitmapCodecInfo\_GetDeviceManufacturer\_Proxy function</span></span>

<span data-ttu-id="299c0-104">Fonction proxy pour la méthode [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) .</span><span class="sxs-lookup"><span data-stu-id="299c0-104">Proxy function for the [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="299c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="299c0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="299c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="299c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="299c0-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="299c0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="299c0-108">Tapez : \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="299c0-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="299c0-109">Pointeur vers cet objet [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="299c0-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="299c0-110">*cchDeviceManufacturer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="299c0-110">*cchDeviceManufacturer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="299c0-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="299c0-111">Type: **UINT**</span></span>

<span data-ttu-id="299c0-112">Taille du nom de la fabrique d’appareils.</span><span class="sxs-lookup"><span data-stu-id="299c0-112">The size of the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="299c0-113">*wzDeviceManufacturer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="299c0-113">*wzDeviceManufacturer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="299c0-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="299c0-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="299c0-115">Pointeur qui reçoit le nom de la fabrique d’appareils.</span><span class="sxs-lookup"><span data-stu-id="299c0-115">A pointer that receives the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="299c0-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="299c0-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="299c0-117">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="299c0-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="299c0-118">Taille réelle de la mémoire tampon nécessaire pour récupérer le nom de la fabrique d’appareils.</span><span class="sxs-lookup"><span data-stu-id="299c0-118">The actual buffer size needed to retrieve the device manufacture's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="299c0-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="299c0-119">Return value</span></span>

<span data-ttu-id="299c0-120">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="299c0-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="299c0-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="299c0-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="299c0-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="299c0-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="299c0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="299c0-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="299c0-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="299c0-124">Requirements</span></span>



| <span data-ttu-id="299c0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="299c0-125">Requirement</span></span> | <span data-ttu-id="299c0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="299c0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="299c0-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="299c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="299c0-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="299c0-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="299c0-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="299c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="299c0-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="299c0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="299c0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="299c0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="299c0-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="299c0-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




