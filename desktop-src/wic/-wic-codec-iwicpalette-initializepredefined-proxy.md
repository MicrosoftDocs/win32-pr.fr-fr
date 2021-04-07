---
description: Fonction proxy pour la méthode InitializePredefined.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: IWICPalette_InitializePredefined_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758848"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a><span data-ttu-id="14c42-103">IWICPalette \_ \_ fonction proxy InitializePredefined</span><span class="sxs-lookup"><span data-stu-id="14c42-103">IWICPalette\_InitializePredefined\_Proxy function</span></span>

<span data-ttu-id="14c42-104">Fonction proxy pour la méthode [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) .</span><span class="sxs-lookup"><span data-stu-id="14c42-104">Proxy function for the [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14c42-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="14c42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14c42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c42-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14c42-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c42-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="14c42-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="14c42-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="14c42-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="14c42-110">*ePaletteType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14c42-110">*ePaletteType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c42-111">Type : **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="14c42-111">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="14c42-112">Type de palette prédéfinie souhaité.</span><span class="sxs-lookup"><span data-stu-id="14c42-112">The desired pre-defined palette type.</span></span>

</dd> <dt>

<span data-ttu-id="14c42-113">*fAddTransparentColor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14c42-113">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c42-114">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="14c42-114">Type: **BOOL**</span></span>

<span data-ttu-id="14c42-115">Couleur tranparent facultative à ajouter à la palette.</span><span class="sxs-lookup"><span data-stu-id="14c42-115">The optional tranparent color to add to the palette.</span></span> <span data-ttu-id="14c42-116">Si aucune couleur transparente n’est nécessaire, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="14c42-116">If no transparent color is needed, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c42-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14c42-117">Return value</span></span>

<span data-ttu-id="14c42-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14c42-118">Type: **HRESULT**</span></span>

<span data-ttu-id="14c42-119">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="14c42-119">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14c42-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14c42-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c42-121">Notes</span><span class="sxs-lookup"><span data-stu-id="14c42-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="14c42-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="14c42-122">Requirements</span></span>



| <span data-ttu-id="14c42-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14c42-123">Requirement</span></span> | <span data-ttu-id="14c42-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="14c42-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c42-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14c42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="14c42-126">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14c42-126">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="14c42-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14c42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="14c42-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14c42-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="14c42-129">DLL</span><span class="sxs-lookup"><span data-stu-id="14c42-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14c42-130"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c42-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




