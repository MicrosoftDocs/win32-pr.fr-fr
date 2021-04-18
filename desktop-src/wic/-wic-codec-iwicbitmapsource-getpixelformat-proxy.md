---
description: Fonction proxy pour la méthode GetPixelFormat.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: IWICBitmapSource_GetPixelFormat_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519760"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a><span data-ttu-id="32ae7-103">IWICBitmapSource \_ \_ fonction proxy GetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="32ae7-103">IWICBitmapSource\_GetPixelFormat\_Proxy function</span></span>

<span data-ttu-id="32ae7-104">Fonction proxy pour la méthode [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .</span><span class="sxs-lookup"><span data-stu-id="32ae7-104">Proxy function for the [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ae7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32ae7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a><span data-ttu-id="32ae7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32ae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ae7-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32ae7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ae7-108">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="32ae7-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="32ae7-109">Pointeur vers cet objet [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="32ae7-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="32ae7-110">*pPixelFormat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="32ae7-110">*pPixelFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32ae7-111">Tapez : \**WICPixelFormatGUID \** _</span><span class="sxs-lookup"><span data-stu-id="32ae7-111">Type: \**WICPixelFormatGUID\** _</span></span>

<span data-ttu-id="32ae7-112">Pointeur qui reçoit le GUID de format de pixel dans lequel la bitmap est stockée.</span><span class="sxs-lookup"><span data-stu-id="32ae7-112">A pointer that receives the pixel format GUID the bitmap is stored in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ae7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32ae7-113">Return value</span></span>

<span data-ttu-id="32ae7-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="32ae7-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="32ae7-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="32ae7-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32ae7-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32ae7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ae7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="32ae7-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="32ae7-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="32ae7-118">Requirements</span></span>



| <span data-ttu-id="32ae7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32ae7-119">Requirement</span></span> | <span data-ttu-id="32ae7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="32ae7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ae7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32ae7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32ae7-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32ae7-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="32ae7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32ae7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32ae7-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32ae7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="32ae7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="32ae7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32ae7-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32ae7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




