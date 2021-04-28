---
description: IWICBitmap_SetPalette_Proxy fonction de proxy de fonction pour la méthode SetPalette.
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
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086407"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="6a5de-103">IWICBitmap \_ \_ fonction proxy SetPalette</span><span class="sxs-lookup"><span data-stu-id="6a5de-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="6a5de-104">Fonction proxy pour la méthode [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="6a5de-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a5de-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="6a5de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a5de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a5de-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a5de-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5de-108">Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="6a5de-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="6a5de-109">Pointeur vers cet objet [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="6a5de-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="6a5de-110">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a5de-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5de-111">Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="6a5de-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="6a5de-112">Palette à utiliser pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="6a5de-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a5de-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a5de-113">Return value</span></span>

<span data-ttu-id="6a5de-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a5de-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6a5de-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a5de-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a5de-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a5de-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5de-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6a5de-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6a5de-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6a5de-118">Requirements</span></span>



| <span data-ttu-id="6a5de-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a5de-119">Requirement</span></span> | <span data-ttu-id="6a5de-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a5de-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5de-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a5de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a5de-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a5de-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6a5de-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a5de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a5de-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a5de-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6a5de-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6a5de-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a5de-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a5de-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




