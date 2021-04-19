---
description: Configure la préférence des fonctionnalités par défaut.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx :: SetDefaultCapabilityPreferrence, méthode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530949"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a><span data-ttu-id="4d682-103">IH323LineEx :: SetDefaultCapabilityPreferrence, méthode</span><span class="sxs-lookup"><span data-stu-id="4d682-103">IH323LineEx::SetDefaultCapabilityPreferrence method</span></span>

<span data-ttu-id="4d682-104">\[**SetDefaultCapabilityPreferrence** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4d682-104">\[**SetDefaultCapabilityPreferrence** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4d682-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="4d682-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4d682-106">La méthode **SetDefaultCapabilityPreferrence** configure la préférence des fonctionnalités par défaut.</span><span class="sxs-lookup"><span data-stu-id="4d682-106">The **SetDefaultCapabilityPreferrence** method configures the preference of the default capabilities.</span></span> <span data-ttu-id="4d682-107">Les capacités ont un poids par défaut de 100.</span><span class="sxs-lookup"><span data-stu-id="4d682-107">Capabilities have a default weight of 100.</span></span> <span data-ttu-id="4d682-108">Si l’application spécifie une pondération plus élevée pour une capacité, elle aura une priorité plus élevée au cours de la négociation H. 245.</span><span class="sxs-lookup"><span data-stu-id="4d682-108">If the application specifies a higher weight for a capability, it will have a higher priority during the H.245 negotiation.</span></span> <span data-ttu-id="4d682-109">Si l’application définit le poids d’une capacité sur 0, elle n’est pas utilisée dans la négociation H. 245.</span><span class="sxs-lookup"><span data-stu-id="4d682-109">If the application sets the weight of a capability to 0, it will not be used in the H.245 negotiation.</span></span>

<span data-ttu-id="4d682-110">Cette méthode est cumulative.</span><span class="sxs-lookup"><span data-stu-id="4d682-110">This method is cumulative.</span></span> <span data-ttu-id="4d682-111">Par exemple, si cette méthode est appelée en premier pour désactiver une fonctionnalité et est à nouveau appelée pour en désactiver une autre, les deux fonctionnalités seront désactivées à la suite de ces deux appels.</span><span class="sxs-lookup"><span data-stu-id="4d682-111">For example, if this method is called first to disable a capability and is called again to disable another, both capabilities will be disabled as the result of these two calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d682-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d682-112">Syntax</span></span>


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="4d682-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d682-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d682-114">*dwNumCaps* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4d682-114">*dwNumCaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d682-115">Valeur **DWORD** qui contient le nombre de fonctionnalités définies avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4d682-115">A **DWORD** value that contains the number of capabilities set with this method.</span></span>

</dd> <dt>

<span data-ttu-id="4d682-116">*pCapabilities* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4d682-116">*pCapabilities* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d682-117">Tableau de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4d682-117">An array of capabilities.</span></span> <span data-ttu-id="4d682-118">Chaque élément du tableau est une valeur [**de \_ capacité h245**](h245-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="4d682-118">Each element of the array is an [**H245\_CAPABILITY**](h245-capability.md) value.</span></span>

</dd> <dt>

<span data-ttu-id="4d682-119">*pWeights* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4d682-119">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d682-120">Tableau de poids associé aux fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4d682-120">An array of weights associated with the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d682-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d682-121">Return value</span></span>

<span data-ttu-id="4d682-122">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4d682-122">This method can return one of these values.</span></span>



| <span data-ttu-id="4d682-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4d682-123">Return code</span></span>                                                                                   | <span data-ttu-id="4d682-124">Description</span><span class="sxs-lookup"><span data-stu-id="4d682-124">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d682-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4d682-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4d682-126">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4d682-126">Method succeeded.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="4d682-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="4d682-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4d682-128">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="4d682-128">Insufficient memory exists to perform the operation.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="4d682-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4d682-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4d682-130">Le paramètre *pCapabilities* a la **valeur null**, ou le paramètre *pWeights* a la valeur **null**, ou *pCapabilities* et *pWeights* ont la **valeur null**, ou le tableau pCapabilities contient un objet de fonctionnalité H. 245 non valide.</span><span class="sxs-lookup"><span data-stu-id="4d682-130">The *pCapabilities* parameter is **NULL**, or the *pWeights* parameter is **NULL**, or both *pCapabilities* and *pWeights* are **NULL**, or the pCapabilities array contains an invalid H.245 capability object.</span></span><br/> |
| <dl> <span data-ttu-id="4d682-131"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="4d682-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4d682-132">Impossible de lire un élément du tableau *pWeights* ou un élément du tableau *pCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="4d682-132">Unable to read an element of the *pWeights* array or an element of the *pCapabilities* array.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="4d682-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d682-133">Requirements</span></span>



| <span data-ttu-id="4d682-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d682-134">Requirement</span></span> | <span data-ttu-id="4d682-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d682-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d682-136">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="4d682-136">TAPI version</span></span><br/> | <span data-ttu-id="4d682-137">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4d682-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4d682-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d682-138">Header</span></span><br/>       | <dl> <span data-ttu-id="4d682-139"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d682-139"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="4d682-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d682-140">Library</span></span><br/>      | <dl> <span data-ttu-id="4d682-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d682-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4d682-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4d682-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="4d682-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d682-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




