---
description: Fonction proxy pour la méthode CreateBitmapFlipRotator.
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: IWICImagingFactory_CreateBitmapFlipRotator_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523367"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a><span data-ttu-id="262cb-103">IWICImagingFactory \_ \_ fonction proxy CreateBitmapFlipRotator</span><span class="sxs-lookup"><span data-stu-id="262cb-103">IWICImagingFactory\_CreateBitmapFlipRotator\_Proxy function</span></span>

<span data-ttu-id="262cb-104">Fonction proxy pour la méthode [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="262cb-104">Proxy function for the [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="262cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="262cb-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a><span data-ttu-id="262cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="262cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="262cb-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="262cb-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="262cb-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="262cb-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="262cb-109">_ppIBitmapFlipRotator \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="262cb-109">_ppIBitmapFlipRotator\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="262cb-110">Type : **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span><span class="sxs-lookup"><span data-stu-id="262cb-110">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span></span>

<span data-ttu-id="262cb-111">Pointeur qui reçoit un pointeur vers un nouveau [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span><span class="sxs-lookup"><span data-stu-id="262cb-111">A pointer that receives a pointer to a new [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="262cb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="262cb-112">Return value</span></span>

<span data-ttu-id="262cb-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="262cb-113">Type: **HRESULT**</span></span>

<span data-ttu-id="262cb-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="262cb-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="262cb-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="262cb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="262cb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="262cb-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="262cb-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="262cb-117">Requirements</span></span>



| <span data-ttu-id="262cb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="262cb-118">Requirement</span></span> | <span data-ttu-id="262cb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="262cb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="262cb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="262cb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="262cb-121">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="262cb-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="262cb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="262cb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="262cb-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="262cb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="262cb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="262cb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="262cb-125"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="262cb-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




