---
description: IWICBitmap_SetResolution_Proxy fonction de proxy de fonction pour la méthode SetResolution.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086377"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="5fa9d-103">IWICBitmap \_ \_ fonction proxy SetResolution</span><span class="sxs-lookup"><span data-stu-id="5fa9d-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="5fa9d-104">Fonction proxy pour la méthode [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fa9d-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="5fa9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fa9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fa9d-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fa9d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa9d-108">Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="5fa9d-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="5fa9d-109">Pointeur vers cet objet [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="5fa9d-110">*DpiX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fa9d-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa9d-111">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="5fa9d-111">Type: **double**</span></span>

<span data-ttu-id="5fa9d-112">Résolution horizontale.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="5fa9d-113">*DpiY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fa9d-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa9d-114">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="5fa9d-114">Type: **double**</span></span>

<span data-ttu-id="5fa9d-115">Résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fa9d-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5fa9d-116">Return value</span></span>

<span data-ttu-id="5fa9d-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5fa9d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="5fa9d-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5fa9d-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5fa9d-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5fa9d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fa9d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5fa9d-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa9d-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5fa9d-121">Requirements</span></span>



| <span data-ttu-id="5fa9d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fa9d-122">Requirement</span></span> | <span data-ttu-id="5fa9d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fa9d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa9d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fa9d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa9d-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fa9d-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5fa9d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fa9d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa9d-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fa9d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5fa9d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5fa9d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fa9d-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fa9d-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




