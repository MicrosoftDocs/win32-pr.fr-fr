---
description: Fonction proxy pour la méthode HasAlpha.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: IWICPalette_HasAlpha_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952421"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a><span data-ttu-id="c2b2b-103">IWICPalette \_ \_ fonction proxy HasAlpha</span><span class="sxs-lookup"><span data-stu-id="c2b2b-103">IWICPalette\_HasAlpha\_Proxy function</span></span>

<span data-ttu-id="c2b2b-104">Fonction proxy pour la méthode [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) .</span><span class="sxs-lookup"><span data-stu-id="c2b2b-104">Proxy function for the [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2b2b-105">Syntax</span></span>


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="c2b2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2b2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2b2b-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2b2b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b2b-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="c2b2b-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="c2b2b-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="c2b2b-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="c2b2b-110">*pfHasAlpha* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c2b2b-110">*pfHasAlpha* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b2b-111">Type : \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="c2b2b-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="c2b2b-112">Pointeur qui reçoit `TRUE` si la palette contient une couleur transparente ; sinon, `FALSE` .</span><span class="sxs-lookup"><span data-stu-id="c2b2b-112">Pointer that receives `TRUE` if the palette contains a transparent color; otherwise, `FALSE`.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2b2b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2b2b-113">Return value</span></span>

<span data-ttu-id="c2b2b-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c2b2b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c2b2b-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2b2b-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2b2b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2b2b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c2b2b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b2b-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c2b2b-118">Requirements</span></span>



| <span data-ttu-id="c2b2b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2b2b-119">Requirement</span></span> | <span data-ttu-id="c2b2b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2b2b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b2b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2b2b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b2b-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2b2b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c2b2b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2b2b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b2b-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2b2b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c2b2b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c2b2b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2b2b-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2b2b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




