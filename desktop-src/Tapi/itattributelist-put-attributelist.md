---
description: La \_ méthode put AttributeList définit la liste des attributs.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: ITAttributeList ::p ut_AttributeList, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3876b2cd8ecdef46a933ff3f3c91be96dd028892
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543329"
---
# <a name="itattributelistput_attributelist-method"></a><span data-ttu-id="78ce4-103">ITAttributeList ::p ut \_ AttributeList, méthode</span><span class="sxs-lookup"><span data-stu-id="78ce4-103">ITAttributeList::put\_AttributeList method</span></span>

<span data-ttu-id="78ce4-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="78ce4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="78ce4-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="78ce4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="78ce4-106">La méthode **put \_ AttributeList** définit la liste des attributs.</span><span class="sxs-lookup"><span data-stu-id="78ce4-106">The **put\_AttributeList** method sets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ce4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78ce4-107">Syntax</span></span>


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="78ce4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78ce4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78ce4-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="78ce4-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ce4-110">Tableau d’attributs à définir.</span><span class="sxs-lookup"><span data-stu-id="78ce4-110">Array of attributes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78ce4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78ce4-111">Return value</span></span>

<span data-ttu-id="78ce4-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="78ce4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="78ce4-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="78ce4-113">Return code</span></span>                                                                                   | <span data-ttu-id="78ce4-114">Description</span><span class="sxs-lookup"><span data-stu-id="78ce4-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="78ce4-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="78ce4-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="78ce4-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="78ce4-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="78ce4-118">Le paramètre *newVal* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="78ce4-118">The *newVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="78ce4-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="78ce4-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="78ce4-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="78ce4-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="78ce4-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="78ce4-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="78ce4-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="78ce4-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="78ce4-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="78ce4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78ce4-125">Requirements</span></span>



| <span data-ttu-id="78ce4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78ce4-126">Requirement</span></span> | <span data-ttu-id="78ce4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="78ce4-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78ce4-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="78ce4-128">TAPI version</span></span><br/> | <span data-ttu-id="78ce4-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="78ce4-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="78ce4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="78ce4-130">Header</span></span><br/>       | <dl> <span data-ttu-id="78ce4-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="78ce4-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78ce4-132">Library</span></span><br/>      | <dl> <span data-ttu-id="78ce4-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="78ce4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="78ce4-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="78ce4-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78ce4-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78ce4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ce4-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="78ce4-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="78ce4-138">**ITAttributeList :: obtient \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="78ce4-138">**ITAttributeList::get\_AttributeList**</span></span>](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




