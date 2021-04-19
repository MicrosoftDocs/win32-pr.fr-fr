---
description: La \_ méthode obtenir l’expéditeur obtient l’expéditeur de la Conférence.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'ITSdp :: get_Originator, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534968"
---
# <a name="itsdpget_originator-method"></a><span data-ttu-id="3eda3-103">ITSdp :: obtient l' \_ appelant, méthode</span><span class="sxs-lookup"><span data-stu-id="3eda3-103">ITSdp::get\_Originator method</span></span>

<span data-ttu-id="3eda3-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3eda3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3eda3-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3eda3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3eda3-106">La méthode **obtenir l' \_ expéditeur** obtient l’expéditeur de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="3eda3-106">The **get\_Originator** method gets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eda3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eda3-107">Syntax</span></span>


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="3eda3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eda3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eda3-109">*ppOriginator* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3eda3-109">*ppOriginator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3eda3-110">Pointeur vers une représentation **BSTR** de l’expéditeur de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="3eda3-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eda3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eda3-111">Return value</span></span>

<span data-ttu-id="3eda3-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3eda3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3eda3-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3eda3-113">Return code</span></span>                                                                                   | <span data-ttu-id="3eda3-114">Description</span><span class="sxs-lookup"><span data-stu-id="3eda3-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3eda3-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3eda3-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="3eda3-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3eda3-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3eda3-118">Le paramètre *ppOriginator* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="3eda3-118">The *ppOriginator* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="3eda3-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3eda3-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3eda3-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3eda3-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3eda3-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3eda3-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3eda3-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3eda3-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="3eda3-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3eda3-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3eda3-125">Remarks</span></span>

<span data-ttu-id="3eda3-126">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppOriginator* .</span><span class="sxs-lookup"><span data-stu-id="3eda3-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppOriginator* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eda3-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eda3-127">Requirements</span></span>



| <span data-ttu-id="3eda3-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eda3-128">Requirement</span></span> | <span data-ttu-id="3eda3-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eda3-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3eda3-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3eda3-130">TAPI version</span></span><br/> | <span data-ttu-id="3eda3-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3eda3-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3eda3-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="3eda3-132">Header</span></span><br/>       | <dl> <span data-ttu-id="3eda3-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3eda3-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3eda3-134">Library</span></span><br/>      | <dl> <span data-ttu-id="3eda3-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3eda3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3eda3-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="3eda3-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eda3-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eda3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eda3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eda3-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="3eda3-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="3eda3-140">**ITSdp : \_ :p ut**</span><span class="sxs-lookup"><span data-stu-id="3eda3-140">**ITSdp::put\_Originator**</span></span>](itsdp-put-originator.md)
</dt> </dl>

 

