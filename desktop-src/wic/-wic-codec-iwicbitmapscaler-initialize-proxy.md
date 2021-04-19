---
description: Fonction proxy pour la méthode Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531206"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="1069d-103">IWICBitmapScaler \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="1069d-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="1069d-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="1069d-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1069d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1069d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="1069d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1069d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1069d-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1069d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069d-108">Tapez : \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _</span><span class="sxs-lookup"><span data-stu-id="1069d-108">Type: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\** _</span></span>

<span data-ttu-id="1069d-109">Pointeur vers cet objet [_ *IWICBitmapScaler* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="1069d-109">Pointer to this [_ *IWICBitmapScaler*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="1069d-110">*pISource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1069d-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069d-111">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="1069d-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="1069d-112">Source de l’image bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1069d-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="1069d-113">_uiWidth \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1069d-113">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069d-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1069d-114">Type: **UINT**</span></span>

<span data-ttu-id="1069d-115">Largeur de destination.</span><span class="sxs-lookup"><span data-stu-id="1069d-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="1069d-116">*uiHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1069d-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069d-117">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1069d-117">Type: **UINT**</span></span>

<span data-ttu-id="1069d-118">Hauteur de destination.</span><span class="sxs-lookup"><span data-stu-id="1069d-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="1069d-119">*mode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1069d-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1069d-120">Type : **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="1069d-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="1069d-121">Mode d’interpolation à utiliser lors de la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="1069d-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1069d-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1069d-122">Return value</span></span>

<span data-ttu-id="1069d-123">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1069d-123">Type: **HRESULT**</span></span>

<span data-ttu-id="1069d-124">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1069d-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1069d-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1069d-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1069d-126">Notes</span><span class="sxs-lookup"><span data-stu-id="1069d-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1069d-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1069d-127">Requirements</span></span>



| <span data-ttu-id="1069d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1069d-128">Requirement</span></span> | <span data-ttu-id="1069d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1069d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1069d-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1069d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1069d-131">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1069d-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1069d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1069d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1069d-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1069d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1069d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1069d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1069d-135"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1069d-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




