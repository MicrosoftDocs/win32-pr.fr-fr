---
description: 'Vérifie si une extension spécifiée est disponible sur l’ordinateur et si elle peut être utilisée par la méthode IWiaItem2 :: GetExtension.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2 :: CheckExtension, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518552"
---
# <a name="iwiaitem2checkextension-method"></a><span data-ttu-id="81829-103">IWiaItem2 :: CheckExtension, méthode</span><span class="sxs-lookup"><span data-stu-id="81829-103">IWiaItem2::CheckExtension method</span></span>

<span data-ttu-id="81829-104">Vérifie si une extension spécifiée est disponible sur l’ordinateur et si elle peut être utilisée par la méthode [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="81829-104">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81829-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81829-105">Syntax</span></span>


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a><span data-ttu-id="81829-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81829-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81829-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81829-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81829-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="81829-108">Type: **LONG**</span></span>

<span data-ttu-id="81829-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="81829-109">Currently unused.</span></span> <span data-ttu-id="81829-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="81829-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="81829-111">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81829-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81829-112">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="81829-112">Type: **BSTR**</span></span>

<span data-ttu-id="81829-113">Spécifie le nom de l'extension.</span><span class="sxs-lookup"><span data-stu-id="81829-113">Specifies the name of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="81829-114">*riidExtensionInterface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81829-114">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81829-115">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="81829-115">Type: **REFIID**</span></span>

<span data-ttu-id="81829-116">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="81829-116">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="81829-117">*pbExtensionExists* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="81829-117">*pbExtensionExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81829-118">Type : \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="81829-118">Type: \**BOOL\** _</span></span>

<span data-ttu-id="81829-119">Reçoit un pointeur vers un _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="81829-119">Receives a pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="81829-120"><span id="FALSE"></span><span id="false"></span>**FAUSSES**</span><span class="sxs-lookup"><span data-stu-id="81829-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="81829-121">L’extension spécifiée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="81829-121">The specified extension is not available.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="81829-122"><span id="TRUE"></span><span id="true"></span>**:**</span><span class="sxs-lookup"><span data-stu-id="81829-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="81829-123">L’extension spécifiée est disponible.</span><span class="sxs-lookup"><span data-stu-id="81829-123">The specified extension is available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81829-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81829-124">Return value</span></span>

<span data-ttu-id="81829-125">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="81829-125">Type: **HRESULT**</span></span>

<span data-ttu-id="81829-126">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="81829-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81829-127">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81829-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81829-128">Notes</span><span class="sxs-lookup"><span data-stu-id="81829-128">Remarks</span></span>

<span data-ttu-id="81829-129">À l’aide de cette méthode, les applications peuvent vérifier si une extension est disponible avant d’appeler la méthode [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="81829-129">Using this method, applications can check whether an extension is available before calling the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <span data-ttu-id="81829-130">En outre, l’application peut vérifier les extensions qui sont disponibles sans co-créer chacune d’elles, puis choisir celle qui doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="81829-130">Also, the application can check which extensions are available without co-creating each of them, and then decide which one to use.</span></span>

## <a name="examples"></a><span data-ttu-id="81829-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="81829-131">Examples</span></span>

<span data-ttu-id="81829-132">CheckImgFilter vérifie si le pilote a un filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="81829-132">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="81829-133">Avant d’appeler la version préliminaire du composant, une application doit s’assurer que le pilote possède un filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="81829-133">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a><span data-ttu-id="81829-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81829-134">Requirements</span></span>



| <span data-ttu-id="81829-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81829-135">Requirement</span></span> | <span data-ttu-id="81829-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="81829-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81829-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81829-137">Minimum supported client</span></span><br/> | <span data-ttu-id="81829-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81829-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="81829-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81829-139">Minimum supported server</span></span><br/> | <span data-ttu-id="81829-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81829-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="81829-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="81829-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="81829-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="81829-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="81829-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="81829-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81829-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81829-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 




