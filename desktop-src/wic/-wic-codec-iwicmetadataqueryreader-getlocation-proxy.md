---
description: Fonction proxy pour la méthode GetLocation.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: IWICMetadataQueryReader_GetLocation_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522452"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a><span data-ttu-id="85cb0-103">IWICMetadataQueryReader \_ \_ fonction proxy GetLocation</span><span class="sxs-lookup"><span data-stu-id="85cb0-103">IWICMetadataQueryReader\_GetLocation\_Proxy function</span></span>

<span data-ttu-id="85cb0-104">Fonction proxy pour la méthode [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .</span><span class="sxs-lookup"><span data-stu-id="85cb0-104">Proxy function for the [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85cb0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85cb0-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a><span data-ttu-id="85cb0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85cb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85cb0-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85cb0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cb0-108">Tapez : \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="85cb0-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="85cb0-109">Pointeur vers cet objet [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="85cb0-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="85cb0-110">*cchMaxLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85cb0-110">*cchMaxLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cb0-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="85cb0-111">Type: **UINT**</span></span>

<span data-ttu-id="85cb0-112">Longueur de la mémoire tampon *wzNamespace* .</span><span class="sxs-lookup"><span data-stu-id="85cb0-112">The length of the *wzNamespace* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="85cb0-113">*wzNamespace* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85cb0-113">*wzNamespace* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85cb0-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="85cb0-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="85cb0-115">Pointeur qui reçoit l’emplacement actuel de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="85cb0-115">Pointer that receives the current namespace location.</span></span>

</dd> <dt>

<span data-ttu-id="85cb0-116">_pcchActualLength \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85cb0-116">_pcchActualLength\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85cb0-117">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="85cb0-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="85cb0-118">Longueur réelle de la mémoire tampon nécessaire pour récupérer l’emplacement actuel de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="85cb0-118">The actual buffer length needed to retrieve the current namespace location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85cb0-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85cb0-119">Return value</span></span>

<span data-ttu-id="85cb0-120">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="85cb0-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="85cb0-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="85cb0-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85cb0-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85cb0-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85cb0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="85cb0-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="85cb0-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="85cb0-124">Requirements</span></span>



| <span data-ttu-id="85cb0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85cb0-125">Requirement</span></span> | <span data-ttu-id="85cb0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="85cb0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85cb0-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85cb0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="85cb0-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85cb0-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="85cb0-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85cb0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="85cb0-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85cb0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="85cb0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="85cb0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85cb0-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85cb0-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




