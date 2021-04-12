---
description: Obtient les interfaces d’extension qui peuvent être fournies avec le pilote de périphérique WIA (Windows Image Acquisition) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2 :: GetExtension, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034011"
---
# <a name="iwiaitem2getextension-method"></a><span data-ttu-id="67a5f-103">IWiaItem2 :: GetExtension, méthode</span><span class="sxs-lookup"><span data-stu-id="67a5f-103">IWiaItem2::GetExtension method</span></span>

<span data-ttu-id="67a5f-104">Obtient les interfaces d’extension qui peuvent être fournies avec le pilote de périphérique WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="67a5f-104">Gets the extension interfaces that might come with a Windows Image Acquisition (WIA) 2.0 device driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67a5f-105">Syntax</span></span>


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a><span data-ttu-id="67a5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67a5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a5f-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67a5f-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a5f-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="67a5f-108">Type: **LONG**</span></span>

<span data-ttu-id="67a5f-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="67a5f-109">Currently unused.</span></span> <span data-ttu-id="67a5f-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="67a5f-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="67a5f-111">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67a5f-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a5f-112">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="67a5f-112">Type: **BSTR**</span></span>

<span data-ttu-id="67a5f-113">Spécifie le nom de l’extension vers laquelle l’application appelante requiert un pointeur.</span><span class="sxs-lookup"><span data-stu-id="67a5f-113">Specifies the name of the extension that the calling application requires a pointer to.</span></span>

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span data-ttu-id="67a5f-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span><span class="sxs-lookup"><span data-stu-id="67a5f-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span></span>


</dt> <dd>

<span data-ttu-id="67a5f-115">Extension du filtre de segmentation.</span><span class="sxs-lookup"><span data-stu-id="67a5f-115">The segmentation filter extension.</span></span> <span data-ttu-id="67a5f-116">Il s’agit actuellement de la seule valeur valide pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="67a5f-116">This is currently the only valid value for this parameter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="67a5f-117">*riidExtensionInterface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67a5f-117">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a5f-118">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="67a5f-118">Type: **REFIID**</span></span>

<span data-ttu-id="67a5f-119">Spécifie l’identificateur de l’interface d’extension.</span><span class="sxs-lookup"><span data-stu-id="67a5f-119">Specifies the identifier of the extension interface.</span></span>

</dd> <dt>

<span data-ttu-id="67a5f-120">*ppOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="67a5f-120">*ppOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67a5f-121">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="67a5f-121">Type: **VOID\*\***</span></span>

<span data-ttu-id="67a5f-122">Reçoit l’adresse d’un pointeur vers l’interface d’extension.</span><span class="sxs-lookup"><span data-stu-id="67a5f-122">Receives the address of a pointer to the extension interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a5f-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67a5f-123">Return value</span></span>

<span data-ttu-id="67a5f-124">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="67a5f-124">Type: **HRESULT**</span></span>

<span data-ttu-id="67a5f-125">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="67a5f-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67a5f-126">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67a5f-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67a5f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="67a5f-127">Remarks</span></span>

<span data-ttu-id="67a5f-128">Une application appelle cette méthode pour créer un objet d’extension qui implémente l’une des interfaces d’extension de pilote WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="67a5f-128">An application invokes this method to create an extension object implementing one of the WIA 2.0 driver extension interfaces.</span></span> <span data-ttu-id="67a5f-129">**IWiaItem2 :: GetExtension** stocke l’adresse de l’interface d’extension de l’objet d’extension dans le paramètre *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="67a5f-129">**IWiaItem2::GetExtension** stores the address of the extension object's extension interface in the *riidExtensionInterface* parameter.</span></span> <span data-ttu-id="67a5f-130">L’application utilise ensuite le pointeur d’interface pour appeler ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="67a5f-130">The application then uses the interface pointer to call its methods.</span></span>

<span data-ttu-id="67a5f-131">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="67a5f-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *riidExtensionInterface* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="67a5f-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="67a5f-132">Examples</span></span>

<span data-ttu-id="67a5f-133">CreateSegmentationFilter crée une instance du filtre de segmentation du pilote ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) en appelant **IWiaItem2 :: GetExtension** sur l’interface [**IWiaItem2**](-wia-iwiaitem2.md) passée.</span><span class="sxs-lookup"><span data-stu-id="67a5f-133">CreateSegmentationFilter creates an instance of the driver's segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) by calling **IWiaItem2::GetExtension** on the passed-in [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span>


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="67a5f-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67a5f-134">Requirements</span></span>



| <span data-ttu-id="67a5f-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67a5f-135">Requirement</span></span> | <span data-ttu-id="67a5f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="67a5f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67a5f-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67a5f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="67a5f-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67a5f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67a5f-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67a5f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="67a5f-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67a5f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67a5f-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="67a5f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="67a5f-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="67a5f-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="67a5f-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="67a5f-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67a5f-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67a5f-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 
