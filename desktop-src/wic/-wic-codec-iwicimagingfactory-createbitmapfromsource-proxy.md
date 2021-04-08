---
description: Fonction proxy pour la méthode CreateBitmapFromSource.
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: IWICImagingFactory_CreateBitmapFromSource_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953190"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a><span data-ttu-id="3969b-103">IWICImagingFactory \_ \_ fonction proxy CreateBitmapFromSource</span><span class="sxs-lookup"><span data-stu-id="3969b-103">IWICImagingFactory\_CreateBitmapFromSource\_Proxy function</span></span>

<span data-ttu-id="3969b-104">Fonction proxy pour la méthode [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) .</span><span class="sxs-lookup"><span data-stu-id="3969b-104">Proxy function for the [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3969b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3969b-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="3969b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3969b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3969b-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3969b-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3969b-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="3969b-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="3969b-109">_pIBitmapSource \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3969b-109">_pIBitmapSource\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3969b-110">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="3969b-110">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="3969b-111">[_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à partir duquel créer l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="3969b-111">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="3969b-112">*option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3969b-112">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3969b-113">Type : **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="3969b-113">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="3969b-114">Options de cache de la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="3969b-114">The cache options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="3969b-115">*ppIBitmap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3969b-115">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3969b-116">Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="3969b-116">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="3969b-117">Pointeur qui reçoit un pointeur vers la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="3969b-117">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3969b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3969b-118">Return value</span></span>

<span data-ttu-id="3969b-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3969b-119">Type: **HRESULT**</span></span>

<span data-ttu-id="3969b-120">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3969b-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3969b-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3969b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3969b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3969b-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3969b-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3969b-123">Requirements</span></span>



| <span data-ttu-id="3969b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3969b-124">Requirement</span></span> | <span data-ttu-id="3969b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3969b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3969b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3969b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3969b-127">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3969b-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3969b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3969b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3969b-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3969b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3969b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3969b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3969b-131"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3969b-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




