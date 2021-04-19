---
description: La méthode SetConferenceBlob valide les modifications apportées à l’objet blob de conférence. Pour initialiser l’objet blob de conférence pour la première fois, utilisez la méthode Init à la place.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'ITConferenceBlob :: SetConferenceBlob, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539670"
---
# <a name="itconferenceblobsetconferenceblob-method"></a><span data-ttu-id="5a62b-104">ITConferenceBlob :: SetConferenceBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="5a62b-104">ITConferenceBlob::SetConferenceBlob method</span></span>

<span data-ttu-id="5a62b-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5a62b-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a62b-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="5a62b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5a62b-107">La méthode **SetConferenceBlob** valide les modifications apportées à l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="5a62b-107">The **SetConferenceBlob** method commits changes to the conference blob.</span></span> <span data-ttu-id="5a62b-108">Pour initialiser l’objet blob de conférence pour la première fois, utilisez la méthode [**init**](itconferenceblob-init.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="5a62b-108">To initialize the conference blob for the first time, use the [**Init**](itconferenceblob-init.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a62b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a62b-109">Syntax</span></span>


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="5a62b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a62b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a62b-111">*CharacterSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a62b-111">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a62b-112">[**Objet BLOB \_ \_**](blob-character-set.md) Descripteur du jeu de caractères du jeu de caractères de l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="5a62b-112">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the conference blob's character set.</span></span>

</dd> <dt>

<span data-ttu-id="5a62b-113">*pBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a62b-113">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a62b-114">Pointeur vers un **BSTR** contenant l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="5a62b-114">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a62b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a62b-115">Return value</span></span>

<span data-ttu-id="5a62b-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="5a62b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="5a62b-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5a62b-117">Return code</span></span>                                                                                   | <span data-ttu-id="5a62b-118">Description</span><span class="sxs-lookup"><span data-stu-id="5a62b-118">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a62b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5a62b-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5a62b-120">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5a62b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5a62b-122">Le paramètre *CharacterSet* ou *pBlob* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a62b-122">The *CharacterSet* or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="5a62b-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5a62b-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5a62b-124">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="5a62b-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5a62b-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5a62b-126">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5a62b-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5a62b-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="5a62b-128">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="5a62b-129">Notes</span><span class="sxs-lookup"><span data-stu-id="5a62b-129">Remarks</span></span>

<span data-ttu-id="5a62b-130">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PBlob* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5a62b-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pBlob* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a62b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a62b-131">Requirements</span></span>



| <span data-ttu-id="5a62b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a62b-132">Requirement</span></span> | <span data-ttu-id="5a62b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a62b-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a62b-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5a62b-134">TAPI version</span></span><br/> | <span data-ttu-id="5a62b-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5a62b-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5a62b-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a62b-136">Header</span></span><br/>       | <dl> <span data-ttu-id="5a62b-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a62b-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a62b-138">Library</span></span><br/>      | <dl> <span data-ttu-id="5a62b-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5a62b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5a62b-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="5a62b-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a62b-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a62b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a62b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a62b-143">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="5a62b-143">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="5a62b-144">**\_jeu de caractères BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="5a62b-144">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

