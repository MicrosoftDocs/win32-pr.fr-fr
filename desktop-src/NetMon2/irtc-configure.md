---
description: Envoie des données de configuration pour une capture de données.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'IRTC :: configure, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543656"
---
# <a name="irtcconfigure-method"></a><span data-ttu-id="7b36e-103">IRTC :: configure, méthode</span><span class="sxs-lookup"><span data-stu-id="7b36e-103">IRTC::Configure method</span></span>

<span data-ttu-id="7b36e-104">La méthode [**configure**](configure.md) envoie les données de configuration d’une capture de données.</span><span class="sxs-lookup"><span data-stu-id="7b36e-104">The [**Configure**](configure.md) method submits configuration data for a data capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b36e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b36e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="7b36e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b36e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b36e-107">*hConfigurationBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b36e-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b36e-108">Handle vers l’objet BLOB configuré par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7b36e-108">A handle to the BLOB that is configured by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="7b36e-109">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7b36e-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b36e-110">Handle d’un objet BLOB d’erreur qui contient des données d’erreur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7b36e-110">A handle to an error BLOB that contains additional error data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b36e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b36e-111">Return value</span></span>

<span data-ttu-id="7b36e-112">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7b36e-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7b36e-113">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="7b36e-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7b36e-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7b36e-114">Return code</span></span>                                                                                                         | <span data-ttu-id="7b36e-115">Description</span><span class="sxs-lookup"><span data-stu-id="7b36e-115">Description</span></span>                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b36e-116"><dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-116"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="7b36e-117">La méthode **CreateBlob** n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="7b36e-117">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                 |
| <dl> <span data-ttu-id="7b36e-118"><dt>**NMERR \_ \_ objet blob non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-118"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="7b36e-119">L’objet pointé n’est pas un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="7b36e-119">The object pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="7b36e-120"><dt>**NMERR \_ objet blob de niveau supérieur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-120"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="7b36e-121">Le numéro de version de l’objet BLOB est incorrect.</span><span class="sxs-lookup"><span data-stu-id="7b36e-121">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="7b36e-122"><dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ \_ existe déjà**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-122"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="7b36e-123">Objet BLOB dupliqué.</span><span class="sxs-lookup"><span data-stu-id="7b36e-123">Duplicate BLOB.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="7b36e-124"><dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-124"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="7b36e-125">L’objet BLOB de configuration spécifié par *hConfigurationBlob* n’a pas d’entrée nécessaire pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="7b36e-125">The configuration BLOB specified by *hConfigurationBlob* lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="7b36e-126">Affichez l’objet BLOB d’erreur retourné par *hErrorBlob* pour déterminer l’entrée qui est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7b36e-126">View the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="7b36e-127"><dt>**NMERR \_ , \_ spécificateur ambigu**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-127"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="7b36e-128">Le propriétaire de l’objet BLOB ou les données de catégorie sont manquantes.</span><span class="sxs-lookup"><span data-stu-id="7b36e-128">The BLOB Owner or Category data is missing.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="7b36e-129"><dt>**propriétaire de l' \_ objet BLOB NMERR \_ \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-129"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="7b36e-130">La section propriétaire de l’objet BLOB est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7b36e-130">The BLOB Owner section was not found.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="7b36e-131"><dt>**\_catégorie d’objet BLOB NMERR \_ \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-131"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="7b36e-132">La section de catégorie d’objets BLOB est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7b36e-132">The BLOB Category section was not found.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="7b36e-133"><dt>**NMERR \_ \_ catégorie inconnue**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-133"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="7b36e-134">La section de catégorie BLOB a été trouvée, mais n’est pas comprise.</span><span class="sxs-lookup"><span data-stu-id="7b36e-134">The BLOB Category section was found, but not understood.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="7b36e-135"><dt>**NMERR \_ \_ balise inconnue**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-135"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="7b36e-136">La section de la balise BLOB a été trouvée, mais n’est pas comprise.</span><span class="sxs-lookup"><span data-stu-id="7b36e-136">The BLOB Tag section was found, but not understood.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="7b36e-137"><dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-137"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="7b36e-138">L’objet BLOB est endommagé.</span><span class="sxs-lookup"><span data-stu-id="7b36e-138">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="7b36e-139"><dt>**\_déclencheur NMERR non conforme \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-139"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="7b36e-140">La partie du déclencheur de l’objet BLOB est endommagée.</span><span class="sxs-lookup"><span data-stu-id="7b36e-140">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="7b36e-141"><dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-141"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="7b36e-142">La chaîne ne se termine pas par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="7b36e-142">The string is not null-terminated.</span></span><br/>                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="7b36e-143">Notes</span><span class="sxs-lookup"><span data-stu-id="7b36e-143">Remarks</span></span>

<span data-ttu-id="7b36e-144">Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré, arrêté, mais pas déconnecté.</span><span class="sxs-lookup"><span data-stu-id="7b36e-144">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="7b36e-145">L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="7b36e-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="7b36e-146">L’objet BLOB d’erreurs renvoyé contient des données d’erreur que l’application peut utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="7b36e-146">The returned error BLOB contains error data that the application can use for troubleshooting.</span></span> <span data-ttu-id="7b36e-147">Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="7b36e-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor cannot find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b36e-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b36e-148">Requirements</span></span>



| <span data-ttu-id="7b36e-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b36e-149">Requirement</span></span> | <span data-ttu-id="7b36e-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b36e-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b36e-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b36e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7b36e-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b36e-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7b36e-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b36e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7b36e-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b36e-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7b36e-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b36e-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b36e-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7b36e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7b36e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b36e-158"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b36e-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b36e-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b36e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b36e-160">IRTC</span><span class="sxs-lookup"><span data-stu-id="7b36e-160">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="7b36e-161">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="7b36e-161">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="7b36e-162">OBJETS BLOB Moniteur réseau</span><span class="sxs-lookup"><span data-stu-id="7b36e-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




