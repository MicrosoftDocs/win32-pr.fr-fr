---
description: Fonction proxy pour la méthode CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545144"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a><span data-ttu-id="a33f6-103">IWICImagingFactory \_ \_ fonction proxy CreateDecoderFromFilename</span><span class="sxs-lookup"><span data-stu-id="a33f6-103">IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function</span></span>

<span data-ttu-id="a33f6-104">Fonction proxy pour la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="a33f6-104">Proxy function for the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a33f6-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="a33f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a33f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33f6-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f6-108">Tapez : \**IWICImagingFactory \** _</span><span class="sxs-lookup"><span data-stu-id="a33f6-108">Type: \**IWICImagingFactory \** _</span></span>

</dd> <dt>

<span data-ttu-id="a33f6-109">_wzFilename \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-109">_wzFilename\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f6-110">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a33f6-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="a33f6-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un objet à créer ou ouvrir.</span><span class="sxs-lookup"><span data-stu-id="a33f6-111">A pointer to a null-terminated string that specifies the name of an object to create or open.</span></span>

</dd> <dt>

<span data-ttu-id="a33f6-112">*pGuidVendor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f6-113">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="a33f6-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="a33f6-114">GUID du fournisseur pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="a33f6-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="a33f6-115">_dwDesiredAccess \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-115">_dwDesiredAccess\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f6-116">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a33f6-116">Type: **DWORD**</span></span>

<span data-ttu-id="a33f6-117">Accès à l’objet, qui peut être en lecture, en écriture ou les deux.</span><span class="sxs-lookup"><span data-stu-id="a33f6-117">The access to the object, which can be read, write, or both.</span></span>

<span data-ttu-id="a33f6-118">Pour plus d’informations, consultez [ \[ fichiers \] de sécurité de fichiers et de droits d’accès](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="a33f6-118">For more information, see [File Security and Access Rights \[Files\]](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="a33f6-119">*metadataOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-119">*metadataOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f6-120">Type : **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="a33f6-120">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="a33f6-121">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) à utiliser lors de la création du décodeur.</span><span class="sxs-lookup"><span data-stu-id="a33f6-121">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="a33f6-122">*ppIDecoder* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-122">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f6-123">Tapez : **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="a33f6-123">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="a33f6-124">Pointeur qui reçoit un pointeur vers le nouveau [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="a33f6-124">A pointer that receives a pointer to the new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33f6-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a33f6-125">Return value</span></span>

<span data-ttu-id="a33f6-126">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a33f6-126">Type: **HRESULT**</span></span>

<span data-ttu-id="a33f6-127">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a33f6-127">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a33f6-128">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a33f6-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a33f6-129">Notes</span><span class="sxs-lookup"><span data-stu-id="a33f6-129">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a33f6-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a33f6-130">Requirements</span></span>



| <span data-ttu-id="a33f6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a33f6-131">Requirement</span></span> | <span data-ttu-id="a33f6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a33f6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a33f6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a33f6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a33f6-134">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-134">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a33f6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a33f6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a33f6-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a33f6-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a33f6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a33f6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a33f6-138"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a33f6-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

