---
description: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy fonction de proxy de fonction pour la méthode GetMetadataQueryWriter.
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 89eb7342277d335c78ee2bc6807f2fc4d170bb9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113607"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="2d501-103">\_ \_ Fonction proxy GetMetadataQueryWriter IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="2d501-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="2d501-104">Fonction proxy pour la méthode [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="2d501-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d501-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d501-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="2d501-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d501-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d501-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d501-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d501-108">Type : **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="2d501-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="2d501-109">Pointeur vers cet objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="2d501-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="2d501-110">*ppIMetadataQueryWriter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d501-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d501-111">Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="2d501-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="2d501-112">Pointeur qui reçoit un générateur de requêtes de métadonnées pour le frame.</span><span class="sxs-lookup"><span data-stu-id="2d501-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d501-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d501-113">Return value</span></span>

<span data-ttu-id="2d501-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2d501-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2d501-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2d501-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d501-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d501-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d501-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2d501-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2d501-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2d501-118">Requirements</span></span>



| <span data-ttu-id="2d501-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d501-119">Requirement</span></span> | <span data-ttu-id="2d501-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d501-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d501-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d501-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2d501-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d501-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2d501-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d501-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2d501-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d501-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2d501-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2d501-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d501-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d501-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




