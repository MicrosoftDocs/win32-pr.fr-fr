---
description: Fonction proxy pour la méthode Initialize.
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
ms.openlocfilehash: da9192409636de96dbd9d35d9614df2c926c9032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751220"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="70f99-103">IWICBitmapFrameEncode \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="70f99-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="70f99-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="70f99-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f99-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70f99-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="70f99-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70f99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f99-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70f99-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70f99-108">Type : \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="70f99-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="70f99-109">Pointeur vers cet objet [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="70f99-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="70f99-110">*pIEncoderOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70f99-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70f99-111">Tapez : \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="70f99-111">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="70f99-112">Ensemble de propriétés à utiliser pour l’initialisation de [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="70f99-112">The set of properties to use for [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70f99-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70f99-113">Return value</span></span>

<span data-ttu-id="70f99-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="70f99-114">Type: **HRESULT**</span></span>

<span data-ttu-id="70f99-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="70f99-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70f99-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70f99-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70f99-117">Notes</span><span class="sxs-lookup"><span data-stu-id="70f99-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="70f99-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="70f99-118">Requirements</span></span>



| <span data-ttu-id="70f99-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70f99-119">Requirement</span></span> | <span data-ttu-id="70f99-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="70f99-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f99-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70f99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="70f99-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70f99-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="70f99-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70f99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="70f99-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70f99-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="70f99-125">DLL</span><span class="sxs-lookup"><span data-stu-id="70f99-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70f99-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70f99-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

