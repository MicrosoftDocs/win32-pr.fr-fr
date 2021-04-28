---
description: IWICBitmapFrameDecode_GetThumbnail_Proxy fonction de proxy de fonction pour la méthode miniature.
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
ms.openlocfilehash: 7f3c94461ac13aa39d14b97f13fe5e9e8d7569a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113637"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="2d476-103">\_ \_ Fonction proxy miniature IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="2d476-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="2d476-104">Fonction proxy pour la méthode [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="2d476-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d476-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d476-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="2d476-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d476-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d476-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d476-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d476-108">Type : **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="2d476-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="2d476-109">Pointeur vers cet objet [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="2d476-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="2d476-110">*ppIThumbnail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d476-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d476-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="2d476-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="2d476-112">Pointeur qui reçoit un pointeur vers le [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) de la miniature.</span><span class="sxs-lookup"><span data-stu-id="2d476-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d476-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d476-113">Return value</span></span>

<span data-ttu-id="2d476-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2d476-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2d476-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2d476-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d476-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d476-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d476-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2d476-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2d476-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2d476-118">Requirements</span></span>



| <span data-ttu-id="2d476-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d476-119">Requirement</span></span> | <span data-ttu-id="2d476-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d476-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d476-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d476-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2d476-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d476-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2d476-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d476-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2d476-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d476-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2d476-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2d476-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d476-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d476-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




