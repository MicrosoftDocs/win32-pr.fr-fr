---
description: IWICBitmapFrameDecode_GetColorContexts_Proxy fonction de proxy de fonction pour la méthode GetColorContexts.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: IWICBitmapFrameDecode_GetColorContexts_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100577"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="bd2a3-103">\_ \_ Fonction proxy GetColorContexts IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="bd2a3-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="bd2a3-104">Fonction proxy pour la méthode [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="bd2a3-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd2a3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="bd2a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd2a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd2a3-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd2a3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2a3-108">Type : **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="bd2a3-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="bd2a3-109">Pointeur vers cet objet [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="bd2a3-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="bd2a3-110">*ompte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd2a3-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2a3-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="bd2a3-111">Type: **UINT**</span></span>

<span data-ttu-id="bd2a3-112">Nombre de contextes de couleur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="bd2a3-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="bd2a3-113">Cette valeur doit être inférieure ou égale à la taille disponible pour *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="bd2a3-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="bd2a3-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd2a3-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2a3-115">Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="bd2a3-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="bd2a3-116">Pointeur qui reçoit un pointeur vers les objets [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) .</span><span class="sxs-lookup"><span data-stu-id="bd2a3-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="bd2a3-117">*pcActualCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bd2a3-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2a3-118">Type : **uint \***</span><span class="sxs-lookup"><span data-stu-id="bd2a3-118">Type: **UINT\***</span></span>

<span data-ttu-id="bd2a3-119">Pointeur qui reçoit le nombre de contextes de couleur contenus dans le frame d’image.</span><span class="sxs-lookup"><span data-stu-id="bd2a3-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd2a3-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bd2a3-120">Return value</span></span>

<span data-ttu-id="bd2a3-121">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bd2a3-121">Type: **HRESULT**</span></span>

<span data-ttu-id="bd2a3-122">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bd2a3-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd2a3-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd2a3-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd2a3-124">Notes</span><span class="sxs-lookup"><span data-stu-id="bd2a3-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bd2a3-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bd2a3-125">Requirements</span></span>



| <span data-ttu-id="bd2a3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd2a3-126">Requirement</span></span> | <span data-ttu-id="bd2a3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd2a3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2a3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd2a3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2a3-129">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd2a3-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bd2a3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd2a3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2a3-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd2a3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bd2a3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bd2a3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd2a3-133"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd2a3-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




