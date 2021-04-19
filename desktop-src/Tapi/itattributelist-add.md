---
description: La méthode Add ajoute l’attribut à l’index spécifié.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'ITAttributeList :: Add, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525660"
---
# <a name="itattributelistadd-method"></a><span data-ttu-id="f8266-103">ITAttributeList :: Add, méthode</span><span class="sxs-lookup"><span data-stu-id="f8266-103">ITAttributeList::Add method</span></span>

<span data-ttu-id="f8266-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f8266-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f8266-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f8266-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f8266-106">La méthode **Add** ajoute l’attribut à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f8266-106">The **Add** method adds the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8266-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8266-107">Syntax</span></span>


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="f8266-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8266-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8266-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8266-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8266-110">Index de l’attribut à ajouter.</span><span class="sxs-lookup"><span data-stu-id="f8266-110">Index of the attribute to add.</span></span>

</dd> <dt>

<span data-ttu-id="f8266-111">*pAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8266-111">*pAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8266-112">Pointeur vers un **BSTR** contenant la valeur de l’attribut à ajouter.</span><span class="sxs-lookup"><span data-stu-id="f8266-112">Pointer to a **BSTR** containing the value of the attribute to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8266-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8266-113">Return value</span></span>

<span data-ttu-id="f8266-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f8266-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f8266-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f8266-115">Return code</span></span>                                                                                   | <span data-ttu-id="f8266-116">Description</span><span class="sxs-lookup"><span data-stu-id="f8266-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f8266-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f8266-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f8266-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f8266-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f8266-120">Le paramètre *index* ou *pAttribute* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f8266-120">The *Index* or *pAttribute* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f8266-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f8266-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f8266-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f8266-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f8266-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8266-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f8266-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f8266-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="f8266-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f8266-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f8266-127">Remarks</span></span>

<span data-ttu-id="f8266-128">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PAttribute* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f8266-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAttribute* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8266-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8266-129">Requirements</span></span>



| <span data-ttu-id="f8266-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8266-130">Requirement</span></span> | <span data-ttu-id="f8266-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8266-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8266-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f8266-132">TAPI version</span></span><br/> | <span data-ttu-id="f8266-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f8266-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f8266-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8266-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f8266-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8266-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8266-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f8266-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f8266-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f8266-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f8266-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8266-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8266-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8266-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8266-141">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="f8266-141">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

