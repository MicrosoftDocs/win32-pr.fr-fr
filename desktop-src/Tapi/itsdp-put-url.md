---
description: La \_ méthode put URL définit l’URL.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: ITSdp ::p ut_Url, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533112"
---
# <a name="itsdpput_url-method"></a><span data-ttu-id="543e4-103">ITSdp ::p \_ méthode d’URL ut</span><span class="sxs-lookup"><span data-stu-id="543e4-103">ITSdp::put\_Url method</span></span>

<span data-ttu-id="543e4-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="543e4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="543e4-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="543e4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="543e4-106">La méthode **put \_ URL** définit l’URL.</span><span class="sxs-lookup"><span data-stu-id="543e4-106">The **put\_Url** method sets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="543e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="543e4-107">Syntax</span></span>


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a><span data-ttu-id="543e4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="543e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="543e4-109">*purl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="543e4-109">*pUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="543e4-110">Pointeur vers une représentation **BSTR** de l’URL.</span><span class="sxs-lookup"><span data-stu-id="543e4-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="543e4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="543e4-111">Return value</span></span>

<span data-ttu-id="543e4-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="543e4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="543e4-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="543e4-113">Return code</span></span>                                                                                   | <span data-ttu-id="543e4-114">Description</span><span class="sxs-lookup"><span data-stu-id="543e4-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="543e4-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="543e4-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="543e4-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="543e4-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="543e4-118">Le paramètre *purl* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="543e4-118">The *pUrl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="543e4-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="543e4-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="543e4-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="543e4-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="543e4-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="543e4-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="543e4-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="543e4-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="543e4-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="543e4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="543e4-125">Remarks</span></span>

<span data-ttu-id="543e4-126">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PUrl* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="543e4-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pUrl* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="543e4-127">Une URL est généralement utilisée pour référencer une page Web contenant des ressources supplémentaires ou des informations générales sur une conférence.</span><span class="sxs-lookup"><span data-stu-id="543e4-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

<span data-ttu-id="543e4-128">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="543e4-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="543e4-129">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="543e4-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="543e4-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="543e4-130">Requirements</span></span>



| <span data-ttu-id="543e4-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="543e4-131">Requirement</span></span> | <span data-ttu-id="543e4-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="543e4-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="543e4-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="543e4-133">TAPI version</span></span><br/> | <span data-ttu-id="543e4-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="543e4-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="543e4-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="543e4-135">Header</span></span><br/>       | <dl> <span data-ttu-id="543e4-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="543e4-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="543e4-137">Library</span></span><br/>      | <dl> <span data-ttu-id="543e4-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="543e4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="543e4-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="543e4-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="543e4-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="543e4-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="543e4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="543e4-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="543e4-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="543e4-143">**ITSdp :: obtient l' \_ URL**</span><span class="sxs-lookup"><span data-stu-id="543e4-143">**ITSdp::get\_Url**</span></span>](itsdp-get-url.md)
</dt> </dl>

 

