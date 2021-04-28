---
description: IWICMetadataQueryReader_GetContainerFormat_Proxy fonction de proxy de fonction pour la méthode GetContainerFormat.
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
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097137"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="1f836-103">IWICMetadataQueryReader \_ \_ fonction proxy GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="1f836-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="1f836-104">Fonction proxy pour la méthode [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="1f836-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f836-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f836-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="1f836-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f836-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f836-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f836-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f836-108">Type : **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span><span class="sxs-lookup"><span data-stu-id="1f836-108">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span></span>

<span data-ttu-id="1f836-109">Pointeur vers cet objet [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="1f836-109">Pointer to this [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="1f836-110">*pguidContainerFormat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f836-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f836-111">Type : **GUID \***</span><span class="sxs-lookup"><span data-stu-id="1f836-111">Type: **GUID\***</span></span>

<span data-ttu-id="1f836-112">Pointeur qui reçoit le GUID de format cointainer.</span><span class="sxs-lookup"><span data-stu-id="1f836-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f836-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f836-113">Return value</span></span>

<span data-ttu-id="1f836-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1f836-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1f836-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1f836-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f836-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f836-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f836-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1f836-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1f836-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1f836-118">Requirements</span></span>



| <span data-ttu-id="1f836-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f836-119">Requirement</span></span> | <span data-ttu-id="1f836-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f836-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f836-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f836-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1f836-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f836-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1f836-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f836-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1f836-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f836-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1f836-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1f836-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f836-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f836-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




