---
description: La méthode Delete supprime l’attribut au niveau de l’index spécifié.
ms.assetid: 6bc6f3d2-d630-4a00-9d74-fb5fa7626e3f
title: ITAttributeList ::D méthode supprimable (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729dd79b88198f671949aeb79caf06289abd9a75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535390"
---
# <a name="itattributelistdelete-method"></a><span data-ttu-id="d1dff-103">ITAttributeList ::D méthode supprimable</span><span class="sxs-lookup"><span data-stu-id="d1dff-103">ITAttributeList::Delete method</span></span>

<span data-ttu-id="d1dff-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d1dff-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d1dff-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d1dff-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d1dff-106">La méthode **Delete** supprime l’attribut au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="d1dff-106">The **Delete** method deletes the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1dff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1dff-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="d1dff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1dff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1dff-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1dff-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1dff-110">Index de l’attribut à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d1dff-110">Index of the attribute to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1dff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1dff-111">Return value</span></span>

<span data-ttu-id="d1dff-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d1dff-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d1dff-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d1dff-113">Return code</span></span>                                                                                   | <span data-ttu-id="d1dff-114">Description</span><span class="sxs-lookup"><span data-stu-id="d1dff-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d1dff-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d1dff-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="d1dff-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d1dff-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d1dff-118">Le paramètre d' *index* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d1dff-118">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="d1dff-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d1dff-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d1dff-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d1dff-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d1dff-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d1dff-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d1dff-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d1dff-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="d1dff-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d1dff-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1dff-125">Requirements</span></span>



| <span data-ttu-id="d1dff-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1dff-126">Requirement</span></span> | <span data-ttu-id="d1dff-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1dff-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1dff-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d1dff-128">TAPI version</span></span><br/> | <span data-ttu-id="d1dff-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d1dff-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d1dff-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1dff-130">Header</span></span><br/>       | <dl> <span data-ttu-id="d1dff-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1dff-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1dff-132">Library</span></span><br/>      | <dl> <span data-ttu-id="d1dff-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d1dff-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d1dff-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="d1dff-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1dff-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1dff-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1dff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1dff-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="d1dff-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




