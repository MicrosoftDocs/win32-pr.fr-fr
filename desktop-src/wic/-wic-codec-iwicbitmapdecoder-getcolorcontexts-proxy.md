---
description: Fonction proxy pour la méthode GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorContexts_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536166"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="28485-103">\_Fonction de \_ proxy IWICBitmapDecoder GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="28485-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="28485-104">Fonction proxy pour la méthode [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="28485-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28485-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28485-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="28485-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28485-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28485-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28485-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28485-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="28485-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="28485-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="28485-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="28485-110">*ompte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28485-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28485-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="28485-111">Type: **UINT**</span></span>

<span data-ttu-id="28485-112">Nombre de contextes de couleur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="28485-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="28485-113">Cette valeur doit être inférieure ou égale à la taille disponible pour *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="28485-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="28485-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28485-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28485-115">Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="28485-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="28485-116">Pointeur qui reçoit un pointeur vers [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="28485-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="28485-117">*pcActualCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28485-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28485-118">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="28485-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="28485-119">Pointeur qui reçoit le nombre de contextes de couleur contenus dans l’image.</span><span class="sxs-lookup"><span data-stu-id="28485-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28485-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28485-120">Return value</span></span>

<span data-ttu-id="28485-121">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="28485-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="28485-122">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="28485-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28485-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28485-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28485-124">Notes</span><span class="sxs-lookup"><span data-stu-id="28485-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="28485-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="28485-125">Requirements</span></span>



| <span data-ttu-id="28485-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28485-126">Requirement</span></span> | <span data-ttu-id="28485-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="28485-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28485-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28485-128">Minimum supported client</span></span><br/> | <span data-ttu-id="28485-129">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28485-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="28485-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28485-130">Minimum supported server</span></span><br/> | <span data-ttu-id="28485-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28485-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="28485-132">DLL</span><span class="sxs-lookup"><span data-stu-id="28485-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28485-133"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28485-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




