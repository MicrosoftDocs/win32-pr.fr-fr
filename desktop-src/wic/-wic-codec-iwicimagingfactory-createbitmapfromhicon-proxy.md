---
description: Fonction proxy pour la méthode CreateBitmapFromHICON.
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: IWICImagingFactory_CreateBitmapFromHICON_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534059"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a><span data-ttu-id="5c775-103">IWICImagingFactory \_ \_ fonction proxy CreateBitmapFromHICON</span><span class="sxs-lookup"><span data-stu-id="5c775-103">IWICImagingFactory\_CreateBitmapFromHICON\_Proxy function</span></span>

<span data-ttu-id="5c775-104">Fonction proxy pour la méthode [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) .</span><span class="sxs-lookup"><span data-stu-id="5c775-104">Proxy function for the [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c775-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c775-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="5c775-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c775-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c775-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c775-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c775-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="5c775-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="5c775-109">_hIcon \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c775-109">_hIcon\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c775-110">Type : **HICON**</span><span class="sxs-lookup"><span data-stu-id="5c775-110">Type: **HICON**</span></span>

<span data-ttu-id="5c775-111">Handle d’icône à partir duquel créer la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="5c775-111">The icon handle to create the new bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="5c775-112">*ppIBitmap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5c775-112">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c775-113">Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c775-113">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="5c775-114">Pointeur qui reçoit un pointeur vers la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="5c775-114">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c775-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c775-115">Return value</span></span>

<span data-ttu-id="5c775-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c775-116">Type: **HRESULT**</span></span>

<span data-ttu-id="5c775-117">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c775-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c775-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c775-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c775-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5c775-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5c775-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5c775-120">Requirements</span></span>



| <span data-ttu-id="5c775-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c775-121">Requirement</span></span> | <span data-ttu-id="5c775-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c775-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c775-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c775-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5c775-124">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c775-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5c775-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c775-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5c775-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c775-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5c775-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5c775-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c775-128"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c775-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




