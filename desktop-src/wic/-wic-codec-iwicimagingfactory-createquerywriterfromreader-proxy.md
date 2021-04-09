---
description: Fonction proxy pour la méthode CreateQueryWriterFromReader.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: IWICImagingFactory_CreateQueryWriterFromReader_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952830"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a><span data-ttu-id="c6e95-103">IWICImagingFactory \_ \_ fonction proxy CreateQueryWriterFromReader</span><span class="sxs-lookup"><span data-stu-id="c6e95-103">IWICImagingFactory\_CreateQueryWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="c6e95-104">Fonction proxy pour la méthode [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="c6e95-104">Proxy function for the [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e95-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6e95-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="c6e95-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6e95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e95-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6e95-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e95-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="c6e95-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="c6e95-109">_pIQueryReader \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6e95-109">_pIQueryReader\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e95-110">Tapez : \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="c6e95-110">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="c6e95-111">Lecteur de requêtes de métadonnées à partir duquel créer l’enregistreur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c6e95-111">The metadata query reader to create the metadata writer from.</span></span>

</dd> <dt>

<span data-ttu-id="c6e95-112">_pguidVendor \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6e95-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e95-113">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="c6e95-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="c6e95-114">GUID du fournisseur pour le générateur de requêtes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c6e95-114">The vendor GUID for the metadata query writer.</span></span>

</dd> <dt>

<span data-ttu-id="c6e95-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c6e95-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e95-116">Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6e95-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="c6e95-117">Pointeur qui reçoit un pointeur vers un nouveau [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="c6e95-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e95-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6e95-118">Return value</span></span>

<span data-ttu-id="c6e95-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6e95-119">Type: **HRESULT**</span></span>

<span data-ttu-id="c6e95-120">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c6e95-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6e95-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6e95-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e95-122">Notes</span><span class="sxs-lookup"><span data-stu-id="c6e95-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e95-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c6e95-123">Requirements</span></span>



| <span data-ttu-id="c6e95-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6e95-124">Requirement</span></span> | <span data-ttu-id="c6e95-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6e95-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e95-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e95-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e95-127">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e95-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c6e95-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e95-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e95-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e95-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c6e95-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c6e95-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6e95-131"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6e95-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




