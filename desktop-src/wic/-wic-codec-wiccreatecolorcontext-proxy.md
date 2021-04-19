---
description: Fonction proxy pour la création d’un IWICColorContext.
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: WICCreateColorContext_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e4861bb1ccb275edc38163335e0da5d26441a334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536680"
---
# <a name="wiccreatecolorcontext_proxy-function"></a><span data-ttu-id="b98e6-103">\_Fonction proxy WICCreateColorContext</span><span class="sxs-lookup"><span data-stu-id="b98e6-103">WICCreateColorContext\_Proxy function</span></span>

<span data-ttu-id="b98e6-104">Fonction proxy pour la création d’un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="b98e6-104">Proxy function for creating an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

## <a name="syntax"></a><span data-ttu-id="b98e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b98e6-105">Syntax</span></span>


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="b98e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b98e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b98e6-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b98e6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b98e6-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="b98e6-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

<span data-ttu-id="b98e6-109">Pointeur vers cet objet [_ *IWICImagingFactory* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) .</span><span class="sxs-lookup"><span data-stu-id="b98e6-109">Pointer to this [_ *IWICImagingFactory*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="b98e6-110">*ppIColorContext*</span><span class="sxs-lookup"><span data-stu-id="b98e6-110">*ppIColorContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b98e6-111">Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span><span class="sxs-lookup"><span data-stu-id="b98e6-111">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b98e6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b98e6-112">Return value</span></span>

<span data-ttu-id="b98e6-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b98e6-113">Type: **HRESULT**</span></span>

<span data-ttu-id="b98e6-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b98e6-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b98e6-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b98e6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b98e6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b98e6-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b98e6-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b98e6-117">Requirements</span></span>



| <span data-ttu-id="b98e6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b98e6-118">Requirement</span></span> | <span data-ttu-id="b98e6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b98e6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b98e6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b98e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b98e6-121">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b98e6-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b98e6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b98e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b98e6-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b98e6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b98e6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b98e6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b98e6-125"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b98e6-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




