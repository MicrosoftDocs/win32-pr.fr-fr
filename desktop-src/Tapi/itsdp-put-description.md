---
description: La \_ méthode put Description définit la description de la session.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: ITSdp ::p ut_Description, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea8799ce9b2b8f3f44147b8ca60a92d2c37d5e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526452"
---
# <a name="itsdpput_description-method"></a><span data-ttu-id="a25bb-103">ITSdp ::p ut ( \_ méthode de Description)</span><span class="sxs-lookup"><span data-stu-id="a25bb-103">ITSdp::put\_Description method</span></span>

<span data-ttu-id="a25bb-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a25bb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a25bb-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a25bb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a25bb-106">La méthode **put \_ Description** définit la description de la session.</span><span class="sxs-lookup"><span data-stu-id="a25bb-106">The **put\_Description** method sets the session description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a25bb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a25bb-107">Syntax</span></span>


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a><span data-ttu-id="a25bb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a25bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a25bb-109">*pDescription* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a25bb-109">*pDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a25bb-110">Pointeur vers un **BSTR** contenant la description de session.</span><span class="sxs-lookup"><span data-stu-id="a25bb-110">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a25bb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a25bb-111">Return value</span></span>

<span data-ttu-id="a25bb-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a25bb-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a25bb-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a25bb-113">Return code</span></span>                                                                                   | <span data-ttu-id="a25bb-114">Description</span><span class="sxs-lookup"><span data-stu-id="a25bb-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a25bb-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a25bb-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a25bb-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a25bb-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a25bb-118">Le paramètre *pDescription* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="a25bb-118">The *pDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a25bb-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a25bb-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a25bb-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a25bb-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a25bb-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a25bb-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a25bb-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a25bb-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="a25bb-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a25bb-125">Notes</span><span class="sxs-lookup"><span data-stu-id="a25bb-125">Remarks</span></span>

<span data-ttu-id="a25bb-126">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PDescription* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a25bb-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pDescription* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="a25bb-127">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="a25bb-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="a25bb-128">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a25bb-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a25bb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a25bb-129">Requirements</span></span>



| <span data-ttu-id="a25bb-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a25bb-130">Requirement</span></span> | <span data-ttu-id="a25bb-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a25bb-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a25bb-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a25bb-132">TAPI version</span></span><br/> | <span data-ttu-id="a25bb-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a25bb-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a25bb-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a25bb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a25bb-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a25bb-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a25bb-136">Library</span></span><br/>      | <dl> <span data-ttu-id="a25bb-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a25bb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a25bb-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="a25bb-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a25bb-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a25bb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a25bb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25bb-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="a25bb-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="a25bb-142">**ITSdp :: obtient la \_ Description**</span><span class="sxs-lookup"><span data-stu-id="a25bb-142">**ITSdp::get\_Description**</span></span>](itsdp-get-description.md)
</dt> </dl>

 

