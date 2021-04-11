---
description: Fonction proxy pour la méthode GetColors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203809"
---
# <a name="iwicpalette_getcolors_proxy-function"></a><span data-ttu-id="65f7c-103">IWICPalette \_ \_ fonction proxy GetColors</span><span class="sxs-lookup"><span data-stu-id="65f7c-103">IWICPalette\_GetColors\_Proxy function</span></span>

<span data-ttu-id="65f7c-104">Fonction proxy pour la méthode [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) .</span><span class="sxs-lookup"><span data-stu-id="65f7c-104">Proxy function for the [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65f7c-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a><span data-ttu-id="65f7c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65f7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f7c-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65f7c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f7c-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="65f7c-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="65f7c-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="65f7c-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="65f7c-110">*colorCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65f7c-110">*colorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f7c-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="65f7c-111">Type: **UINT**</span></span>

<span data-ttu-id="65f7c-112">Taille du tableau *pColors* .</span><span class="sxs-lookup"><span data-stu-id="65f7c-112">The size of the *pColors* array.</span></span>

</dd> <dt>

<span data-ttu-id="65f7c-113">*pColors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65f7c-113">*pColors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65f7c-114">Tapez : \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="65f7c-114">Type: \**WICColor\** _</span></span>

<span data-ttu-id="65f7c-115">Pointeur qui reçoit les couleurs de la palette.</span><span class="sxs-lookup"><span data-stu-id="65f7c-115">Pointer that receives the colors of the palette.</span></span>

</dd> <dt>

<span data-ttu-id="65f7c-116">_pcActualColors \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65f7c-116">_pcActualColors\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65f7c-117">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="65f7c-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="65f7c-118">Taille réelle nécessaire pour obtenir les couleurs de la palette.</span><span class="sxs-lookup"><span data-stu-id="65f7c-118">The actual size needed to obtain the palette colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f7c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65f7c-119">Return value</span></span>

<span data-ttu-id="65f7c-120">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="65f7c-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="65f7c-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65f7c-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65f7c-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65f7c-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65f7c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="65f7c-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="65f7c-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65f7c-124">Requirements</span></span>



| <span data-ttu-id="65f7c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65f7c-125">Requirement</span></span> | <span data-ttu-id="65f7c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="65f7c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f7c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65f7c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65f7c-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65f7c-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="65f7c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65f7c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65f7c-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65f7c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="65f7c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="65f7c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f7c-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65f7c-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




