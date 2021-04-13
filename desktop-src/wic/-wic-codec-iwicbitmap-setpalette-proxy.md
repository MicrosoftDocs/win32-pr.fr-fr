---
description: Fonction proxy pour la méthode SetPalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: IWICBitmap_SetPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525941"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="eae95-103">IWICBitmap \_ \_ fonction proxy SetPalette</span><span class="sxs-lookup"><span data-stu-id="eae95-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="eae95-104">Fonction proxy pour la méthode [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="eae95-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eae95-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eae95-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="eae95-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eae95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eae95-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eae95-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eae95-108">Tapez : \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="eae95-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="eae95-109">Pointeur vers cet objet [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="eae95-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="eae95-110">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eae95-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eae95-111">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="eae95-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="eae95-112">Palette à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="eae95-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eae95-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eae95-113">Return value</span></span>

<span data-ttu-id="eae95-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="eae95-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="eae95-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eae95-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eae95-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eae95-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eae95-117">Notes</span><span class="sxs-lookup"><span data-stu-id="eae95-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="eae95-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eae95-118">Requirements</span></span>



| <span data-ttu-id="eae95-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eae95-119">Requirement</span></span> | <span data-ttu-id="eae95-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="eae95-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eae95-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eae95-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eae95-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eae95-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="eae95-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eae95-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eae95-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eae95-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="eae95-125">DLL</span><span class="sxs-lookup"><span data-stu-id="eae95-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eae95-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eae95-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




