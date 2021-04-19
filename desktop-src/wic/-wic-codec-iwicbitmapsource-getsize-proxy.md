---
description: Fonction proxy pour la méthode de traitement.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: IWICBitmapSource_GetSize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543712"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a><span data-ttu-id="22ae2-103">IWICBitmapSource \_ obtient la \_ fonction proxy</span><span class="sxs-lookup"><span data-stu-id="22ae2-103">IWICBitmapSource\_GetSize\_Proxy function</span></span>

<span data-ttu-id="22ae2-104">Fonction proxy [**pour la méthode de traitement**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .</span><span class="sxs-lookup"><span data-stu-id="22ae2-104">Proxy function for the [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ae2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22ae2-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="22ae2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22ae2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ae2-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22ae2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22ae2-108">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="22ae2-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="22ae2-109">Pointeur vers cet objet [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="22ae2-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="22ae2-110">*puiWidth* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="22ae2-110">*puiWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22ae2-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="22ae2-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="22ae2-112">Pointeur qui reçoit la largeur en pixels de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="22ae2-112">A pointer that receives the pixel width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="22ae2-113">_puiHeight \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="22ae2-113">_puiHeight\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22ae2-114">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="22ae2-114">Type: \**UINT\** _</span></span>

<span data-ttu-id="22ae2-115">Pointeur qui reçoit la hauteur en pixels de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="22ae2-115">A pointer that receives the pixel height of the bitmap</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ae2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22ae2-116">Return value</span></span>

<span data-ttu-id="22ae2-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="22ae2-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="22ae2-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="22ae2-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22ae2-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22ae2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ae2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="22ae2-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="22ae2-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22ae2-121">Requirements</span></span>



| <span data-ttu-id="22ae2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22ae2-122">Requirement</span></span> | <span data-ttu-id="22ae2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="22ae2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ae2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22ae2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="22ae2-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22ae2-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="22ae2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22ae2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="22ae2-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22ae2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="22ae2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="22ae2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ae2-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22ae2-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




