---
description: Fonction proxy pour la méthode GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516237"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a><span data-ttu-id="b227f-103">IWICBitmapCodecInfo \_ \_ fonction proxy GetDeviceModels</span><span class="sxs-lookup"><span data-stu-id="b227f-103">IWICBitmapCodecInfo\_GetDeviceModels\_Proxy function</span></span>

<span data-ttu-id="b227f-104">Fonction proxy pour la méthode [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .</span><span class="sxs-lookup"><span data-stu-id="b227f-104">Proxy function for the [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b227f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b227f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="b227f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b227f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b227f-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b227f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b227f-108">Tapez : \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="b227f-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="b227f-109">Pointeur vers cet objet [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="b227f-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="b227f-110">*cchDeviceModels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b227f-110">*cchDeviceModels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b227f-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b227f-111">Type: **UINT**</span></span>

<span data-ttu-id="b227f-112">Taille de la mémoire tampon des modèles d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b227f-112">The size of the device models buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b227f-113">*wzDeviceModels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b227f-113">*wzDeviceModels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b227f-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b227f-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="b227f-115">Pointeur qui reçoit une liste séparée par des virgules des noms de modèles d’appareil associés au codec.</span><span class="sxs-lookup"><span data-stu-id="b227f-115">A pointer that receives a comma delimited list of device model names associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="b227f-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b227f-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b227f-117">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="b227f-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="b227f-118">Taille réelle de la mémoire tampon nécessaire pour récupérer tous les noms de modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b227f-118">The actual buffer size needed to retrieve all of the device model names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b227f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b227f-119">Return value</span></span>

<span data-ttu-id="b227f-120">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b227f-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b227f-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b227f-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b227f-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b227f-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b227f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b227f-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b227f-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b227f-124">Requirements</span></span>



| <span data-ttu-id="b227f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b227f-125">Requirement</span></span> | <span data-ttu-id="b227f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b227f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b227f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b227f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b227f-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b227f-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b227f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b227f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b227f-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b227f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b227f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b227f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b227f-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b227f-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




