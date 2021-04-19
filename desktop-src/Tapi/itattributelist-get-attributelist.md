---
description: La \_ méthode obtenir AttributeList obtient la liste des attributs.
ms.assetid: 75518257-3339-441f-9965-b93e27f0e2bf
title: 'ITAttributeList :: get_AttributeList, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499352cd5087f478e58653fd304e27101db9b433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535389"
---
# <a name="itattributelistget_attributelist-method"></a><span data-ttu-id="bdb41-103">ITAttributeList :: \_ AttributeList, méthode</span><span class="sxs-lookup"><span data-stu-id="bdb41-103">ITAttributeList::get\_AttributeList method</span></span>

<span data-ttu-id="bdb41-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bdb41-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bdb41-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bdb41-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bdb41-106">La méthode **obtenir \_ AttributeList** obtient la liste des attributs.</span><span class="sxs-lookup"><span data-stu-id="bdb41-106">The **get\_AttributeList** method gets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb41-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdb41-107">Syntax</span></span>


```C++
HRESULT get_AttributeList(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bdb41-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdb41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb41-109">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bdb41-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb41-110">Tableau d’attributs.</span><span class="sxs-lookup"><span data-stu-id="bdb41-110">Array of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb41-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdb41-111">Return value</span></span>

<span data-ttu-id="bdb41-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="bdb41-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bdb41-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bdb41-113">Return code</span></span>                                                                                   | <span data-ttu-id="bdb41-114">Description</span><span class="sxs-lookup"><span data-stu-id="bdb41-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bdb41-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bdb41-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="bdb41-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bdb41-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bdb41-118">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="bdb41-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="bdb41-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bdb41-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bdb41-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bdb41-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bdb41-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bdb41-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bdb41-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bdb41-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="bdb41-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="bdb41-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdb41-125">Requirements</span></span>



| <span data-ttu-id="bdb41-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdb41-126">Requirement</span></span> | <span data-ttu-id="bdb41-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdb41-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb41-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="bdb41-128">TAPI version</span></span><br/> | <span data-ttu-id="bdb41-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bdb41-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bdb41-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdb41-130">Header</span></span><br/>       | <dl> <span data-ttu-id="bdb41-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdb41-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bdb41-132">Library</span></span><br/>      | <dl> <span data-ttu-id="bdb41-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bdb41-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bdb41-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="bdb41-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb41-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb41-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdb41-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb41-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="bdb41-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="bdb41-138">**ITAttributeList ::p ut \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="bdb41-138">**ITAttributeList::put\_AttributeList**</span></span>](itattributelist-put-attributelist.md)
</dt> </dl>

 

 




