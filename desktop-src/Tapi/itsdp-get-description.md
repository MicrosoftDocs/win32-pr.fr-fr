---
description: La \_ méthode obtenir la description obtient la description de session (BSTR).
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'ITSdp :: get_Description, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533493"
---
# <a name="itsdpget_description-method"></a><span data-ttu-id="17f90-103">ITSdp :: méthode d’extraction, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="17f90-103">ITSdp::get\_Description method</span></span>

<span data-ttu-id="17f90-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="17f90-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="17f90-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="17f90-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="17f90-106">La méthode **obtenir la \_ Description** obtient la description de session (**BSTR**).</span><span class="sxs-lookup"><span data-stu-id="17f90-106">The **get\_Description** method gets the session description (**BSTR**).</span></span> <span data-ttu-id="17f90-107">Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII.</span><span class="sxs-lookup"><span data-stu-id="17f90-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="17f90-108">(Dans le cas contraire, il peut s’agir d’une chaîne **BSTR** .)</span><span class="sxs-lookup"><span data-stu-id="17f90-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="17f90-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17f90-109">Syntax</span></span>


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a><span data-ttu-id="17f90-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17f90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f90-111">*ppDescription* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="17f90-111">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f90-112">Pointeur vers un **BSTR** contenant la description de session.</span><span class="sxs-lookup"><span data-stu-id="17f90-112">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17f90-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17f90-113">Return value</span></span>

<span data-ttu-id="17f90-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="17f90-114">This method can return one of these values.</span></span>



| <span data-ttu-id="17f90-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="17f90-115">Return code</span></span>                                                                                   | <span data-ttu-id="17f90-116">Description</span><span class="sxs-lookup"><span data-stu-id="17f90-116">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="17f90-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="17f90-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="17f90-118">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="17f90-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="17f90-120">Le paramètre *ppDescription* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="17f90-120">The *ppDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="17f90-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="17f90-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="17f90-122">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="17f90-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="17f90-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="17f90-124">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="17f90-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="17f90-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="17f90-126">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="17f90-127">Notes</span><span class="sxs-lookup"><span data-stu-id="17f90-127">Remarks</span></span>

<span data-ttu-id="17f90-128">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer le paramètre *ppDescription* .</span><span class="sxs-lookup"><span data-stu-id="17f90-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the *ppDescription* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f90-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17f90-129">Requirements</span></span>



| <span data-ttu-id="17f90-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17f90-130">Requirement</span></span> | <span data-ttu-id="17f90-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="17f90-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17f90-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="17f90-132">TAPI version</span></span><br/> | <span data-ttu-id="17f90-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="17f90-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="17f90-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="17f90-134">Header</span></span><br/>       | <dl> <span data-ttu-id="17f90-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="17f90-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17f90-136">Library</span></span><br/>      | <dl> <span data-ttu-id="17f90-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="17f90-138">DLL</span><span class="sxs-lookup"><span data-stu-id="17f90-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="17f90-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17f90-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f90-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17f90-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f90-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="17f90-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="17f90-142">**ITSdp : description de :p ut \_**</span><span class="sxs-lookup"><span data-stu-id="17f90-142">**ITSdp::put\_Description**</span></span>](itsdp-put-description.md)
</dt> </dl>

 

