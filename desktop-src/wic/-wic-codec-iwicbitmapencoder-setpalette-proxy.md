---
description: Fonction proxy pour la méthode SetPalette.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 128953cd56c3bea17ec9761a2acf2b8bc89cacfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525929"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="87a58-103">IWICBitmapEncoder \_ \_ fonction proxy SetPalette</span><span class="sxs-lookup"><span data-stu-id="87a58-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="87a58-104">Fonction proxy pour la méthode [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="87a58-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a58-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87a58-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="87a58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87a58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a58-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87a58-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a58-108">Tapez : \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="87a58-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="87a58-109">Pointeur vers cet objet [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="87a58-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="87a58-110">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87a58-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a58-111">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="87a58-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="87a58-112">[_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) à utiliser comme palette globale.</span><span class="sxs-lookup"><span data-stu-id="87a58-112">The [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a58-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87a58-113">Return value</span></span>

<span data-ttu-id="87a58-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="87a58-114">Type: **HRESULT**</span></span>

<span data-ttu-id="87a58-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="87a58-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="87a58-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87a58-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="87a58-117">Notes</span><span class="sxs-lookup"><span data-stu-id="87a58-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="87a58-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="87a58-118">Requirements</span></span>



| <span data-ttu-id="87a58-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87a58-119">Requirement</span></span> | <span data-ttu-id="87a58-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="87a58-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a58-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87a58-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87a58-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87a58-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="87a58-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87a58-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87a58-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87a58-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="87a58-125">DLL</span><span class="sxs-lookup"><span data-stu-id="87a58-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87a58-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87a58-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




