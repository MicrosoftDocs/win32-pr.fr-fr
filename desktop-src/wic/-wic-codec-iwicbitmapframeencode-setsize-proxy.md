---
description: Fonction proxy pour la méthode Configure.
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: IWICBitmapFrameEncode_SetSize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519390"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a><span data-ttu-id="aca47-103">IWICBitmapFrameEncode \_ définit la \_ fonction de proxy</span><span class="sxs-lookup"><span data-stu-id="aca47-103">IWICBitmapFrameEncode\_SetSize\_Proxy function</span></span>

<span data-ttu-id="aca47-104">Fonction proxy pour la méthode [**configure**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) .</span><span class="sxs-lookup"><span data-stu-id="aca47-104">Proxy function for the [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca47-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aca47-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="aca47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aca47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca47-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aca47-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca47-108">Type : \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="aca47-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="aca47-109">Pointeur vers cet objet [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="aca47-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="aca47-110">*uiWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aca47-110">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca47-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="aca47-111">Type: **UINT**</span></span>

<span data-ttu-id="aca47-112">Largeur de l’image de sortie.</span><span class="sxs-lookup"><span data-stu-id="aca47-112">The width of the output image.</span></span>

</dd> <dt>

<span data-ttu-id="aca47-113">*uiHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aca47-113">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca47-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="aca47-114">Type: **UINT**</span></span>

<span data-ttu-id="aca47-115">Hauteur de l’image de sortie.</span><span class="sxs-lookup"><span data-stu-id="aca47-115">The height of the output image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aca47-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aca47-116">Return value</span></span>

<span data-ttu-id="aca47-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aca47-117">Type: **HRESULT**</span></span>

<span data-ttu-id="aca47-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aca47-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aca47-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aca47-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aca47-120">Notes</span><span class="sxs-lookup"><span data-stu-id="aca47-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="aca47-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aca47-121">Requirements</span></span>



| <span data-ttu-id="aca47-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aca47-122">Requirement</span></span> | <span data-ttu-id="aca47-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="aca47-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aca47-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aca47-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aca47-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aca47-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="aca47-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aca47-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aca47-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aca47-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="aca47-128">DLL</span><span class="sxs-lookup"><span data-stu-id="aca47-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aca47-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aca47-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




