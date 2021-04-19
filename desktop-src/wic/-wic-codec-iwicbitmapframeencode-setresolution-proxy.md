---
description: Fonction proxy pour la méthode SetResolution.
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
ms.openlocfilehash: 9801384e305f2449c6a31b80cb238fc92f7b63b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521235"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="8544e-103">\_ \_ Fonction proxy SetResolution IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="8544e-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="8544e-104">Fonction proxy pour la méthode [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="8544e-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8544e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8544e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="8544e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8544e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8544e-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8544e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8544e-108">Type : \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="8544e-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="8544e-109">Pointeur vers cet objet [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="8544e-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="8544e-110">*DpiX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8544e-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8544e-111">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="8544e-111">Type: **double**</span></span>

<span data-ttu-id="8544e-112">Valeur de résolution horizontale.</span><span class="sxs-lookup"><span data-stu-id="8544e-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="8544e-113">*DpiY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8544e-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8544e-114">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="8544e-114">Type: **double**</span></span>

<span data-ttu-id="8544e-115">Valeur de résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="8544e-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8544e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8544e-116">Return value</span></span>

<span data-ttu-id="8544e-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8544e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8544e-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8544e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8544e-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8544e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8544e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8544e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8544e-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8544e-121">Requirements</span></span>



| <span data-ttu-id="8544e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8544e-122">Requirement</span></span> | <span data-ttu-id="8544e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8544e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8544e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8544e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8544e-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8544e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8544e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8544e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8544e-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8544e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8544e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8544e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8544e-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8544e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




