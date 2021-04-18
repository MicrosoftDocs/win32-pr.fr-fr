---
description: Fonction proxy pour la méthode CreateStream,.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: IWICImagingFactory_CreateStream_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534074"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a><span data-ttu-id="aebb8-103">IWICImagingFactory \_ \_ fonction proxy CreateStream,</span><span class="sxs-lookup"><span data-stu-id="aebb8-103">IWICImagingFactory\_CreateStream\_Proxy function</span></span>

<span data-ttu-id="aebb8-104">Fonction proxy pour la méthode [**CreateStream,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .</span><span class="sxs-lookup"><span data-stu-id="aebb8-104">Proxy function for the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aebb8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aebb8-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a><span data-ttu-id="aebb8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aebb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebb8-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebb8-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="aebb8-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="aebb8-109">_ppIWICStream \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-109">_ppIWICStream\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aebb8-110">Type : **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span><span class="sxs-lookup"><span data-stu-id="aebb8-110">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span></span>

<span data-ttu-id="aebb8-111">Pointeur qui reçoit un pointeur vers un nouveau [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span><span class="sxs-lookup"><span data-stu-id="aebb8-111">A pointer that receives a pointer to a new [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebb8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aebb8-112">Return value</span></span>

<span data-ttu-id="aebb8-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aebb8-113">Type: **HRESULT**</span></span>

<span data-ttu-id="aebb8-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aebb8-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aebb8-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aebb8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aebb8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="aebb8-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="aebb8-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aebb8-117">Requirements</span></span>



| <span data-ttu-id="aebb8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aebb8-118">Requirement</span></span> | <span data-ttu-id="aebb8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebb8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebb8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aebb8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aebb8-121">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="aebb8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aebb8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aebb8-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="aebb8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aebb8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aebb8-125"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aebb8-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




