---
description: IWICBitmapFrameEncode_SetResolution_Proxy fonction de proxy de fonction pour la méthode SetResolution.
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: IWICBitmapFrameEncode_SetResolution_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 632d6e797d499c4c5468505a4cee49e088ab025a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116607"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="ae7d2-103">\_ \_ Fonction proxy SetResolution IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ae7d2-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="ae7d2-104">Fonction proxy pour la méthode [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="ae7d2-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae7d2-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="ae7d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae7d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae7d2-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae7d2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7d2-108">Type : **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="ae7d2-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="ae7d2-109">Pointeur vers cet objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="ae7d2-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="ae7d2-110">*DpiX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae7d2-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7d2-111">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="ae7d2-111">Type: **double**</span></span>

<span data-ttu-id="ae7d2-112">Valeur de résolution horizontale.</span><span class="sxs-lookup"><span data-stu-id="ae7d2-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="ae7d2-113">*DpiY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae7d2-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7d2-114">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="ae7d2-114">Type: **double**</span></span>

<span data-ttu-id="ae7d2-115">Valeur de résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="ae7d2-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae7d2-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae7d2-116">Return value</span></span>

<span data-ttu-id="ae7d2-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ae7d2-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ae7d2-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ae7d2-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae7d2-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae7d2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae7d2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ae7d2-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7d2-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae7d2-121">Requirements</span></span>



| <span data-ttu-id="ae7d2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae7d2-122">Requirement</span></span> | <span data-ttu-id="ae7d2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae7d2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7d2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae7d2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ae7d2-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae7d2-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ae7d2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae7d2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ae7d2-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae7d2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ae7d2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ae7d2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae7d2-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae7d2-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




