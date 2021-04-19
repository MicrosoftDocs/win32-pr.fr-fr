---
description: Fonction proxy pour la méthode CreateEncoder.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: IWICImagingFactory_CreateEncoder_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518519"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a><span data-ttu-id="08464-103">IWICImagingFactory \_ \_ fonction proxy CreateEncoder</span><span class="sxs-lookup"><span data-stu-id="08464-103">IWICImagingFactory\_CreateEncoder\_Proxy function</span></span>

<span data-ttu-id="08464-104">Fonction proxy pour la méthode [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) .</span><span class="sxs-lookup"><span data-stu-id="08464-104">Proxy function for the [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="08464-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08464-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a><span data-ttu-id="08464-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08464-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08464-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08464-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08464-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="08464-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="08464-109">_guidContainerFormat \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08464-109">_guidContainerFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08464-110">Type : **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="08464-110">Type: **REFGUID**</span></span>

<span data-ttu-id="08464-111">GUID pour le format de conteneur souhaité.</span><span class="sxs-lookup"><span data-stu-id="08464-111">The GUID for the desired container format.</span></span>

</dd> <dt>

<span data-ttu-id="08464-112">*pGuidVendor* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="08464-112">*pguidVendor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08464-113">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="08464-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="08464-114">GUID du fournisseur pour l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="08464-114">The vendor GUID for the encoder.</span></span>

</dd> <dt>

<span data-ttu-id="08464-115">_ppIEncoder \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="08464-115">_ppIEncoder\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08464-116">Type : **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="08464-116">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span></span>

<span data-ttu-id="08464-117">Pointeur qui reçoit un pointeur vers un nouveau [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="08464-117">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08464-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08464-118">Return value</span></span>

<span data-ttu-id="08464-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="08464-119">Type: **HRESULT**</span></span>

<span data-ttu-id="08464-120">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="08464-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="08464-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08464-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="08464-122">Notes</span><span class="sxs-lookup"><span data-stu-id="08464-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="08464-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="08464-123">Requirements</span></span>



| <span data-ttu-id="08464-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08464-124">Requirement</span></span> | <span data-ttu-id="08464-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="08464-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08464-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08464-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08464-127">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08464-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="08464-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08464-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08464-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08464-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="08464-130">DLL</span><span class="sxs-lookup"><span data-stu-id="08464-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08464-131"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08464-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




