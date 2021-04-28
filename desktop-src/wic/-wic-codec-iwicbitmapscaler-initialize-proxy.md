---
description: IWICBitmapScaler_Initialize_Proxy fonction-proxy pour la méthode Initialize.
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
ms.openlocfilehash: 76b7c754273f4d55fbf3de9d8ba592806e590aac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100537"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="8841c-103">IWICBitmapScaler \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="8841c-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="8841c-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="8841c-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8841c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8841c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="8841c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8841c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8841c-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8841c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8841c-108">Type : **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span><span class="sxs-lookup"><span data-stu-id="8841c-108">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span></span>

<span data-ttu-id="8841c-109">Pointeur vers cet objet [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="8841c-109">Pointer to this [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="8841c-110">*pISource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8841c-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8841c-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="8841c-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="8841c-112">Source de l’image bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8841c-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="8841c-113">*uiWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8841c-113">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8841c-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8841c-114">Type: **UINT**</span></span>

<span data-ttu-id="8841c-115">Largeur de destination.</span><span class="sxs-lookup"><span data-stu-id="8841c-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="8841c-116">*uiHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8841c-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8841c-117">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8841c-117">Type: **UINT**</span></span>

<span data-ttu-id="8841c-118">Hauteur de destination.</span><span class="sxs-lookup"><span data-stu-id="8841c-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="8841c-119">*mode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8841c-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8841c-120">Type : **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="8841c-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="8841c-121">Mode d’interpolation à utiliser lors de la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="8841c-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8841c-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8841c-122">Return value</span></span>

<span data-ttu-id="8841c-123">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8841c-123">Type: **HRESULT**</span></span>

<span data-ttu-id="8841c-124">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8841c-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8841c-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8841c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8841c-126">Notes</span><span class="sxs-lookup"><span data-stu-id="8841c-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8841c-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8841c-127">Requirements</span></span>



| <span data-ttu-id="8841c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8841c-128">Requirement</span></span> | <span data-ttu-id="8841c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8841c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8841c-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8841c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8841c-131">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8841c-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8841c-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8841c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8841c-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8841c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8841c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8841c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8841c-135"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8841c-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




