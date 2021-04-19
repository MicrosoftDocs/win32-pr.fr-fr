---
description: Fonction proxy pour la méthode InitializeFromBitmap.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: IWICPalette_InitializeFromBitmap_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf5e119acf1efca948281a02f61d8954f4e08818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531754"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a><span data-ttu-id="83e9f-103">IWICPalette \_ \_ fonction proxy InitializeFromBitmap</span><span class="sxs-lookup"><span data-stu-id="83e9f-103">IWICPalette\_InitializeFromBitmap\_Proxy function</span></span>

<span data-ttu-id="83e9f-104">Fonction proxy pour la méthode [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) .</span><span class="sxs-lookup"><span data-stu-id="83e9f-104">Proxy function for the [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83e9f-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="83e9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83e9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83e9f-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83e9f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e9f-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="83e9f-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="83e9f-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="83e9f-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="83e9f-110">*pISurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83e9f-110">*pISurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e9f-111">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="83e9f-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="83e9f-112">Pointeur vers la bitmap source.</span><span class="sxs-lookup"><span data-stu-id="83e9f-112">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="83e9f-113">_colorCount \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83e9f-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e9f-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="83e9f-114">Type: **UINT**</span></span>

<span data-ttu-id="83e9f-115">Nombre de couleurs avec lesquelles initialiser la palette.</span><span class="sxs-lookup"><span data-stu-id="83e9f-115">The number of colors to initialize the palette with.</span></span>

</dd> <dt>

<span data-ttu-id="83e9f-116">*fAddTransparentColor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83e9f-116">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e9f-117">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="83e9f-117">Type: **BOOL**</span></span>

<span data-ttu-id="83e9f-118">Valeur qui indique s’il faut ajouter une couleur transparente.</span><span class="sxs-lookup"><span data-stu-id="83e9f-118">A value to indicate whether to add a transparent color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83e9f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83e9f-119">Return value</span></span>

<span data-ttu-id="83e9f-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="83e9f-120">Type: **HRESULT**</span></span>

<span data-ttu-id="83e9f-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="83e9f-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="83e9f-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83e9f-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="83e9f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="83e9f-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="83e9f-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="83e9f-124">Requirements</span></span>



| <span data-ttu-id="83e9f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83e9f-125">Requirement</span></span> | <span data-ttu-id="83e9f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="83e9f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e9f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83e9f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83e9f-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83e9f-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="83e9f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83e9f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83e9f-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83e9f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="83e9f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="83e9f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83e9f-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83e9f-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




