---
description: La méthode Init Initialise l’objet blob de conférence en fonction d’une chaîne textuelle. Si pBlob a la valeur NULL, les valeurs par défaut sont utilisées.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'ITConferenceBlob :: Init, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528133"
---
# <a name="itconferenceblobinit-method"></a><span data-ttu-id="40b04-104">ITConferenceBlob :: Init, méthode</span><span class="sxs-lookup"><span data-stu-id="40b04-104">ITConferenceBlob::Init method</span></span>

<span data-ttu-id="40b04-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="40b04-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="40b04-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="40b04-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="40b04-107">La méthode **init** Initialise l’objet blob de conférence en fonction d’une chaîne textuelle.</span><span class="sxs-lookup"><span data-stu-id="40b04-107">The **Init** method initializes the conference blob based on a textual string.</span></span> <span data-ttu-id="40b04-108">Si *pBlob* a la **valeur null**, les valeurs par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="40b04-108">If *pBlob* is **NULL**, default values are used.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b04-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40b04-109">Syntax</span></span>


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="40b04-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40b04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40b04-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40b04-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b04-112">Pointeur vers une représentation **BSTR** du nom de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="40b04-112">Pointer to a **BSTR** representation of the conference name.</span></span>

</dd> <dt>

<span data-ttu-id="40b04-113">*CharacterSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40b04-113">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b04-114">[**Objet BLOB \_ Descripteur du jeu \_ de**](blob-character-set.md) caractères du jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="40b04-114">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> <dt>

<span data-ttu-id="40b04-115">*pBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40b04-115">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b04-116">Pointeur vers un **BSTR** contenant l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="40b04-116">Pointer to a **BSTR** containing the conference blob.</span></span> <span data-ttu-id="40b04-117">Si la **valeur est null**, l’objet blob de conférence est initialisé avec les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="40b04-117">If **NULL**, the conference blob is initialized with default values.</span></span> <span data-ttu-id="40b04-118">Actuellement, les valeurs de conférence par défaut sont disponibles uniquement si le paramètre *CharacterSet* est défini sur BCS \_ ASCII.</span><span class="sxs-lookup"><span data-stu-id="40b04-118">Currently, default conference values are available only if the *CharacterSet* parameter is set to BCS\_ASCII.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40b04-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40b04-119">Return value</span></span>

<span data-ttu-id="40b04-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="40b04-120">This method can return one of these values.</span></span>



| <span data-ttu-id="40b04-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="40b04-121">Value</span></span>                                                                                         | <span data-ttu-id="40b04-122">Signification</span><span class="sxs-lookup"><span data-stu-id="40b04-122">Meaning</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40b04-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="40b04-124">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="40b04-124">Method succeeded.</span></span><br/>                                               |
| <dl> <span data-ttu-id="40b04-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="40b04-126">Le paramètre *pname*, *CharacterSet* ou *pBlob* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="40b04-126">The *pName*, *CharacterSet*, or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="40b04-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="40b04-128">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="40b04-128">Insufficient memory exists to perform the operation.</span></span><br/>            |
| <dl> <span data-ttu-id="40b04-129"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-129"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="40b04-130">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40b04-130">Unspecified error.</span></span><br/>                                              |
| <dl> <span data-ttu-id="40b04-131"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-131"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="40b04-132">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="40b04-132">This method is not yet implemented.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="40b04-133">Notes</span><span class="sxs-lookup"><span data-stu-id="40b04-133">Remarks</span></span>

<span data-ttu-id="40b04-134">**ITConferenceBlob :: init** retourne un échec si l’objet BLOB a déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="40b04-134">**ITConferenceBlob::Init** will return a failure if the blob has already been initialized.</span></span>

<span data-ttu-id="40b04-135">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire aux paramètres *pname* et *pBlob* .</span><span class="sxs-lookup"><span data-stu-id="40b04-135">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* and *pBlob* parameters.</span></span> <span data-ttu-id="40b04-136">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque les variables ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="40b04-136">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="40b04-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40b04-137">Requirements</span></span>



| <span data-ttu-id="40b04-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40b04-138">Requirement</span></span> | <span data-ttu-id="40b04-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="40b04-139">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40b04-140">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="40b04-140">TAPI version</span></span><br/> | <span data-ttu-id="40b04-141">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="40b04-141">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="40b04-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="40b04-142">Header</span></span><br/>       | <dl> <span data-ttu-id="40b04-143"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-143"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="40b04-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40b04-144">Library</span></span><br/>      | <dl> <span data-ttu-id="40b04-145"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-145"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="40b04-146">DLL</span><span class="sxs-lookup"><span data-stu-id="40b04-146">DLL</span></span><br/>          | <dl> <span data-ttu-id="40b04-147"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40b04-147"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40b04-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40b04-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b04-149">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="40b04-149">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="40b04-150">**\_jeu de caractères BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="40b04-150">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

