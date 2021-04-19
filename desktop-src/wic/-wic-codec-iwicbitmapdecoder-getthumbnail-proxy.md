---
description: Fonction proxy pour la méthode miniature.
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: IWICBitmapDecoder_GetThumbnail_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7412999b1a685c0188e0f277e073791d753a245b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545170"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="e1188-103">\_Fonction de \_ proxy IWICBitmapDecoder miniature</span><span class="sxs-lookup"><span data-stu-id="e1188-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="e1188-104">Fonction proxy pour la méthode [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="e1188-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1188-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1188-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="e1188-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1188-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1188-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1188-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1188-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="e1188-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="e1188-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="e1188-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="e1188-110">*ppIThumbnail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e1188-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1188-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="e1188-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="e1188-112">Pointeur qui reçoit un pointeur vers le [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) de la miniature.</span><span class="sxs-lookup"><span data-stu-id="e1188-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1188-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1188-113">Return value</span></span>

<span data-ttu-id="e1188-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e1188-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e1188-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e1188-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e1188-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e1188-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1188-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e1188-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e1188-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e1188-118">Requirements</span></span>



| <span data-ttu-id="e1188-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1188-119">Requirement</span></span> | <span data-ttu-id="e1188-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1188-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1188-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1188-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e1188-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1188-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e1188-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1188-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e1188-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1188-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e1188-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e1188-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1188-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1188-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




