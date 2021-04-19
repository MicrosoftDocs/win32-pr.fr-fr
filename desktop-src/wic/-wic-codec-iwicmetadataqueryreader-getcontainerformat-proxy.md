---
description: Fonction proxy pour la méthode GetContainerFormat.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518509"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="f5148-103">IWICMetadataQueryReader \_ \_ fonction proxy GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="f5148-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="f5148-104">Fonction proxy pour la méthode [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="f5148-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5148-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5148-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f5148-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5148-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5148-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5148-108">Tapez : \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="f5148-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="f5148-109">Pointeur vers cet objet [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="f5148-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="f5148-110">*pguidContainerFormat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5148-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5148-111">Type : \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f5148-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="f5148-112">Pointeur qui reçoit le GUID de format cointainer.</span><span class="sxs-lookup"><span data-stu-id="f5148-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5148-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5148-113">Return value</span></span>

<span data-ttu-id="f5148-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f5148-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f5148-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5148-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5148-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5148-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5148-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f5148-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f5148-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f5148-118">Requirements</span></span>



| <span data-ttu-id="f5148-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5148-119">Requirement</span></span> | <span data-ttu-id="f5148-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5148-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5148-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5148-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f5148-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5148-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f5148-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5148-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f5148-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5148-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f5148-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f5148-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5148-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5148-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




