---
description: Fonction proxy pour la méthode Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c1a2e684059b75e41c1d89e2d3dd5379cc208b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536560"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="1cdd9-103">IWICBitmapEncoder \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="1cdd9-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="1cdd9-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) .</span><span class="sxs-lookup"><span data-stu-id="1cdd9-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cdd9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cdd9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="1cdd9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cdd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cdd9-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cdd9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd9-108">Tapez : \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="1cdd9-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="1cdd9-109">Pointeur vers cet objet [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="1cdd9-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="1cdd9-110">*pIStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cdd9-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd9-111">Type : \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="1cdd9-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="1cdd9-112">Flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="1cdd9-113">_cacheOption \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cdd9-113">_cacheOption\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cdd9-114">Type : **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="1cdd9-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="1cdd9-115">[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) utilisé lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cdd9-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cdd9-116">Return value</span></span>

<span data-ttu-id="1cdd9-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1cdd9-117">Type: **HRESULT**</span></span>

<span data-ttu-id="1cdd9-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1cdd9-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cdd9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cdd9-120">Notes</span><span class="sxs-lookup"><span data-stu-id="1cdd9-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1cdd9-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1cdd9-121">Requirements</span></span>



| <span data-ttu-id="1cdd9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cdd9-122">Requirement</span></span> | <span data-ttu-id="1cdd9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cdd9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cdd9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cdd9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1cdd9-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cdd9-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1cdd9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cdd9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1cdd9-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cdd9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1cdd9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1cdd9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cdd9-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cdd9-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

