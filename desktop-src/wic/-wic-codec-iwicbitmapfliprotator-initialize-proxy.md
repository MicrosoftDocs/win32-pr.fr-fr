---
description: Fonction proxy pour la méthode Initialize.
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
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515640"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="8489e-103">IWICBitmapFlipRotator \_ Initialise la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="8489e-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="8489e-104">Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="8489e-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8489e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8489e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="8489e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8489e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8489e-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8489e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8489e-108">Tapez : \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _</span><span class="sxs-lookup"><span data-stu-id="8489e-108">Type: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\** _</span></span>

<span data-ttu-id="8489e-109">Pointeur vers cet objet [_ *IWICBitmapFlipRotator* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="8489e-109">Pointer to this [_ *IWICBitmapFlipRotator*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="8489e-110">*pISource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8489e-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8489e-111">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="8489e-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="8489e-112">Source de l’image bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8489e-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="8489e-113">_options \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8489e-113">_options\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8489e-114">Type : **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="8489e-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="8489e-115">[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) pour retourner ou faire pivoter l’image.</span><span class="sxs-lookup"><span data-stu-id="8489e-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8489e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8489e-116">Return value</span></span>

<span data-ttu-id="8489e-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8489e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8489e-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8489e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8489e-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8489e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8489e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8489e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8489e-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8489e-121">Requirements</span></span>



| <span data-ttu-id="8489e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8489e-122">Requirement</span></span> | <span data-ttu-id="8489e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8489e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8489e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8489e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8489e-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8489e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8489e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8489e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8489e-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8489e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8489e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8489e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8489e-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8489e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




