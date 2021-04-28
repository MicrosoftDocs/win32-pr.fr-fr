---
description: IWICBitmapFlipRotator_Initialize_Proxy fonction-proxy pour la méthode Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091157"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="566ae-103">IWICBitmapFlipRotator \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="566ae-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="566ae-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="566ae-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="566ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="566ae-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="566ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="566ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="566ae-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566ae-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566ae-108">Type : **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span><span class="sxs-lookup"><span data-stu-id="566ae-108">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span></span>

<span data-ttu-id="566ae-109">Pointeur vers cet objet [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="566ae-109">Pointer to this [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="566ae-110">*pISource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566ae-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566ae-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="566ae-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="566ae-112">Source de l’image bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="566ae-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="566ae-113">*options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566ae-113">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566ae-114">Type : **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="566ae-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="566ae-115">[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) pour retourner ou faire pivoter l’image.</span><span class="sxs-lookup"><span data-stu-id="566ae-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="566ae-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="566ae-116">Return value</span></span>

<span data-ttu-id="566ae-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="566ae-117">Type: **HRESULT**</span></span>

<span data-ttu-id="566ae-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="566ae-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="566ae-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="566ae-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="566ae-120">Notes</span><span class="sxs-lookup"><span data-stu-id="566ae-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="566ae-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="566ae-121">Requirements</span></span>



| <span data-ttu-id="566ae-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="566ae-122">Requirement</span></span> | <span data-ttu-id="566ae-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="566ae-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="566ae-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="566ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="566ae-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="566ae-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="566ae-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="566ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="566ae-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="566ae-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="566ae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="566ae-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="566ae-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="566ae-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




