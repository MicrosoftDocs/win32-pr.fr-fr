---
description: Fonction proxy pour la méthode GetEncoderInfo.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: IWICBitmapEncoder_GetEncoderInfo_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535701"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a><span data-ttu-id="c9409-103">IWICBitmapEncoder \_ \_ fonction proxy GetEncoderInfo</span><span class="sxs-lookup"><span data-stu-id="c9409-103">IWICBitmapEncoder\_GetEncoderInfo\_Proxy function</span></span>

<span data-ttu-id="c9409-104">Fonction proxy pour la méthode [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="c9409-104">Proxy function for the [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9409-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9409-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c9409-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9409-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9409-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9409-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9409-108">Tapez : \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="c9409-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="c9409-109">Pointeur vers cet objet [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="c9409-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="c9409-110">*ppIEncoderInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9409-110">*ppIEncoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9409-111">Type : **[ **IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="c9409-111">Type: **[**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span></span>

<span data-ttu-id="c9409-112">Pointeur qui reçoit un pointeur vers un [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span><span class="sxs-lookup"><span data-stu-id="c9409-112">A pointer that receives a pointer to an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9409-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9409-113">Return value</span></span>

<span data-ttu-id="c9409-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c9409-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c9409-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c9409-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9409-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9409-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9409-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c9409-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c9409-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c9409-118">Requirements</span></span>



| <span data-ttu-id="c9409-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9409-119">Requirement</span></span> | <span data-ttu-id="c9409-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9409-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9409-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9409-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c9409-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9409-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c9409-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9409-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c9409-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9409-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c9409-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c9409-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9409-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9409-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




