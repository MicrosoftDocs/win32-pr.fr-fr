---
description: Fonction proxy pour la méthode GetMetadataByName.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: IWICMetadataQueryReader_GetMetadataByName_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521105"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a><span data-ttu-id="c405b-103">IWICMetadataQueryReader \_ \_ fonction proxy GetMetadataByName</span><span class="sxs-lookup"><span data-stu-id="c405b-103">IWICMetadataQueryReader\_GetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="c405b-104">Fonction proxy pour la méthode [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="c405b-104">Proxy function for the [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c405b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c405b-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="c405b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c405b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c405b-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c405b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c405b-108">Tapez : \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="c405b-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="c405b-109">Pointeur vers cet objet [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="c405b-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="c405b-110">*wzName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c405b-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c405b-111">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c405b-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="c405b-112">Nom de l’élément de métadonnées demandé.</span><span class="sxs-lookup"><span data-stu-id="c405b-112">The name of the requested metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="c405b-113">*pvarValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c405b-113">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c405b-114">Tapez : \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="c405b-114">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="c405b-115">Pointeur qui reçoit la propriété de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c405b-115">Pointer that receives the metadata property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c405b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c405b-116">Return value</span></span>

<span data-ttu-id="c405b-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c405b-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c405b-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c405b-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c405b-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c405b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c405b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c405b-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c405b-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c405b-121">Requirements</span></span>



| <span data-ttu-id="c405b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c405b-122">Requirement</span></span> | <span data-ttu-id="c405b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c405b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c405b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c405b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c405b-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c405b-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c405b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c405b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c405b-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c405b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c405b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c405b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c405b-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c405b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

