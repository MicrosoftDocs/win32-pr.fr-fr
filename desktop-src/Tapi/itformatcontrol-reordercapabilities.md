---
description: La méthode ReOrderCapabilities définit une nouvelle commande pour les fonctionnalités de format.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'ITFormatControl :: ReOrderCapabilities, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526543"
---
# <a name="itformatcontrolreordercapabilities-method"></a><span data-ttu-id="43429-103">ITFormatControl :: ReOrderCapabilities, méthode</span><span class="sxs-lookup"><span data-stu-id="43429-103">ITFormatControl::ReOrderCapabilities method</span></span>

<span data-ttu-id="43429-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="43429-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43429-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="43429-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="43429-106">La méthode **ReOrderCapabilities** définit une nouvelle commande pour les fonctionnalités de format.</span><span class="sxs-lookup"><span data-stu-id="43429-106">The **ReOrderCapabilities** method sets a new order for format capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="43429-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43429-107">Syntax</span></span>


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="43429-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43429-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43429-109">*pdwIndices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43429-109">*pdwIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43429-110">Index du format en cours de réorganisation.</span><span class="sxs-lookup"><span data-stu-id="43429-110">Index of the format being reordered.</span></span>

</dd> <dt>

<span data-ttu-id="43429-111">*pfEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43429-111">*pfEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43429-112">Indique si le format doit être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="43429-112">Indicates whether the format should be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="43429-113">*pfPublicize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43429-113">*pfPublicize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43429-114">Indique si le format doit être rendu disponible.</span><span class="sxs-lookup"><span data-stu-id="43429-114">Indicates whether the format should be made available.</span></span>

</dd> <dt>

<span data-ttu-id="43429-115">*dwNumIndices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43429-115">*dwNumIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43429-116">Nouveau numéro d’index pour le format.</span><span class="sxs-lookup"><span data-stu-id="43429-116">New index number for the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43429-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43429-117">Return value</span></span>

<span data-ttu-id="43429-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="43429-118">This method can return one of these values.</span></span>



| <span data-ttu-id="43429-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="43429-119">Return code</span></span>                                                                                   | <span data-ttu-id="43429-120">Description</span><span class="sxs-lookup"><span data-stu-id="43429-120">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="43429-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43429-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="43429-122">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="43429-122">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="43429-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="43429-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="43429-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="43429-124">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43429-125">Notes</span><span class="sxs-lookup"><span data-stu-id="43429-125">Remarks</span></span>

<span data-ttu-id="43429-126">La méthode [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) doit être appelée avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="43429-126">The [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) method must be called prior to using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43429-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43429-127">Requirements</span></span>



| <span data-ttu-id="43429-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43429-128">Requirement</span></span> | <span data-ttu-id="43429-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="43429-129">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43429-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="43429-130">TAPI version</span></span><br/> | <span data-ttu-id="43429-131">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="43429-131">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="43429-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="43429-132">Header</span></span><br/>       | <dl> <span data-ttu-id="43429-133"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43429-133"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="43429-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43429-134">Library</span></span><br/>      | <dl> <span data-ttu-id="43429-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43429-135"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="43429-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43429-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="43429-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43429-137"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43429-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43429-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43429-139">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="43429-139">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="43429-140">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="43429-140">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




