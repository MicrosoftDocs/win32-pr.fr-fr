---
description: Fonction proxy pour la méthode GetEnumerator.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: IWICMetadataQueryReader_GetEnumerator_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534720"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a><span data-ttu-id="87124-103">IWICMetadataQueryReader \_ \_ fonction proxy GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="87124-103">IWICMetadataQueryReader\_GetEnumerator\_Proxy function</span></span>

<span data-ttu-id="87124-104">Fonction proxy pour la méthode [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) .</span><span class="sxs-lookup"><span data-stu-id="87124-104">Proxy function for the [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="87124-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87124-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a><span data-ttu-id="87124-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87124-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87124-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87124-108">Tapez : \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="87124-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="87124-109">Pointeur vers cet objet [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="87124-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="87124-110">*ppIEnumString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="87124-110">*ppIEnumString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87124-111">Type : **IEnumString \* \***</span><span class="sxs-lookup"><span data-stu-id="87124-111">Type: **IEnumString\*\***</span></span>

<span data-ttu-id="87124-112">Pointeur qui reçoit un pointeur vers un énumérateur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87124-112">A pointer that receives a pointer to a metadata enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87124-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87124-113">Return value</span></span>

<span data-ttu-id="87124-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="87124-114">Type: **HRESULT**</span></span>

<span data-ttu-id="87124-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="87124-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="87124-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87124-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="87124-117">Notes</span><span class="sxs-lookup"><span data-stu-id="87124-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="87124-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="87124-118">Requirements</span></span>



| <span data-ttu-id="87124-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87124-119">Requirement</span></span> | <span data-ttu-id="87124-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="87124-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87124-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87124-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87124-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87124-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="87124-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87124-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87124-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87124-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="87124-125">DLL</span><span class="sxs-lookup"><span data-stu-id="87124-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87124-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87124-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




