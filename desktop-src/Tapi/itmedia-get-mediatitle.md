---
description: La \_ méthode obtenir MediaTitle récupère un titre textuel pour le média que l’application peut utiliser à des fins d’information ou d’affichage. Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII. Dans le cas contraire, il peut s’agir de n’importe quelle chaîne BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'ITMedia :: get_MediaTitle, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535985"
---
# <a name="itmediaget_mediatitle-method"></a><span data-ttu-id="9e8ed-105">ITMedia :: \_ MediaTitle, méthode</span><span class="sxs-lookup"><span data-stu-id="9e8ed-105">ITMedia::get\_MediaTitle method</span></span>

<span data-ttu-id="9e8ed-106">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9e8ed-107">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="9e8ed-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9e8ed-108">La méthode **obtenir \_ MediaTitle** récupère un titre textuel pour le média que l’application peut utiliser à des fins d’information ou d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-108">The **get\_MediaTitle** method retrieves a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="9e8ed-109">Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="9e8ed-110">Dans le cas contraire, il peut s’agir de n’importe quelle chaîne **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="9e8ed-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8ed-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e8ed-111">Syntax</span></span>


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="9e8ed-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e8ed-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e8ed-113">*ppMediaTitle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e8ed-113">*ppMediaTitle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8ed-114">Pointeur vers un **BSTR** contenant le titre du média.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e8ed-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e8ed-115">Return value</span></span>

<span data-ttu-id="9e8ed-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-116">This method can return one of these values.</span></span>



| <span data-ttu-id="9e8ed-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9e8ed-117">Return code</span></span>                                                                                   | <span data-ttu-id="9e8ed-118">Description</span><span class="sxs-lookup"><span data-stu-id="9e8ed-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9e8ed-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9e8ed-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9e8ed-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9e8ed-122">Le paramètre *ppMediaTitle* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-122">The *ppMediaTitle* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="9e8ed-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9e8ed-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9e8ed-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9e8ed-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9e8ed-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9e8ed-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="9e8ed-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9e8ed-129">Notes</span><span class="sxs-lookup"><span data-stu-id="9e8ed-129">Remarks</span></span>

<span data-ttu-id="9e8ed-130">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppMediaTitle* .</span><span class="sxs-lookup"><span data-stu-id="9e8ed-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaTitle* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8ed-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e8ed-131">Requirements</span></span>



| <span data-ttu-id="9e8ed-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e8ed-132">Requirement</span></span> | <span data-ttu-id="9e8ed-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e8ed-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8ed-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="9e8ed-134">TAPI version</span></span><br/> | <span data-ttu-id="9e8ed-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9e8ed-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9e8ed-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e8ed-136">Header</span></span><br/>       | <dl> <span data-ttu-id="9e8ed-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e8ed-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e8ed-138">Library</span></span><br/>      | <dl> <span data-ttu-id="9e8ed-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9e8ed-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8ed-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="9e8ed-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ed-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e8ed-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e8ed-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8ed-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="9e8ed-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="9e8ed-144">**ITMedia ::P ut \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="9e8ed-144">**ITMedia::Put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)
</dt> </dl>

 

