---
description: IWICBitmapDecoder_CopyPalette_Proxy fonction de proxy de fonction pour la méthode CopyPalette.
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
ms.openlocfilehash: 56dbc523fe29ef9cc958b6ffbd80509284b78b88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086357"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="9eb27-103">\_Fonction de \_ proxy IWICBitmapDecoder CopyPalette</span><span class="sxs-lookup"><span data-stu-id="9eb27-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="9eb27-104">Fonction proxy pour la méthode [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="9eb27-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eb27-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="9eb27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9eb27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb27-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eb27-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb27-108">Tapez : **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="9eb27-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="9eb27-109">Pointeur vers cet objet [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="9eb27-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="9eb27-110">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eb27-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb27-111">Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="9eb27-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="9eb27-112">Palette d’images à copier.</span><span class="sxs-lookup"><span data-stu-id="9eb27-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb27-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9eb27-113">Return value</span></span>

<span data-ttu-id="9eb27-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9eb27-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9eb27-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb27-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9eb27-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9eb27-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb27-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9eb27-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb27-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9eb27-118">Requirements</span></span>



| <span data-ttu-id="9eb27-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eb27-119">Requirement</span></span> | <span data-ttu-id="9eb27-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eb27-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb27-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eb27-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb27-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eb27-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9eb27-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eb27-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb27-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eb27-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9eb27-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb27-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb27-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eb27-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




