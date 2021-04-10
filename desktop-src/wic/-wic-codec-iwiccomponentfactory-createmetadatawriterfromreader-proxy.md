---
description: Fonction proxy pour la méthode CreateMetadataWriterFromReader.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: IWICComponentFactory_CreateMetadataWriterFromReader_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865802"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a><span data-ttu-id="a567f-103">IWICComponentFactory \_ \_ fonction proxy CreateMetadataWriterFromReader</span><span class="sxs-lookup"><span data-stu-id="a567f-103">IWICComponentFactory\_CreateMetadataWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="a567f-104">Fonction proxy pour la méthode [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="a567f-104">Proxy function for the [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a567f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a567f-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a><span data-ttu-id="a567f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a567f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a567f-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a567f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a567f-108">Tapez : \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a567f-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="a567f-109">Pointeur vers cet objet [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="a567f-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="a567f-110">*pIReader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a567f-110">*pIReader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a567f-111">Tapez : \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _</span><span class="sxs-lookup"><span data-stu-id="a567f-111">Type: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\** _</span></span>

</dd> <dt>

<span data-ttu-id="a567f-112">_pguidVendor \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a567f-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a567f-113">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="a567f-113">Type: \**const GUID\** _</span></span>

</dd> <dt>

<span data-ttu-id="a567f-114">_ppIWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a567f-114">_ppIWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a567f-115">Type : **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="a567f-115">Type: **[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a567f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a567f-116">Return value</span></span>

<span data-ttu-id="a567f-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a567f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="a567f-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a567f-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a567f-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a567f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a567f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a567f-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a567f-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a567f-121">Requirements</span></span>



| <span data-ttu-id="a567f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a567f-122">Requirement</span></span> | <span data-ttu-id="a567f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a567f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a567f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a567f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a567f-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a567f-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a567f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a567f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a567f-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a567f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a567f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a567f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a567f-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a567f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




