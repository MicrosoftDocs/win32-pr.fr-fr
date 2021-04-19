---
description: Fonction proxy pour la méthode CreatePalette.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: IWICImagingFactory_CreatePalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518943"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a><span data-ttu-id="19289-103">IWICImagingFactory \_ \_ fonction proxy CreatePalette</span><span class="sxs-lookup"><span data-stu-id="19289-103">IWICImagingFactory\_CreatePalette\_Proxy function</span></span>

<span data-ttu-id="19289-104">Fonction proxy pour la méthode [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) .</span><span class="sxs-lookup"><span data-stu-id="19289-104">Proxy function for the [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="19289-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19289-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="19289-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19289-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19289-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19289-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19289-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="19289-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="19289-109">_ppIPalette \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19289-109">_ppIPalette\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19289-110">Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span><span class="sxs-lookup"><span data-stu-id="19289-110">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span></span>

<span data-ttu-id="19289-111">Pointeur qui reçoit un pointeur vers un nouveau [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span><span class="sxs-lookup"><span data-stu-id="19289-111">A pointer that receives a pointer to a new [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19289-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19289-112">Return value</span></span>

<span data-ttu-id="19289-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19289-113">Type: **HRESULT**</span></span>

<span data-ttu-id="19289-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="19289-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19289-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19289-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19289-116">Notes</span><span class="sxs-lookup"><span data-stu-id="19289-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="19289-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="19289-117">Requirements</span></span>



| <span data-ttu-id="19289-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19289-118">Requirement</span></span> | <span data-ttu-id="19289-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="19289-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19289-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19289-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19289-121">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19289-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="19289-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19289-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19289-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19289-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="19289-124">DLL</span><span class="sxs-lookup"><span data-stu-id="19289-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19289-125"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19289-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




