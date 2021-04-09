---
description: Fonction proxy pour la méthode CreateBitmapClipper.
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: IWICImagingFactory_CreateBitmapClipper_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952744"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a><span data-ttu-id="89de1-103">IWICImagingFactory \_ \_ fonction proxy CreateBitmapClipper</span><span class="sxs-lookup"><span data-stu-id="89de1-103">IWICImagingFactory\_CreateBitmapClipper\_Proxy function</span></span>

<span data-ttu-id="89de1-104">Fonction proxy pour la méthode [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="89de1-104">Proxy function for the [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89de1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89de1-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a><span data-ttu-id="89de1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89de1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89de1-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89de1-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89de1-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="89de1-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="89de1-109">_ppIBitmapClipper \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89de1-109">_ppIBitmapClipper\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89de1-110">Type : **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span><span class="sxs-lookup"><span data-stu-id="89de1-110">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span></span>

<span data-ttu-id="89de1-111">Pointeur qui reçoit un pointeur vers un nouveau [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span><span class="sxs-lookup"><span data-stu-id="89de1-111">A pointer that receives a pointer to a new [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89de1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89de1-112">Return value</span></span>

<span data-ttu-id="89de1-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89de1-113">Type: **HRESULT**</span></span>

<span data-ttu-id="89de1-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="89de1-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89de1-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89de1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89de1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="89de1-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="89de1-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="89de1-117">Requirements</span></span>



| <span data-ttu-id="89de1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89de1-118">Requirement</span></span> | <span data-ttu-id="89de1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="89de1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89de1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89de1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="89de1-121">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89de1-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="89de1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89de1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="89de1-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89de1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="89de1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="89de1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89de1-125"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89de1-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




