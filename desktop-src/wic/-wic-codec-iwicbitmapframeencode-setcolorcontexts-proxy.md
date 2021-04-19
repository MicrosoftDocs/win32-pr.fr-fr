---
description: Fonction proxy pour la méthode SetColorContexts.
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: IWICBitmapFrameEncode_SetColorContexts_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8a960873340c15772113a3f1553a9b6e16c44338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543080"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a><span data-ttu-id="5833b-103">\_ \_ Fonction proxy SetColorContexts IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="5833b-103">IWICBitmapFrameEncode\_SetColorContexts\_Proxy function</span></span>

<span data-ttu-id="5833b-104">Fonction proxy pour la méthode [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="5833b-104">Proxy function for the [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5833b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5833b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="5833b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5833b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5833b-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5833b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5833b-108">Type : \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="5833b-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="5833b-109">Pointeur vers cet objet [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="5833b-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="5833b-110">*ompte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5833b-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5833b-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="5833b-111">Type: **UINT**</span></span>

<span data-ttu-id="5833b-112">Nombre de profils [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) à définir.</span><span class="sxs-lookup"><span data-stu-id="5833b-112">The number of [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) profiles to set.</span></span>

</dd> <dt>

<span data-ttu-id="5833b-113">*ppIColorContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5833b-113">*ppIColorContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5833b-114">Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="5833b-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="5833b-115">Pointeur vers un pointeur [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) contenant les profils de contextes de couleur à définir sur le frame.</span><span class="sxs-lookup"><span data-stu-id="5833b-115">A pointer to an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) pointer containing the color contexts profiles to set to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5833b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5833b-116">Return value</span></span>

<span data-ttu-id="5833b-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5833b-117">Type: **HRESULT**</span></span>

<span data-ttu-id="5833b-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5833b-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5833b-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5833b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5833b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5833b-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5833b-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5833b-121">Requirements</span></span>



| <span data-ttu-id="5833b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5833b-122">Requirement</span></span> | <span data-ttu-id="5833b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5833b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5833b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5833b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5833b-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5833b-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5833b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5833b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5833b-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5833b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5833b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5833b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5833b-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5833b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




