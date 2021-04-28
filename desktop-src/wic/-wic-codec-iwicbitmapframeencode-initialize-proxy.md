---
description: IWICBitmapFrameEncode_Initialize_Proxy fonction-proxy pour la méthode Initialize.
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: IWICBitmapFrameEncode_Initialize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e8c8a7526343e6dfcda9859fd06259700019a9bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100547"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="c4484-103">IWICBitmapFrameEncode \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="c4484-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="c4484-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="c4484-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4484-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4484-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="c4484-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4484-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4484-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4484-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4484-108">Type : **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="c4484-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="c4484-109">Pointeur vers cet objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="c4484-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="c4484-110">*pIEncoderOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4484-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4484-111">Type : **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="c4484-111">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\***</span></span>

<span data-ttu-id="c4484-112">Ensemble de propriétés à utiliser pour l’initialisation de [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="c4484-112">The set of properties to use for [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4484-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4484-113">Return value</span></span>

<span data-ttu-id="c4484-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4484-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c4484-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4484-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4484-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4484-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4484-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c4484-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c4484-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4484-118">Requirements</span></span>



| <span data-ttu-id="c4484-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4484-119">Requirement</span></span> | <span data-ttu-id="c4484-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4484-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4484-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4484-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4484-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4484-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c4484-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4484-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c4484-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4484-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c4484-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c4484-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4484-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4484-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

