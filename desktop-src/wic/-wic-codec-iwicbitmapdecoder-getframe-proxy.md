---
description: Fonction proxy pour la méthode GetFrame.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: IWICBitmapDecoder_GetFrame_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318266"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a><span data-ttu-id="9f398-103">\_Fonction de \_ proxy IWICBitmapDecoder GetFrame</span><span class="sxs-lookup"><span data-stu-id="9f398-103">IWICBitmapDecoder\_GetFrame\_Proxy function</span></span>

<span data-ttu-id="9f398-104">Fonction proxy pour la méthode [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) .</span><span class="sxs-lookup"><span data-stu-id="9f398-104">Proxy function for the [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f398-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f398-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a><span data-ttu-id="9f398-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f398-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f398-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f398-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f398-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="9f398-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="9f398-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="9f398-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="9f398-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f398-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f398-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="9f398-111">Type: **UINT**</span></span>

<span data-ttu-id="9f398-112">Frame particulier à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9f398-112">The particular frame to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9f398-113">*ppIBitmapFrame* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9f398-113">*ppIBitmapFrame* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f398-114">Type : **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span><span class="sxs-lookup"><span data-stu-id="9f398-114">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span></span>

<span data-ttu-id="9f398-115">Pointeur qui reçoit un pointeur vers [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="9f398-115">A pointer that receives a pointer to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f398-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f398-116">Return value</span></span>

<span data-ttu-id="9f398-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9f398-117">Type: **HRESULT**</span></span>

<span data-ttu-id="9f398-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9f398-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f398-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f398-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f398-120">Notes</span><span class="sxs-lookup"><span data-stu-id="9f398-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9f398-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f398-121">Requirements</span></span>



| <span data-ttu-id="9f398-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f398-122">Requirement</span></span> | <span data-ttu-id="9f398-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f398-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f398-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f398-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9f398-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f398-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9f398-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f398-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9f398-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f398-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9f398-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9f398-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f398-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f398-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




