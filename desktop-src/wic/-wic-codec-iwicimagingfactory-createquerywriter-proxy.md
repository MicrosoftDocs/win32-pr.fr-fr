---
description: Fonction proxy pour la méthode CreateQueryWriter.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: IWICImagingFactory_CreateQueryWriter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759063"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a><span data-ttu-id="f5ce4-103">IWICImagingFactory \_ \_ fonction proxy CreateQueryWriter</span><span class="sxs-lookup"><span data-stu-id="f5ce4-103">IWICImagingFactory\_CreateQueryWriter\_Proxy function</span></span>

<span data-ttu-id="f5ce4-104">Fonction proxy pour la méthode [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="f5ce4-104">Proxy function for the [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ce4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5ce4-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="f5ce4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ce4-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5ce4-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ce4-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="f5ce4-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="f5ce4-109">_guidMetadataFormat \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5ce4-109">_guidMetadataFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ce4-110">Type : **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="f5ce4-110">Type: **REFGUID**</span></span>

<span data-ttu-id="f5ce4-111">GUID pour le format de métadonnées souhaité.</span><span class="sxs-lookup"><span data-stu-id="f5ce4-111">The GUID for the desired metadata format.</span></span>

</dd> <dt>

<span data-ttu-id="f5ce4-112">*pGuidVendor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5ce4-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ce4-113">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="f5ce4-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f5ce4-114">GUID du fournisseur de l’enregistreur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="f5ce4-114">The vendor GUID of the metadata writer.</span></span>

</dd> <dt>

<span data-ttu-id="f5ce4-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f5ce4-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ce4-116">Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="f5ce4-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="f5ce4-117">Pointeur qui reçoit un pointeur vers un nouveau [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="f5ce4-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ce4-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5ce4-118">Return value</span></span>

<span data-ttu-id="f5ce4-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f5ce4-119">Type: **HRESULT**</span></span>

<span data-ttu-id="f5ce4-120">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5ce4-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5ce4-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5ce4-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5ce4-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f5ce4-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ce4-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f5ce4-123">Requirements</span></span>



| <span data-ttu-id="f5ce4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5ce4-124">Requirement</span></span> | <span data-ttu-id="f5ce4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5ce4-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ce4-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ce4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ce4-127">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5ce4-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f5ce4-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ce4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ce4-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5ce4-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f5ce4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f5ce4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5ce4-131"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5ce4-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




