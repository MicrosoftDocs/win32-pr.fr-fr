---
description: La \_ méthode obtenir CharacterSet obtient un \_ \_ descripteur de jeu de caractères BLOB du jeu de caractères utilisé dans l’objet blob de conférence actuel.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'ITConferenceBlob :: get_CharacterSet, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541125"
---
# <a name="itconferenceblobget_characterset-method"></a><span data-ttu-id="c3d15-103">ITConferenceBlob :: obtient la \_ méthode CharacterSet</span><span class="sxs-lookup"><span data-stu-id="c3d15-103">ITConferenceBlob::get\_CharacterSet method</span></span>

<span data-ttu-id="c3d15-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c3d15-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c3d15-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="c3d15-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c3d15-106">La méthode **obtenir \_ CharacterSet** obtient un descripteur de [**\_ \_ jeu de caractères BLOB**](blob-character-set.md) du jeu de caractères utilisé dans l’objet blob de conférence actuel.</span><span class="sxs-lookup"><span data-stu-id="c3d15-106">The **get\_CharacterSet** method gets a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set used in the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d15-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3d15-107">Syntax</span></span>


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a><span data-ttu-id="c3d15-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3d15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d15-109">*pCharacterSet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3d15-109">*pCharacterSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d15-110">Pointeur vers le descripteur d’un [**\_ \_ jeu de caractères BLOB**](blob-character-set.md) du jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="c3d15-110">Pointer to a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d15-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3d15-111">Return value</span></span>

<span data-ttu-id="c3d15-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c3d15-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c3d15-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c3d15-113">Return code</span></span>                                                                                                   | <span data-ttu-id="c3d15-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3d15-114">Description</span></span>                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3d15-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-115"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="c3d15-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c3d15-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="c3d15-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-117"><dt>**E\_POINTER**</dt></span></span> </dl>                     | <span data-ttu-id="c3d15-118">Le paramètre *pCharacterSet* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="c3d15-118">The *pCharacterSet* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="c3d15-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                 | <span data-ttu-id="c3d15-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="c3d15-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="c3d15-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-121"><dt>**E\_FAIL**</dt></span></span> </dl>                        | <span data-ttu-id="c3d15-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c3d15-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c3d15-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                     | <span data-ttu-id="c3d15-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="c3d15-124">This method is not yet implemented.</span></span><br/>                   |
| <dl> <span data-ttu-id="c3d15-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                  | <span data-ttu-id="c3d15-126">*pCharacterSet* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c3d15-126">*pCharacterSet* is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="c3d15-127"><dt>**SIGNÉ ERREUR de \_ données non valides \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-127"><dt>**(HRESULT) ERROR\_INVALID\_DATA**</dt></span></span> </dl> | <span data-ttu-id="c3d15-128">Le jeu de caractères actuel n’est pas valide ou n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c3d15-128">The current character set is invalid or unavailable.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="c3d15-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3d15-129">Requirements</span></span>



| <span data-ttu-id="c3d15-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3d15-130">Requirement</span></span> | <span data-ttu-id="c3d15-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3d15-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d15-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c3d15-132">TAPI version</span></span><br/> | <span data-ttu-id="c3d15-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c3d15-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c3d15-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3d15-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c3d15-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3d15-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3d15-136">Library</span></span><br/>      | <dl> <span data-ttu-id="c3d15-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c3d15-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c3d15-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="c3d15-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3d15-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d15-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d15-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d15-141">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="c3d15-141">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="c3d15-142">**\_jeu de caractères BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="c3d15-142">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

 




