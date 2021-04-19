---
description: La méthode SetEmailNames définit un tableau d’adresses de messagerie associées à l’objet blob de conférence.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'ITSdp :: SetEmailNames, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539231"
---
# <a name="itsdpsetemailnames-method"></a><span data-ttu-id="79e2f-103">ITSdp :: SetEmailNames, méthode</span><span class="sxs-lookup"><span data-stu-id="79e2f-103">ITSdp::SetEmailNames method</span></span>

<span data-ttu-id="79e2f-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="79e2f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="79e2f-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="79e2f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="79e2f-106">La méthode **SetEmailNames** définit un tableau d’adresses de messagerie associées à l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="79e2f-106">The **SetEmailNames** method sets an array of e-mail addresses associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e2f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79e2f-107">Syntax</span></span>


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="79e2f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79e2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79e2f-109">*Adresses* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e2f-109">*Addresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e2f-110">SAFEARRAY de **BSTR** répertoriant les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="79e2f-110">SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="79e2f-111">*Noms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e2f-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e2f-112">SAFEARRAY de noms de liste de **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="79e2f-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79e2f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79e2f-113">Return value</span></span>

<span data-ttu-id="79e2f-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="79e2f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="79e2f-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="79e2f-115">Return code</span></span>                                                                                   | <span data-ttu-id="79e2f-116">Description</span><span class="sxs-lookup"><span data-stu-id="79e2f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="79e2f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="79e2f-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="79e2f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="79e2f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="79e2f-120">Le paramètre des *adresses* ou des *noms* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="79e2f-120">The *Addresses* or *Names* parameter is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="79e2f-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="79e2f-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="79e2f-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="79e2f-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="79e2f-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="79e2f-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="79e2f-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="79e2f-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="79e2f-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="79e2f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="79e2f-127">Remarks</span></span>

<span data-ttu-id="79e2f-128">Les listes dont les *adresses* et les *noms* pointent sont de la même longueur.</span><span class="sxs-lookup"><span data-stu-id="79e2f-128">The lists that *Addresses* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e2f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79e2f-129">Requirements</span></span>



| <span data-ttu-id="79e2f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79e2f-130">Requirement</span></span> | <span data-ttu-id="79e2f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="79e2f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79e2f-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="79e2f-132">TAPI version</span></span><br/> | <span data-ttu-id="79e2f-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="79e2f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="79e2f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="79e2f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="79e2f-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="79e2f-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79e2f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="79e2f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="79e2f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="79e2f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="79e2f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e2f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79e2f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e2f-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="79e2f-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




