---
description: Fonction proxy pour la méthode SetThumbnail.
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
ms.openlocfilehash: 052e73911178ef0db957c5dd8edcf6e9d6892ace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866769"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="73887-103">\_ \_ Fonction proxy SetThumbnail IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="73887-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="73887-104">Fonction proxy pour la méthode [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="73887-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73887-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73887-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="73887-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73887-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73887-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73887-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73887-108">Type : \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="73887-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="73887-109">Pointeur vers cet objet [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="73887-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="73887-110">*pIThumbnail* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73887-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73887-111">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="73887-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="73887-112">Source bitmap à utiliser comme miniature.</span><span class="sxs-lookup"><span data-stu-id="73887-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73887-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73887-113">Return value</span></span>

<span data-ttu-id="73887-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="73887-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="73887-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73887-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73887-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73887-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73887-117">Notes</span><span class="sxs-lookup"><span data-stu-id="73887-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="73887-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="73887-118">Requirements</span></span>



| <span data-ttu-id="73887-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73887-119">Requirement</span></span> | <span data-ttu-id="73887-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="73887-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73887-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73887-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73887-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73887-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="73887-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73887-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73887-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73887-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="73887-125">DLL</span><span class="sxs-lookup"><span data-stu-id="73887-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73887-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73887-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




