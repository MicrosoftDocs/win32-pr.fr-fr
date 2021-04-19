---
description: La \_ méthode obtenir ConferenceBlob obtient un pointeur vers l’objet blob de conférence textuel actuellement stocké dans l’objet blob de conférence.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'ITConferenceBlob :: get_ConferenceBlob, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530526"
---
# <a name="itconferenceblobget_conferenceblob-method"></a><span data-ttu-id="86e10-103">ITConferenceBlob :: \_ ConferenceBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="86e10-103">ITConferenceBlob::get\_ConferenceBlob method</span></span>

<span data-ttu-id="86e10-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="86e10-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86e10-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="86e10-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86e10-106">La méthode **obtenir \_ ConferenceBlob** obtient un pointeur vers l’objet blob de conférence textuel actuellement stocké dans l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="86e10-106">The **get\_ConferenceBlob** method gets a pointer to the textual conference blob currently stored in the conference blob object.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e10-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86e10-107">Syntax</span></span>


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a><span data-ttu-id="86e10-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86e10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e10-109">*ppBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86e10-109">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86e10-110">Pointeur vers un **BSTR** contenant l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="86e10-110">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e10-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86e10-111">Return value</span></span>

<span data-ttu-id="86e10-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="86e10-112">This method can return one of these values.</span></span>



| <span data-ttu-id="86e10-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="86e10-113">Return code</span></span>                                                                                   | <span data-ttu-id="86e10-114">Description</span><span class="sxs-lookup"><span data-stu-id="86e10-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="86e10-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86e10-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="86e10-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="86e10-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="86e10-118">Le paramètre *ppBlob* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="86e10-118">The *ppBlob* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="86e10-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86e10-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="86e10-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="86e10-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="86e10-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="86e10-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86e10-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="86e10-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="86e10-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="86e10-125">Notes</span><span class="sxs-lookup"><span data-stu-id="86e10-125">Remarks</span></span>

<span data-ttu-id="86e10-126">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppBlob* .</span><span class="sxs-lookup"><span data-stu-id="86e10-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppBlob* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e10-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86e10-127">Requirements</span></span>



| <span data-ttu-id="86e10-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86e10-128">Requirement</span></span> | <span data-ttu-id="86e10-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="86e10-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86e10-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="86e10-130">TAPI version</span></span><br/> | <span data-ttu-id="86e10-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="86e10-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86e10-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="86e10-132">Header</span></span><br/>       | <dl> <span data-ttu-id="86e10-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="86e10-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86e10-134">Library</span></span><br/>      | <dl> <span data-ttu-id="86e10-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86e10-136">DLL</span><span class="sxs-lookup"><span data-stu-id="86e10-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="86e10-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e10-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86e10-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e10-139">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="86e10-139">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="86e10-140">**\_jeu de caractères BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="86e10-140">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

