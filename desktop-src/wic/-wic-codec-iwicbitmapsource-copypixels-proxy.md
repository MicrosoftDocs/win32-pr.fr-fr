---
description: Fonction proxy pour la méthode CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209915"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a><span data-ttu-id="23d8e-103">\_ \_ Fonction Proxy copyPixels IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="23d8e-103">IWICBitmapSource\_CopyPixels\_Proxy function</span></span>

<span data-ttu-id="23d8e-104">Fonction proxy pour la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="23d8e-104">Proxy function for the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="23d8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23d8e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="23d8e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23d8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d8e-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23d8e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d8e-108">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="23d8e-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="23d8e-109">Pointeur vers cet objet [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="23d8e-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="23d8e-110">*PRC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23d8e-110">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d8e-111">Type : \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="23d8e-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="23d8e-112">Rectangle à copier.</span><span class="sxs-lookup"><span data-stu-id="23d8e-112">The rectangle to copy.</span></span> <span data-ttu-id="23d8e-113">Une valeur NULL spécifie la bitmap entière.</span><span class="sxs-lookup"><span data-stu-id="23d8e-113">A NULL value specifies the entire bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="23d8e-114">_cbStride \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23d8e-114">_cbStride\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d8e-115">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="23d8e-115">Type: **UINT**</span></span>

<span data-ttu-id="23d8e-116">STRIDE de la bitmap</span><span class="sxs-lookup"><span data-stu-id="23d8e-116">The stride of the bitmap</span></span>

</dd> <dt>

<span data-ttu-id="23d8e-117">*cbBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23d8e-117">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d8e-118">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="23d8e-118">Type: **UINT**</span></span>

<span data-ttu-id="23d8e-119">Taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="23d8e-119">The size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="23d8e-120">*pbBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="23d8e-120">*pbBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23d8e-121">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="23d8e-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="23d8e-122">Pointeur vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="23d8e-122">A pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23d8e-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23d8e-123">Return value</span></span>

<span data-ttu-id="23d8e-124">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="23d8e-124">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="23d8e-125">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="23d8e-125">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23d8e-126">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23d8e-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23d8e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="23d8e-127">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="23d8e-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="23d8e-128">Requirements</span></span>



| <span data-ttu-id="23d8e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23d8e-129">Requirement</span></span> | <span data-ttu-id="23d8e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="23d8e-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d8e-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23d8e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="23d8e-132">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23d8e-132">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="23d8e-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23d8e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="23d8e-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23d8e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="23d8e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="23d8e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23d8e-136"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23d8e-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




