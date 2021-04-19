---
description: La méthode Configure envoie les informations de configuration d’une capture.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP :: configure, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515407"
---
# <a name="iespconfigure-method"></a><span data-ttu-id="4512e-103">IESP :: configure, méthode</span><span class="sxs-lookup"><span data-stu-id="4512e-103">IESP::Configure method</span></span>

<span data-ttu-id="4512e-104">La méthode **configure** envoie les informations de configuration d’une capture.</span><span class="sxs-lookup"><span data-stu-id="4512e-104">The **Configure** method submits configuration information for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4512e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4512e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="4512e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4512e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4512e-107">*hConfigurationBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4512e-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4512e-108">Handle de l’objet BLOB configuré par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="4512e-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="4512e-109">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4512e-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4512e-110">Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4512e-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="4512e-111">Pour plus d’informations sur le contenu d’un objet BLOB d’erreur, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4512e-111">For information about the contents of an error BLOB, see the Remarks section in this topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4512e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4512e-112">Return value</span></span>

<span data-ttu-id="4512e-113">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4512e-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4512e-114">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="4512e-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4512e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4512e-115">Return code</span></span>                                                                                                         | <span data-ttu-id="4512e-116">Description</span><span class="sxs-lookup"><span data-stu-id="4512e-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4512e-117"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-117"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>                | <span data-ttu-id="4512e-118">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="4512e-118">The NPP is not connected to the network.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="4512e-119"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>                      | <span data-ttu-id="4512e-120">Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="4512e-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="4512e-121"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-121"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                     | <span data-ttu-id="4512e-122">Le NPP signale que la session de capture a démarré.</span><span class="sxs-lookup"><span data-stu-id="4512e-122">The NPP reports that the capture session has started.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="4512e-123"><dt>**\_déclencheur NMERR non conforme \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-123"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="4512e-124">La partie déclencheur de l’objet BLOB de configuration est endommagée.</span><span class="sxs-lookup"><span data-stu-id="4512e-124">The trigger portion of the configuration BLOB is corrupt.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="4512e-125"><dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-125"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="4512e-126">Une entrée nécessaire à l’exécution de cette opération est manquante dans l’objet BLOB de configuration spécifié par *hConfigurationBlob* .</span><span class="sxs-lookup"><span data-stu-id="4512e-126">The configuration BLOB specified by *hConfigurationBlob* is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="4512e-127">Examinez l’objet BLOB d’erreur retourné par *hErrorBlob* pour déterminer quelle entrée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="4512e-127">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="4512e-128"><dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-128"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="4512e-129">L’objet BLOB est endommagé.</span><span class="sxs-lookup"><span data-stu-id="4512e-129">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="4512e-130"><dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-130"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="4512e-131">La méthode **CreateBlob** n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="4512e-131">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="4512e-132"><dt>**NMERR \_ \_ objet blob non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-132"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="4512e-133">L’objet pointé n’est pas un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="4512e-133">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="4512e-134"><dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-134"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="4512e-135">La chaîne ne se termine pas par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="4512e-135">The string is not null-terminated.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="4512e-136"><dt>**NMERR \_ objet blob de niveau supérieur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-136"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="4512e-137">Le numéro de version de l’objet BLOB est incorrect.</span><span class="sxs-lookup"><span data-stu-id="4512e-137">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="4512e-138"><dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-138"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="4512e-139">Aucune mémoire n’était disponible.</span><span class="sxs-lookup"><span data-stu-id="4512e-139">No memory was available.</span></span> <span data-ttu-id="4512e-140">Arrêtez Windows pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="4512e-140">Shut down windows to free up resources.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="4512e-141"><dt>**\_délai d’expiration de NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-141"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="4512e-142">Le délai d'attente de la requête a expiré.</span><span class="sxs-lookup"><span data-stu-id="4512e-142">The request has timed out.</span></span><br/>                                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="4512e-143">Notes</span><span class="sxs-lookup"><span data-stu-id="4512e-143">Remarks</span></span>

<span data-ttu-id="4512e-144">Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré et arrêté, mais qui n’est pas déconnecté.</span><span class="sxs-lookup"><span data-stu-id="4512e-144">You must apply this method to restart an NPP that has been started and stopped, but not disconnected.</span></span>

<span data-ttu-id="4512e-145">L’objet BLOB d’erreur retourné par le paramètre *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="4512e-145">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="4512e-146">L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="4512e-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="4512e-147">Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="4512e-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="4512e-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4512e-148">Requirements</span></span>



| <span data-ttu-id="4512e-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4512e-149">Requirement</span></span> | <span data-ttu-id="4512e-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="4512e-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4512e-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4512e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="4512e-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4512e-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4512e-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4512e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="4512e-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4512e-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4512e-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="4512e-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="4512e-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4512e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4512e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4512e-158"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4512e-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

 




