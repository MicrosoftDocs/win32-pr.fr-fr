---
description: Fonction proxy pour la méthode GetFileExtensions.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: IWICBitmapCodecInfo_GetFileExtensions_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318269"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a><span data-ttu-id="80d78-103">IWICBitmapCodecInfo \_ \_ fonction proxy GetFileExtensions</span><span class="sxs-lookup"><span data-stu-id="80d78-103">IWICBitmapCodecInfo\_GetFileExtensions\_Proxy function</span></span>

<span data-ttu-id="80d78-104">Fonction proxy pour la méthode [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .</span><span class="sxs-lookup"><span data-stu-id="80d78-104">Proxy function for the [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80d78-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="80d78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80d78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80d78-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80d78-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d78-108">Tapez : \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="80d78-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="80d78-109">Pointeur vers cet objet [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="80d78-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="80d78-110">*cchFileExtensions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80d78-110">*cchFileExtensions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d78-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="80d78-111">Type: **UINT**</span></span>

<span data-ttu-id="80d78-112">Taille de la mémoire tampon d’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="80d78-112">The size of the file name extension buffer.</span></span>

</dd> <dt>

<span data-ttu-id="80d78-113">*wzFileExtensions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="80d78-113">*wzFileExtensions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d78-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="80d78-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="80d78-115">Pointeur qui reçoit les extensions de nom de fichier associées au codec.</span><span class="sxs-lookup"><span data-stu-id="80d78-115">A pointer that receives the file name extensions associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="80d78-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="80d78-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d78-117">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="80d78-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="80d78-118">Taille réelle de la mémoire tampon nécessaire à la récupération de toutes les extensions de nom de fichier associées au codec.</span><span class="sxs-lookup"><span data-stu-id="80d78-118">The actual buffer size needed to retrieve all file name extensions associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80d78-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80d78-119">Return value</span></span>

<span data-ttu-id="80d78-120">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="80d78-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="80d78-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80d78-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80d78-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80d78-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80d78-123">Notes</span><span class="sxs-lookup"><span data-stu-id="80d78-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="80d78-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="80d78-124">Requirements</span></span>



| <span data-ttu-id="80d78-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80d78-125">Requirement</span></span> | <span data-ttu-id="80d78-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="80d78-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80d78-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80d78-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80d78-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80d78-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="80d78-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80d78-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80d78-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80d78-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="80d78-131">DLL</span><span class="sxs-lookup"><span data-stu-id="80d78-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80d78-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80d78-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




