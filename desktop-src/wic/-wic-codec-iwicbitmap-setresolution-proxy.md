---
description: Fonction proxy pour la méthode SetResolution.
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
ms.openlocfilehash: eef599147a67986c6b9853f7a67e53a15be68e00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516860"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="782d3-103">IWICBitmap \_ \_ fonction proxy SetResolution</span><span class="sxs-lookup"><span data-stu-id="782d3-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="782d3-104">Fonction proxy pour la méthode [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="782d3-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="782d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="782d3-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="782d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="782d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="782d3-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="782d3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="782d3-108">Tapez : \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="782d3-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="782d3-109">Pointeur vers cet objet [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="782d3-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="782d3-110">*DpiX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="782d3-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="782d3-111">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="782d3-111">Type: **double**</span></span>

<span data-ttu-id="782d3-112">Résolution horizontale.</span><span class="sxs-lookup"><span data-stu-id="782d3-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="782d3-113">*DpiY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="782d3-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="782d3-114">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="782d3-114">Type: **double**</span></span>

<span data-ttu-id="782d3-115">Résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="782d3-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="782d3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="782d3-116">Return value</span></span>

<span data-ttu-id="782d3-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="782d3-117">Type: **HRESULT**</span></span>

<span data-ttu-id="782d3-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="782d3-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="782d3-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="782d3-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="782d3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="782d3-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="782d3-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="782d3-121">Requirements</span></span>



| <span data-ttu-id="782d3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="782d3-122">Requirement</span></span> | <span data-ttu-id="782d3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="782d3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="782d3-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="782d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="782d3-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="782d3-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="782d3-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="782d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="782d3-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="782d3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="782d3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="782d3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="782d3-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="782d3-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




