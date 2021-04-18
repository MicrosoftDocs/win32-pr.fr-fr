---
description: Fonction proxy pour la méthode SetMetadataByName.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: IWICMetadataQueryWriter_SetMetadataByName_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526210"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a><span data-ttu-id="58c46-103">IWICMetadataQueryWriter \_ \_ fonction proxy SetMetadataByName</span><span class="sxs-lookup"><span data-stu-id="58c46-103">IWICMetadataQueryWriter\_SetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="58c46-104">Fonction proxy pour la méthode [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="58c46-104">Proxy function for the [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c46-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58c46-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="58c46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58c46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c46-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58c46-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c46-108">Tapez : \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="58c46-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="58c46-109">Pointeur vers cet objet [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="58c46-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="58c46-110">*wzName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58c46-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c46-111">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="58c46-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="58c46-112">Nom de l’élément de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="58c46-112">The name of the metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="58c46-113">*pvarValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58c46-113">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c46-114">Type : \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="58c46-114">Type: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="58c46-115">Métadonnées à définir.</span><span class="sxs-lookup"><span data-stu-id="58c46-115">The metadata to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c46-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58c46-116">Return value</span></span>

<span data-ttu-id="58c46-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="58c46-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="58c46-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="58c46-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58c46-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58c46-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58c46-120">Notes</span><span class="sxs-lookup"><span data-stu-id="58c46-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="58c46-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="58c46-121">Requirements</span></span>



| <span data-ttu-id="58c46-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58c46-122">Requirement</span></span> | <span data-ttu-id="58c46-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="58c46-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c46-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58c46-124">Minimum supported client</span></span><br/> | <span data-ttu-id="58c46-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58c46-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="58c46-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58c46-126">Minimum supported server</span></span><br/> | <span data-ttu-id="58c46-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58c46-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="58c46-128">DLL</span><span class="sxs-lookup"><span data-stu-id="58c46-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c46-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58c46-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

