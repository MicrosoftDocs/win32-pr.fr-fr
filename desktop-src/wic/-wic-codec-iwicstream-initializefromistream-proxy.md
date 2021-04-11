---
description: Fonction proxy pour la méthode InitializeFromIStream.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: IWICStream_InitializeFromIStream_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204224"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a><span data-ttu-id="f9928-103">IWICStream \_ \_ fonction proxy InitializeFromIStream</span><span class="sxs-lookup"><span data-stu-id="f9928-103">IWICStream\_InitializeFromIStream\_Proxy function</span></span>

<span data-ttu-id="f9928-104">Fonction proxy pour la méthode [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) .</span><span class="sxs-lookup"><span data-stu-id="f9928-104">Proxy function for the [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9928-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9928-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a><span data-ttu-id="f9928-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9928-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9928-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9928-108">Tapez : \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="f9928-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="f9928-109">Pointeur vers cet objet [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="f9928-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="f9928-110">*pIStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9928-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9928-111">Type : \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="f9928-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="f9928-112">Flux d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="f9928-112">The initialize stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9928-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9928-113">Return value</span></span>

<span data-ttu-id="f9928-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f9928-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f9928-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f9928-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9928-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9928-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9928-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f9928-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f9928-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f9928-118">Requirements</span></span>



| <span data-ttu-id="f9928-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9928-119">Requirement</span></span> | <span data-ttu-id="f9928-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9928-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9928-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9928-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9928-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9928-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f9928-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9928-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9928-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9928-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f9928-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f9928-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9928-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9928-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

