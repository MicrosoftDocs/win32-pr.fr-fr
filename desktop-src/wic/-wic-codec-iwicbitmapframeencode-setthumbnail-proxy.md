---
description: IWICBitmapFrameEncode_SetThumbnail_Proxy fonction de proxy de fonction pour la méthode SetThumbnail.
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: IWICBitmapFrameEncode_SetThumbnail_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9af9dd2d4f8fe71a6dc94420db17383a5da6da28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116597"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="1a7dc-103">\_ \_ Fonction proxy SetThumbnail IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="1a7dc-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="1a7dc-104">Fonction proxy pour la méthode [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="1a7dc-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a7dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a7dc-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="1a7dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a7dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a7dc-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a7dc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a7dc-108">Type : **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="1a7dc-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="1a7dc-109">Pointeur vers cet objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="1a7dc-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="1a7dc-110">*pIThumbnail* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a7dc-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a7dc-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="1a7dc-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="1a7dc-112">Source bitmap à utiliser comme miniature.</span><span class="sxs-lookup"><span data-stu-id="1a7dc-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a7dc-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a7dc-113">Return value</span></span>

<span data-ttu-id="1a7dc-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1a7dc-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1a7dc-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a7dc-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a7dc-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a7dc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a7dc-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1a7dc-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1a7dc-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1a7dc-118">Requirements</span></span>



| <span data-ttu-id="1a7dc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a7dc-119">Requirement</span></span> | <span data-ttu-id="1a7dc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a7dc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7dc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a7dc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a7dc-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a7dc-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1a7dc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a7dc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a7dc-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a7dc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1a7dc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1a7dc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a7dc-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a7dc-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




