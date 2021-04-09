---
description: Fonction proxy pour la méthode RemoveMetadataByName.
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: IWICMetadataQueryWriter_RemoveMetadataByName_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866530"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a><span data-ttu-id="6eeca-103">IWICMetadataQueryWriter \_ \_ fonction proxy RemoveMetadataByName</span><span class="sxs-lookup"><span data-stu-id="6eeca-103">IWICMetadataQueryWriter\_RemoveMetadataByName\_Proxy function</span></span>

<span data-ttu-id="6eeca-104">Fonction proxy pour la méthode [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="6eeca-104">Proxy function for the [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eeca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6eeca-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a><span data-ttu-id="6eeca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6eeca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eeca-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeca-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeca-108">Tapez : \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="6eeca-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="6eeca-109">Pointeur vers cet objet [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="6eeca-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="6eeca-110">*wzName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeca-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeca-111">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6eeca-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="6eeca-112">Nom de l’élément de métadonnées à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6eeca-112">The name of the metadata item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eeca-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6eeca-113">Return value</span></span>

<span data-ttu-id="6eeca-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6eeca-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6eeca-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6eeca-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6eeca-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6eeca-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eeca-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6eeca-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6eeca-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6eeca-118">Requirements</span></span>



| <span data-ttu-id="6eeca-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6eeca-119">Requirement</span></span> | <span data-ttu-id="6eeca-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6eeca-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eeca-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eeca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6eeca-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eeca-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6eeca-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eeca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6eeca-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eeca-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6eeca-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6eeca-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eeca-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eeca-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




