---
title: MpErrorMessageFormat, fonction (MpClient. h)
description: Retourne un message d’erreur mis en forme en fonction d’un code d’erreur.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpErrorMessageFormat
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942705"
---
# <a name="mperrormessageformat-function"></a><span data-ttu-id="04b06-104">MpErrorMessageFormat fonction)</span><span class="sxs-lookup"><span data-stu-id="04b06-104">MpErrorMessageFormat function</span></span>

<span data-ttu-id="04b06-105">Retourne un message d’erreur mis en forme en fonction d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="04b06-105">Returns a formatted error message based on an error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b06-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04b06-106">Syntax</span></span>


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a><span data-ttu-id="04b06-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04b06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b06-108">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04b06-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b06-109">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="04b06-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="04b06-110">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="04b06-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="04b06-111">Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="04b06-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="04b06-112">*hrError* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04b06-112">*hrError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b06-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04b06-113">Type: **HRESULT**</span></span>

<span data-ttu-id="04b06-114">Code d’erreur basé sur **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="04b06-114">An **HRESULT**-based error code.</span></span>

</dd> <dt>

<span data-ttu-id="04b06-115">*pwszErrorDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04b06-115">*pwszErrorDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04b06-116">Tapez : \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="04b06-116">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="04b06-117">Retourne un message d’erreur mis en forme en fonction de _hrError \*.</span><span class="sxs-lookup"><span data-stu-id="04b06-117">Returns a formatted error message based on _hrError\*.</span></span> <span data-ttu-id="04b06-118">Cette chaîne doit être libérée à l’aide de [**MpFreeMemory**](mpfreememory.md).</span><span class="sxs-lookup"><span data-stu-id="04b06-118">This string must be freed using [**MpFreeMemory**](mpfreememory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b06-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04b06-119">Return value</span></span>

<span data-ttu-id="04b06-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04b06-120">Type: **HRESULT**</span></span>

<span data-ttu-id="04b06-121">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="04b06-121">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="04b06-122">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="04b06-122">If the function fails then the return value is a failed **HRESULT** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b06-123">Notes</span><span class="sxs-lookup"><span data-stu-id="04b06-123">Remarks</span></span>

<span data-ttu-id="04b06-124">Cette fonction est en charge de la mise en forme des codes d’erreur système en plus des codes d’erreur spécifiques retournés par les fonctions de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="04b06-124">This function is capable of formatting system error codes in addition to specific error codes returned by malware protection functions.</span></span> <span data-ttu-id="04b06-125">Les codes d’erreur **HRESULT** spécifiques aux fonctions de protection contre les programmes malveillants ont une fonctionnalité de 0x50.</span><span class="sxs-lookup"><span data-stu-id="04b06-125">The **HRESULT** error codes specific to malware protection functions have a facility of 0x50.</span></span> <span data-ttu-id="04b06-126">Voici une liste d’un sous-ensemble de codes d’erreur spécifiques à la protection contre les programmes malveillants qui peuvent être renvoyés par différentes fonctions de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="04b06-126">Below is a list of a subset of the malware protection-specific error codes that can be returned by various malware protection functions.</span></span> <span data-ttu-id="04b06-127">À l’aide **de la macro HRESULT \_ de l' \_ \_ État MP**, les codes d’erreur suivants peuvent être convertis en **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="04b06-127">Using the macro **HRESULT\_FROM\_MP\_STATUS**, the following error codes can be converted to **HRESULT**.</span></span> <span data-ttu-id="04b06-128">Voir aussi [codes d’erreur du moteur anti-programme malveillant Forefront Client Security](https://support.microsoft.com/kb/939359) pour obtenir la liste des autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="04b06-128">See also [Forefront Client Security anti-malware engine error codes](https://support.microsoft.com/kb/939359) for a list of other possible error codes.</span></span>



| <span data-ttu-id="04b06-129">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="04b06-129">Error Code</span></span>                              | <span data-ttu-id="04b06-130">Description</span><span class="sxs-lookup"><span data-stu-id="04b06-130">Description</span></span>                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b06-131">ERREUR \_ MP \_ noengine</span><span class="sxs-lookup"><span data-stu-id="04b06-131">ERROR\_MP\_NOENGINE</span></span>                     | <span data-ttu-id="04b06-132">Aucun moteur n’est chargé dans le service anti-programme malveillant pour effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="04b06-132">No engine is loaded in antimalware service to perform the requested operation.</span></span>                                              |
| <span data-ttu-id="04b06-133">ERREUR \_ MP- \_ aucune \_ mémoire</span><span class="sxs-lookup"><span data-stu-id="04b06-133">ERROR\_MP\_NO\_MEMORY</span></span>                   | <span data-ttu-id="04b06-134">Le moteur du logiciel anti-programme malveillant a rencontré une situation sans mémoire.</span><span class="sxs-lookup"><span data-stu-id="04b06-134">The antimalware engine has encountered a no memory situation.</span></span>                                                               |
| <span data-ttu-id="04b06-135">ERREUR \_ échec de la suppression du pack d' \_ installation \_</span><span class="sxs-lookup"><span data-stu-id="04b06-135">ERROR\_MP\_REMOVE\_FAILED</span></span>               | <span data-ttu-id="04b06-136">Échec de l’opération de suppression pour une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="04b06-136">Remove operation failed for a specific threat.</span></span>                                                                              |
| <span data-ttu-id="04b06-137">échec de la mise en quarantaine du pack d’erreur \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="04b06-137">ERROR\_MP\_QUARANTINE\_FAILED</span></span>           | <span data-ttu-id="04b06-138">Échec de l’opération de mise en quarantaine pour une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="04b06-138">Quarantine operation failed for a specific threat.</span></span>                                                                          |
| <span data-ttu-id="04b06-139">ERREUR \_ MP \_ Threat \_ \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="04b06-139">ERROR\_MP\_THREAT\_NOT\_FOUND</span></span>           | <span data-ttu-id="04b06-140">La menace spécifique n’existe plus dans le système.</span><span class="sxs-lookup"><span data-stu-id="04b06-140">The specific threat no longer exists in the system.</span></span>                                                                         |
| <span data-ttu-id="04b06-141">ERREUR de \_ suppression du pack d' \_ installation \_ non \_ prise en charge</span><span class="sxs-lookup"><span data-stu-id="04b06-141">ERROR\_MP\_REMOVE\_NOT\_SUPPORTED</span></span>       | <span data-ttu-id="04b06-142">La suppression de l’opération pour une menace spécifique à l’intérieur du type de conteneur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="04b06-142">Remove operation for a specific threat inside the container type is not supported.</span></span>                                          |
| <span data-ttu-id="04b06-143">ERREUR \_ MP de \_ suppression du \_ \_ conteneur immuable</span><span class="sxs-lookup"><span data-stu-id="04b06-143">ERROR\_MP\_REMOVE\_IMMUTABLE\_CONTAINER</span></span> | <span data-ttu-id="04b06-144">En raison de la stratégie du moteur, une opération de suppression d’une menace spécifique à l’intérieur d’un conteneur bloqué n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="04b06-144">Due to engine policy, a remove operation of a specific threat inside a blocked container is not supported.</span></span> <span data-ttu-id="04b06-145">(Archives de messagerie.)</span><span class="sxs-lookup"><span data-stu-id="04b06-145">(Mail archives.)</span></span> |
| <span data-ttu-id="04b06-146">ERREUR \_ MP \_ BADDB \_ OLDENGINE</span><span class="sxs-lookup"><span data-stu-id="04b06-146">ERROR\_MP\_BADDB\_OLDENGINE</span></span>             | <span data-ttu-id="04b06-147">La demande de mise à jour de signature a fourni un moteur ou des fichiers de signature plus anciens.</span><span class="sxs-lookup"><span data-stu-id="04b06-147">Signature update request provided an older engine or signature files(s).</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="04b06-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04b06-148">Requirements</span></span>



| <span data-ttu-id="04b06-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04b06-149">Requirement</span></span> | <span data-ttu-id="04b06-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="04b06-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b06-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04b06-151">Minimum supported client</span></span><br/> | <span data-ttu-id="04b06-152">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04b06-152">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="04b06-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04b06-153">Minimum supported server</span></span><br/> | <span data-ttu-id="04b06-154">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04b06-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04b06-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="04b06-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="04b06-156"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b06-156"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="04b06-157">DLL</span><span class="sxs-lookup"><span data-stu-id="04b06-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b06-158"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b06-158"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b06-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04b06-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b06-160">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="04b06-160">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="04b06-161">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="04b06-161">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="04b06-162">Codes d’erreur du moteur anti-programme malveillant Forefront Client Security</span><span class="sxs-lookup"><span data-stu-id="04b06-162">Forefront Client Security anti-malware engine error codes</span></span>](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





