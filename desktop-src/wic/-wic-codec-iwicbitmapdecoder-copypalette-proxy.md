---
description: Fonction proxy pour la méthode CopyPalette.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: IWICBitmapDecoder_CopyPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6902668a9c4feffdcc696ce0d5f6214a707bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516648"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="b4969-103">\_Fonction de \_ proxy IWICBitmapDecoder CopyPalette</span><span class="sxs-lookup"><span data-stu-id="b4969-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="b4969-104">Fonction proxy pour la méthode [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="b4969-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4969-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4969-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="b4969-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4969-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4969-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4969-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4969-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="b4969-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="b4969-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="b4969-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="b4969-110">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4969-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4969-111">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="b4969-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="b4969-112">Palette d’images à copier.</span><span class="sxs-lookup"><span data-stu-id="b4969-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4969-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4969-113">Return value</span></span>

<span data-ttu-id="b4969-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b4969-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b4969-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b4969-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4969-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4969-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4969-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b4969-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b4969-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b4969-118">Requirements</span></span>



| <span data-ttu-id="b4969-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4969-119">Requirement</span></span> | <span data-ttu-id="b4969-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4969-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4969-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4969-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b4969-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4969-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b4969-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4969-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b4969-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4969-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b4969-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b4969-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4969-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4969-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




