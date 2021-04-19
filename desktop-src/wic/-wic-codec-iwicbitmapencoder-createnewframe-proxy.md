---
description: Fonction proxy pour la méthode CreateNewFrame.
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: IWICBitmapEncoder_CreateNewFrame_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527685"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a><span data-ttu-id="2e520-103">IWICBitmapEncoder \_ \_ fonction proxy CreateNewFrame</span><span class="sxs-lookup"><span data-stu-id="2e520-103">IWICBitmapEncoder\_CreateNewFrame\_Proxy function</span></span>

<span data-ttu-id="2e520-104">Fonction proxy pour la méthode [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) .</span><span class="sxs-lookup"><span data-stu-id="2e520-104">Proxy function for the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e520-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e520-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="2e520-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e520-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e520-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e520-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e520-108">Tapez : \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="2e520-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="2e520-109">Pointeur vers cet objet [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="2e520-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e520-110">*ppIFrameEncode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2e520-110">*ppIFrameEncode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e520-111">Type : **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e520-111">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span></span>

<span data-ttu-id="2e520-112">Pointeur qui reçoit un pointeur vers la nouvelle instance d’un [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="2e520-112">A pointer that receives a pointer to the new instance of an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

</dd> <dt>

<span data-ttu-id="2e520-113">*ppIEncoderOptions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2e520-113">*ppIEncoderOptions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e520-114">Type : **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span><span class="sxs-lookup"><span data-stu-id="2e520-114">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span></span>

<span data-ttu-id="2e520-115">Propriétés nommées à utiliser pour l’initialisation de frame.</span><span class="sxs-lookup"><span data-stu-id="2e520-115">The named properties to use for frame initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e520-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e520-116">Return value</span></span>

<span data-ttu-id="2e520-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e520-117">Type: **HRESULT**</span></span>

<span data-ttu-id="2e520-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e520-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e520-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e520-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e520-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2e520-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2e520-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2e520-121">Requirements</span></span>



| <span data-ttu-id="2e520-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e520-122">Requirement</span></span> | <span data-ttu-id="2e520-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e520-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e520-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e520-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2e520-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e520-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2e520-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e520-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2e520-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e520-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2e520-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2e520-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e520-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e520-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

