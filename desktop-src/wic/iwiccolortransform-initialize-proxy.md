---
description: Initialise un IWICColorTransform avec un IWICBitmapSource et le transforme d’un IWICColorContext en un autre.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530497"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a><span data-ttu-id="681ae-103">IWICColorTransform \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="681ae-103">IWICColorTransform\_Initialize\_Proxy function</span></span>

<span data-ttu-id="681ae-104">Initialise un [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) avec un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) et le transforme d’un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) en un autre.</span><span class="sxs-lookup"><span data-stu-id="681ae-104">Initializes an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) with a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) and transforms it from one [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="681ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="681ae-105">Syntax</span></span>


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a><span data-ttu-id="681ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="681ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681ae-107">*pIColorTransform* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="681ae-107">*pIColorTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681ae-108">Type : **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span><span class="sxs-lookup"><span data-stu-id="681ae-108">Type: **[**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span></span>

<span data-ttu-id="681ae-109">Transformation de couleur à initialiser.</span><span class="sxs-lookup"><span data-stu-id="681ae-109">The color transform to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="681ae-110">*pIBitmapSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="681ae-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681ae-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="681ae-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="681ae-112">Source bitmap utilisée pour initialiser la transformation de couleur.</span><span class="sxs-lookup"><span data-stu-id="681ae-112">The bitmap source used to initialize the color transform.</span></span>

</dd> <dt>

<span data-ttu-id="681ae-113">*pIContextSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="681ae-113">*pIContextSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681ae-114">Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="681ae-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="681ae-115">Source du contexte de couleur.</span><span class="sxs-lookup"><span data-stu-id="681ae-115">The color context source.</span></span>

</dd> <dt>

<span data-ttu-id="681ae-116">*pIContextDest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="681ae-116">*pIContextDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681ae-117">Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="681ae-117">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="681ae-118">Destination du contexte de couleur.</span><span class="sxs-lookup"><span data-stu-id="681ae-118">The color context destination.</span></span>

</dd> <dt>

<span data-ttu-id="681ae-119">*pixelFmtDest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="681ae-119">*pixelFmtDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681ae-120">Type : **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="681ae-120">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="681ae-121">GUID du format de pixel souhaité.</span><span class="sxs-lookup"><span data-stu-id="681ae-121">The GUID of the desired pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="681ae-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="681ae-122">Return value</span></span>

<span data-ttu-id="681ae-123">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="681ae-123">Type: **HRESULT**</span></span>

<span data-ttu-id="681ae-124">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="681ae-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="681ae-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="681ae-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="681ae-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="681ae-126">Requirements</span></span>



| <span data-ttu-id="681ae-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="681ae-127">Requirement</span></span> | <span data-ttu-id="681ae-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="681ae-128">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="681ae-129">DLL</span><span class="sxs-lookup"><span data-stu-id="681ae-129">DLL</span></span><br/> | <dl> <span data-ttu-id="681ae-130"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="681ae-130"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 




