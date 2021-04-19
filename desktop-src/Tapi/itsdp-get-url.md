---
description: La méthode d’extraction d' \_ URL obtient l’URL.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'ITSdp :: get_Url, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542810"
---
# <a name="itsdpget_url-method"></a><span data-ttu-id="5607e-103">ITSdp :: obtient l' \_ URL, méthode</span><span class="sxs-lookup"><span data-stu-id="5607e-103">ITSdp::get\_Url method</span></span>

<span data-ttu-id="5607e-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5607e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5607e-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="5607e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5607e-106">La méthode d' **extraction d' \_ URL** obtient l’URL.</span><span class="sxs-lookup"><span data-stu-id="5607e-106">The **get\_Url** method gets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="5607e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5607e-107">Syntax</span></span>


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a><span data-ttu-id="5607e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5607e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5607e-109">*ppUrl* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5607e-109">*ppUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5607e-110">Pointeur vers une représentation **BSTR** de l’URL.</span><span class="sxs-lookup"><span data-stu-id="5607e-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5607e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5607e-111">Return value</span></span>

<span data-ttu-id="5607e-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="5607e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5607e-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5607e-113">Return code</span></span>                                                                                   | <span data-ttu-id="5607e-114">Description</span><span class="sxs-lookup"><span data-stu-id="5607e-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5607e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5607e-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5607e-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5607e-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5607e-118">Le paramètre *ppUrl* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="5607e-118">The *ppUrl* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="5607e-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5607e-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5607e-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5607e-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5607e-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5607e-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5607e-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5607e-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="5607e-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5607e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5607e-125">Remarks</span></span>

<span data-ttu-id="5607e-126">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppUrl* .</span><span class="sxs-lookup"><span data-stu-id="5607e-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppUrl* parameter.</span></span>

<span data-ttu-id="5607e-127">Une URL est généralement utilisée pour référencer une page Web contenant des ressources supplémentaires ou des informations générales sur une conférence.</span><span class="sxs-lookup"><span data-stu-id="5607e-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

## <a name="requirements"></a><span data-ttu-id="5607e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5607e-128">Requirements</span></span>



| <span data-ttu-id="5607e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5607e-129">Requirement</span></span> | <span data-ttu-id="5607e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="5607e-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5607e-131">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5607e-131">TAPI version</span></span><br/> | <span data-ttu-id="5607e-132">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5607e-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5607e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="5607e-133">Header</span></span><br/>       | <dl> <span data-ttu-id="5607e-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5607e-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5607e-135">Library</span></span><br/>      | <dl> <span data-ttu-id="5607e-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5607e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5607e-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="5607e-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5607e-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5607e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5607e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5607e-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="5607e-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="5607e-141">**ITSdp : URL de :p ut \_**</span><span class="sxs-lookup"><span data-stu-id="5607e-141">**ITSdp::put\_Url**</span></span>](itsdp-put-url.md)
</dt> </dl>

 

