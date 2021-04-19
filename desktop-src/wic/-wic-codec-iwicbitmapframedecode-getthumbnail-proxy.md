---
description: Fonction proxy pour la méthode miniature.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: IWICBitmapFrameDecode_GetThumbnail_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c29b62b4d3839b7cd3db51574f38ab824b215310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544649"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="11266-103">\_ \_ Fonction proxy miniature IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="11266-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="11266-104">Fonction proxy pour la méthode [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="11266-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11266-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11266-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="11266-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11266-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11266-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11266-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11266-108">Tapez : \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="11266-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="11266-109">Pointeur vers cet objet [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="11266-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="11266-110">*ppIThumbnail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11266-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11266-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="11266-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="11266-112">Pointeur qui reçoit un pointeur vers le [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) de la miniature.</span><span class="sxs-lookup"><span data-stu-id="11266-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11266-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11266-113">Return value</span></span>

<span data-ttu-id="11266-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="11266-114">Type: **HRESULT**</span></span>

<span data-ttu-id="11266-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="11266-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11266-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11266-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11266-117">Notes</span><span class="sxs-lookup"><span data-stu-id="11266-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="11266-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="11266-118">Requirements</span></span>



| <span data-ttu-id="11266-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11266-119">Requirement</span></span> | <span data-ttu-id="11266-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="11266-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11266-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11266-121">Minimum supported client</span></span><br/> | <span data-ttu-id="11266-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11266-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="11266-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11266-123">Minimum supported server</span></span><br/> | <span data-ttu-id="11266-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11266-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="11266-125">DLL</span><span class="sxs-lookup"><span data-stu-id="11266-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11266-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11266-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




