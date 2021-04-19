---
description: Fonction proxy pour la méthode GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: IWICPalette_GetType_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531722"
---
# <a name="iwicpalette_gettype_proxy-function"></a><span data-ttu-id="5a360-103">IWICPalette \_ \_ fonction proxy GetType</span><span class="sxs-lookup"><span data-stu-id="5a360-103">IWICPalette\_GetType\_Proxy function</span></span>

<span data-ttu-id="5a360-104">Fonction proxy pour la méthode [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .</span><span class="sxs-lookup"><span data-stu-id="5a360-104">Proxy function for the [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a360-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a360-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a><span data-ttu-id="5a360-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a360-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a360-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a360-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a360-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="5a360-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="5a360-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="5a360-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="5a360-110">*pePaletteType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a360-110">*pePaletteType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a360-111">Tapez : \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _</span><span class="sxs-lookup"><span data-stu-id="5a360-111">Type: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\** _</span></span>

<span data-ttu-id="5a360-112">Pointeur qui reçoit le type de palette du bimtap.</span><span class="sxs-lookup"><span data-stu-id="5a360-112">Pointer that receives the palette type of the bimtap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a360-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a360-113">Return value</span></span>

<span data-ttu-id="5a360-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5a360-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5a360-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a360-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a360-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a360-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a360-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5a360-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5a360-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5a360-118">Requirements</span></span>



| <span data-ttu-id="5a360-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a360-119">Requirement</span></span> | <span data-ttu-id="5a360-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a360-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a360-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a360-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5a360-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a360-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5a360-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a360-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5a360-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a360-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5a360-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5a360-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a360-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a360-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




