---
description: La \_ méthode put MediaTitle définit un titre textuel pour le média que l’application peut utiliser à des fins d’information ou d’affichage. Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII. Dans le cas contraire, il peut s’agir de n’importe quelle chaîne BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: ITMedia ::p ut_MediaTitle, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522785"
---
# <a name="itmediaput_mediatitle-method"></a><span data-ttu-id="528d8-105">ITMedia ::p ut \_ MediaTitle, méthode</span><span class="sxs-lookup"><span data-stu-id="528d8-105">ITMedia::put\_MediaTitle method</span></span>

<span data-ttu-id="528d8-106">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="528d8-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="528d8-107">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="528d8-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="528d8-108">La méthode **put \_ MediaTitle** définit un titre textuel pour le média que l’application peut utiliser à des fins d’information ou d’affichage.</span><span class="sxs-lookup"><span data-stu-id="528d8-108">The **put\_MediaTitle** method sets a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="528d8-109">Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII.</span><span class="sxs-lookup"><span data-stu-id="528d8-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="528d8-110">Dans le cas contraire, il peut s’agir de n’importe quelle chaîne **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="528d8-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="528d8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="528d8-111">Syntax</span></span>


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="528d8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="528d8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="528d8-113">*pMediaTitle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="528d8-113">*pMediaTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="528d8-114">Pointeur vers un **BSTR** contenant le titre du média.</span><span class="sxs-lookup"><span data-stu-id="528d8-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="528d8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="528d8-115">Return value</span></span>

<span data-ttu-id="528d8-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="528d8-116">This method can return one of these values.</span></span>



| <span data-ttu-id="528d8-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="528d8-117">Return code</span></span>                                                                                   | <span data-ttu-id="528d8-118">Description</span><span class="sxs-lookup"><span data-stu-id="528d8-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="528d8-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="528d8-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="528d8-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="528d8-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="528d8-122">Le paramètre *pMediaTitle* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="528d8-122">The *pMediaTitle* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="528d8-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="528d8-124">Le paramètre *pMediaTitle* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="528d8-124">The *pMediaTitle* parameter is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="528d8-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="528d8-126">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="528d8-126">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="528d8-127"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-127"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="528d8-128">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="528d8-128">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="528d8-129"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-129"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="528d8-130">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="528d8-130">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="528d8-131">Notes</span><span class="sxs-lookup"><span data-stu-id="528d8-131">Remarks</span></span>

<span data-ttu-id="528d8-132">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PMediaTitle* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="528d8-132">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaTitle* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="528d8-133">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="528d8-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="528d8-134">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="528d8-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="528d8-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="528d8-135">Requirements</span></span>



| <span data-ttu-id="528d8-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="528d8-136">Requirement</span></span> | <span data-ttu-id="528d8-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="528d8-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="528d8-138">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="528d8-138">TAPI version</span></span><br/> | <span data-ttu-id="528d8-139">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="528d8-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="528d8-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="528d8-140">Header</span></span><br/>       | <dl> <span data-ttu-id="528d8-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="528d8-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="528d8-142">Library</span></span><br/>      | <dl> <span data-ttu-id="528d8-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="528d8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="528d8-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="528d8-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="528d8-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="528d8-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="528d8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528d8-147">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="528d8-147">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="528d8-148">**ITMedia :: obtient \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="528d8-148">**ITMedia::get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)
</dt> </dl>

 

