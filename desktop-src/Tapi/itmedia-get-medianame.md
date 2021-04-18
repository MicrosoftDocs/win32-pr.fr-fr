---
description: La \_ méthode obtenir MEDIANAME obtient le nom du support. Les médias définis sont audio, vidéo, tableau blanc, texte et données.
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'ITMedia :: get_MediaName, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9152994eac98d5e846ac147072a51a3334930da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526843"
---
# <a name="itmediaget_medianame-method"></a><span data-ttu-id="98fb1-104">ITMedia :: obtient la \_ méthode MEDIANAME</span><span class="sxs-lookup"><span data-stu-id="98fb1-104">ITMedia::get\_MediaName method</span></span>

<span data-ttu-id="98fb1-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="98fb1-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="98fb1-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="98fb1-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="98fb1-107">La méthode **obtenir \_ MEDIANAME** obtient le nom du support.</span><span class="sxs-lookup"><span data-stu-id="98fb1-107">The **get\_MediaName** method gets the media name.</span></span> <span data-ttu-id="98fb1-108">Les médias définis sont audio, vidéo, tableau blanc, texte et données.</span><span class="sxs-lookup"><span data-stu-id="98fb1-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="98fb1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98fb1-109">Syntax</span></span>


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="98fb1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98fb1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98fb1-111">*ppMediaName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="98fb1-111">*ppMediaName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98fb1-112">Pointeur vers un **BSTR** contenant le nom du média, tel que l’audio.</span><span class="sxs-lookup"><span data-stu-id="98fb1-112">Pointer to a **BSTR** containing the name of the media, such as audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98fb1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98fb1-113">Return value</span></span>

<span data-ttu-id="98fb1-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="98fb1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="98fb1-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="98fb1-115">Return code</span></span>                                                                                   | <span data-ttu-id="98fb1-116">Description</span><span class="sxs-lookup"><span data-stu-id="98fb1-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="98fb1-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="98fb1-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="98fb1-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="98fb1-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="98fb1-120">Le paramètre *ppMediaName* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="98fb1-120">The *ppMediaName* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="98fb1-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="98fb1-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="98fb1-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="98fb1-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="98fb1-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="98fb1-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="98fb1-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="98fb1-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="98fb1-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="98fb1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="98fb1-127">Remarks</span></span>

<span data-ttu-id="98fb1-128">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppMediaName* .</span><span class="sxs-lookup"><span data-stu-id="98fb1-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="98fb1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98fb1-129">Requirements</span></span>



| <span data-ttu-id="98fb1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98fb1-130">Requirement</span></span> | <span data-ttu-id="98fb1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="98fb1-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98fb1-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="98fb1-132">TAPI version</span></span><br/> | <span data-ttu-id="98fb1-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="98fb1-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="98fb1-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="98fb1-134">Header</span></span><br/>       | <dl> <span data-ttu-id="98fb1-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="98fb1-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="98fb1-136">Library</span></span><br/>      | <dl> <span data-ttu-id="98fb1-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="98fb1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="98fb1-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="98fb1-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98fb1-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98fb1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98fb1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fb1-141">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="98fb1-141">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="98fb1-142">**ITMedia ::p ut \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="98fb1-142">**ITMedia::put\_MediaName**</span></span>](itmedia-put-medianame.md)
</dt> </dl>

 

