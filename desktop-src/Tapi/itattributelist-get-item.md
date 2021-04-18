---
description: La méthode d’extraction \_ d’élément retourne l’attribut spécifié par l’index.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'ITAttributeList :: get_Item, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543330"
---
# <a name="itattributelistget_item-method"></a><span data-ttu-id="b5c4c-103">ITAttributeList :: obten, \_ méthode d’élément</span><span class="sxs-lookup"><span data-stu-id="b5c4c-103">ITAttributeList::get\_Item method</span></span>

<span data-ttu-id="b5c4c-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b5c4c-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="b5c4c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b5c4c-106">La méthode d' **extraction d' \_ élément** retourne l’attribut spécifié par l’index.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-106">The **get\_Item** method returns the attribute specified by the index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c4c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5c4c-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b5c4c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5c4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c4c-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5c4c-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c4c-110">Index de l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="b5c4c-111">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b5c4c-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c4c-112">Pointeur vers un **BSTR** contenant les valeurs de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-112">Pointer to a **BSTR** containing the values of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c4c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5c4c-113">Return value</span></span>

<span data-ttu-id="b5c4c-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b5c4c-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b5c4c-115">Return code</span></span>                                                                                   | <span data-ttu-id="b5c4c-116">Description</span><span class="sxs-lookup"><span data-stu-id="b5c4c-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b5c4c-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b5c4c-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b5c4c-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b5c4c-120">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="b5c4c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b5c4c-122">Le paramètre d' *index* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="b5c4c-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b5c4c-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b5c4c-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b5c4c-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b5c4c-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b5c4c-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b5c4c-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b5c4c-129">Remarks</span></span>

<span data-ttu-id="b5c4c-130">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *pval* .</span><span class="sxs-lookup"><span data-stu-id="b5c4c-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *pVal* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c4c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5c4c-131">Requirements</span></span>



| <span data-ttu-id="b5c4c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5c4c-132">Requirement</span></span> | <span data-ttu-id="b5c4c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5c4c-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c4c-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b5c4c-134">TAPI version</span></span><br/> | <span data-ttu-id="b5c4c-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b5c4c-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b5c4c-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5c4c-136">Header</span></span><br/>       | <dl> <span data-ttu-id="b5c4c-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5c4c-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5c4c-138">Library</span></span><br/>      | <dl> <span data-ttu-id="b5c4c-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b5c4c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b5c4c-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="b5c4c-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5c4c-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c4c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5c4c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c4c-143">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="b5c4c-143">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

