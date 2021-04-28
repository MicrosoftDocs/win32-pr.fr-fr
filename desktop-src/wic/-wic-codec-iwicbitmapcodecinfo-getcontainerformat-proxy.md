---
description: IWICBitmapCodecInfo_GetContainerFormat_Proxy fonction de proxy de fonction pour la méthode GetContainerFormat.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086367"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="fd791-103">IWICBitmapCodecInfo \_ \_ fonction proxy GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="fd791-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="fd791-104">Fonction proxy pour la méthode [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="fd791-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd791-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd791-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="fd791-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd791-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd791-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd791-108">Type : **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span><span class="sxs-lookup"><span data-stu-id="fd791-108">Type: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span></span>

<span data-ttu-id="fd791-109">Pointeur vers cet objet [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="fd791-109">Pointer to this [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="fd791-110">*pguidContainerFormat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fd791-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd791-111">Type : **GUID \***</span><span class="sxs-lookup"><span data-stu-id="fd791-111">Type: **GUID\***</span></span>

<span data-ttu-id="fd791-112">Pointeur qui reçoit le GUID du conteneur.</span><span class="sxs-lookup"><span data-stu-id="fd791-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd791-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd791-113">Return value</span></span>

<span data-ttu-id="fd791-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd791-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fd791-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fd791-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd791-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd791-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd791-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fd791-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fd791-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd791-118">Requirements</span></span>



| <span data-ttu-id="fd791-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd791-119">Requirement</span></span> | <span data-ttu-id="fd791-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd791-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd791-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd791-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fd791-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd791-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fd791-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd791-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fd791-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd791-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fd791-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fd791-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd791-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd791-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




