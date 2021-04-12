---
description: La méthode Configure envoie les informations de configuration de capture.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'IStats :: configure, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210047"
---
# <a name="istatsconfigure-method"></a><span data-ttu-id="28a49-103">IStats :: configure, méthode</span><span class="sxs-lookup"><span data-stu-id="28a49-103">IStats::Configure method</span></span>

<span data-ttu-id="28a49-104">La méthode **configure** envoie les informations de configuration de capture.</span><span class="sxs-lookup"><span data-stu-id="28a49-104">The **Configure** method submits capture configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a49-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28a49-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="28a49-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28a49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a49-107">*hConfigurationBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28a49-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-108">Handle de l’objet BLOB configuré par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="28a49-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="28a49-109">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28a49-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-110">Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="28a49-110">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28a49-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28a49-111">Return value</span></span>

<span data-ttu-id="28a49-112">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="28a49-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="28a49-113">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="28a49-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="28a49-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="28a49-114">Return code</span></span>                                                                                                         | <span data-ttu-id="28a49-115">Description</span><span class="sxs-lookup"><span data-stu-id="28a49-115">Description</span></span>                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28a49-116"><dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-116"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="28a49-117">La chaîne ne se termine pas par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="28a49-117">The string is not null-terminated.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="28a49-118"><dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-118"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="28a49-119">La méthode **CreateBlob** n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="28a49-119">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="28a49-120"><dt>**NMERR \_ \_ objet blob non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-120"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="28a49-121">L’objet pointé n’est pas un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="28a49-121">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="28a49-122"><dt>**NMERR \_ objet blob de niveau supérieur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-122"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="28a49-123">Le numéro de version de l’objet BLOB est incorrect.</span><span class="sxs-lookup"><span data-stu-id="28a49-123">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="28a49-124"><dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ \_ existe déjà**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-124"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="28a49-125">Une entrée d’objet BLOB existe déjà.</span><span class="sxs-lookup"><span data-stu-id="28a49-125">A BLOB entry already exists.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="28a49-126"><dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-126"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="28a49-127">L’objet BLOB de configuration spécifié par le paramètre *hConfigurationBlob* n’a pas d’entrée nécessaire pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="28a49-127">The configuration BLOB specified by the *hConfigurationBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="28a49-128">Examinez l’objet BLOB d’erreur retourné par le paramètre *hErrorBlob* pour déterminer quelle entrée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="28a49-128">Look at the error BLOB returned by the *hErrorBlob* parameter to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="28a49-129"><dt>**NMERR \_ , \_ spécificateur ambigu**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-129"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="28a49-130">L’objet BLOB n’a pas d’informations de propriétaire ou de catégorie.</span><span class="sxs-lookup"><span data-stu-id="28a49-130">The BLOB lacks owner or category information.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="28a49-131"><dt>**propriétaire de l' \_ objet BLOB NMERR \_ \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-131"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="28a49-132">La section propriétaire de l’objet BLOB est introuvable.</span><span class="sxs-lookup"><span data-stu-id="28a49-132">The Owner section of the BLOB was not found.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="28a49-133"><dt>**\_catégorie d’objet BLOB NMERR \_ \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-133"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="28a49-134">La section de catégorie de l’objet BLOB est introuvable.</span><span class="sxs-lookup"><span data-stu-id="28a49-134">The Category section of the BLOB was not found.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="28a49-135"><dt>**NMERR \_ \_ catégorie inconnue**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-135"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="28a49-136">Les informations de catégorie ont été trouvées, mais elles ne sont pas comprises.</span><span class="sxs-lookup"><span data-stu-id="28a49-136">Category information was found but not understood.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="28a49-137"><dt>**NMERR \_ \_ balise inconnue**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-137"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="28a49-138">Les informations de balise ont été trouvées mais ne sont pas comprises.</span><span class="sxs-lookup"><span data-stu-id="28a49-138">Tag information was found but not understood.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="28a49-139"><dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-139"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="28a49-140">L’objet BLOB est endommagé.</span><span class="sxs-lookup"><span data-stu-id="28a49-140">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="28a49-141"><dt>**\_déclencheur NMERR non conforme \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-141"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="28a49-142">La partie du déclencheur de l’objet BLOB est endommagée.</span><span class="sxs-lookup"><span data-stu-id="28a49-142">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="28a49-143">Notes</span><span class="sxs-lookup"><span data-stu-id="28a49-143">Remarks</span></span>

<span data-ttu-id="28a49-144">Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré, arrêté mais non déconnecté.</span><span class="sxs-lookup"><span data-stu-id="28a49-144">You must apply this method to restart an NPP that has been started, stopped but not disconnected.</span></span>

<span data-ttu-id="28a49-145">L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans le paramètre *hConfigurationBlob* .</span><span class="sxs-lookup"><span data-stu-id="28a49-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in the *hConfigurationBlob* parameter.</span></span> <span data-ttu-id="28a49-146">L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="28a49-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="28a49-147">Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="28a49-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="28a49-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28a49-148">Requirements</span></span>



| <span data-ttu-id="28a49-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28a49-149">Requirement</span></span> | <span data-ttu-id="28a49-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="28a49-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a49-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28a49-151">Minimum supported client</span></span><br/> | <span data-ttu-id="28a49-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28a49-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="28a49-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28a49-153">Minimum supported server</span></span><br/> | <span data-ttu-id="28a49-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28a49-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="28a49-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="28a49-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="28a49-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="28a49-157">DLL</span><span class="sxs-lookup"><span data-stu-id="28a49-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28a49-158"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a49-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28a49-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a49-160">IStats</span><span class="sxs-lookup"><span data-stu-id="28a49-160">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="28a49-161">ISTATS :: Connect</span><span class="sxs-lookup"><span data-stu-id="28a49-161">ISTATS::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="28a49-162">OBJETS BLOB Moniteur réseau</span><span class="sxs-lookup"><span data-stu-id="28a49-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




