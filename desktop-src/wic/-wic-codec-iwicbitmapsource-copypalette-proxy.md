---
description: IWICBitmapSource_CopyPalette_Proxy fonction de proxy de fonction pour la méthode CopyPalette.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: IWICBitmapSource_CopyPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ad9f5096aff7770a0b1624495c5c717440b6bd39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100497"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="0d0cf-103">IWICBitmapSource \_ \_ fonction proxy CopyPalette</span><span class="sxs-lookup"><span data-stu-id="0d0cf-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="0d0cf-104">Fonction proxy pour la méthode [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="0d0cf-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d0cf-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="0d0cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d0cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d0cf-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d0cf-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0cf-108">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="0d0cf-108">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="0d0cf-109">Pointeur vers cet objet [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="0d0cf-109">Pointer to this [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="0d0cf-110">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d0cf-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0cf-111">Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="0d0cf-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="0d0cf-112">Palette.</span><span class="sxs-lookup"><span data-stu-id="0d0cf-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d0cf-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d0cf-113">Return value</span></span>

<span data-ttu-id="0d0cf-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0d0cf-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0d0cf-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0d0cf-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d0cf-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d0cf-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0cf-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0d0cf-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0cf-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0d0cf-118">Requirements</span></span>



| <span data-ttu-id="0d0cf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d0cf-119">Requirement</span></span> | <span data-ttu-id="0d0cf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d0cf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0cf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d0cf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0cf-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d0cf-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0d0cf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d0cf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0cf-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d0cf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0d0cf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d0cf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d0cf-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d0cf-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




