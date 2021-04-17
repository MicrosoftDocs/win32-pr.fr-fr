---
title: MpUpdateStart, fonction (MpClient. h)
description: Démarre une opération de mise à jour de signature.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpUpdateStart
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466654"
---
# <a name="mpupdatestart-function"></a><span data-ttu-id="cc9ed-104">MpUpdateStart fonction)</span><span class="sxs-lookup"><span data-stu-id="cc9ed-104">MpUpdateStart function</span></span>

<span data-ttu-id="cc9ed-105">Démarre une opération de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-105">Starts a signature update operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc9ed-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc9ed-106">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a><span data-ttu-id="cc9ed-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc9ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc9ed-108">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc9ed-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc9ed-109">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="cc9ed-110">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="cc9ed-111">Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ed-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cc9ed-112">*dwUpdateOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc9ed-112">*dwUpdateOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc9ed-113">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-113">Type: **DWORD**</span></span>

<span data-ttu-id="cc9ed-114">Spécifie l’option pour l’opération de mise à jour des signatures.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-114">Specifies the option for the signature update operation.</span></span> <span data-ttu-id="cc9ed-115">Ce peut être l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc9ed-115">It can be one of the following values:</span></span>



| <span data-ttu-id="cc9ed-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc9ed-116">Value</span></span>                                                                                                                                                                                              | <span data-ttu-id="cc9ed-117">Signification</span><span class="sxs-lookup"><span data-stu-id="cc9ed-117">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <span data-ttu-id="cc9ed-118"><dt>**\_option mise à jour \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-118"><dt>**MPUPDATE\_OPTION\_NONE**</dt></span></span> </dl>                | <span data-ttu-id="cc9ed-119">Aucune option spécifique n’est demandée.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-119">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <span data-ttu-id="cc9ed-120"><dt>**\_option mise à jour \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-120"><dt>**MPUPDATE\_OPTION\_ASYNC**</dt></span></span> </dl>             | <span data-ttu-id="cc9ed-121">L’opération de mise à jour doit être asynchrone, où **MpUpdateStart** retourne immédiatement après l’initialisation réussie de la mise à jour de la signature.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-121">The update operation is to be asynchronous, where **MpUpdateStart** returns immediately after the successful initiation of the signature update.</span></span> <span data-ttu-id="cc9ed-122">(Par défaut, l’opération de mise à jour est synchrone, ce qui signifie que **MpUpdateStart** retournera uniquement une fois la mise à jour de signature terminée.)</span><span class="sxs-lookup"><span data-stu-id="cc9ed-122">(By default the update operation is synchronous, meaning **MpUpdateStart** will return only after the signature update is finished.)</span></span><br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <span data-ttu-id="cc9ed-123"><dt>**progression de l' \_ option mise à jour \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-123"><dt>**MPUPDATE\_OPTION\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="cc9ed-124">L’appelant souhaite recevoir des informations de progression de mise à jour de signature via un rappel.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-124">The caller is interested in receiving signature update progress information via a callback.</span></span><br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <span data-ttu-id="cc9ed-125"><dt>**\_option mise à jour \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-125"><dt>**MPUPDATE\_OPTION\_HTTP**</dt></span></span> </dl>                | <span data-ttu-id="cc9ed-126">La mise à jour de signature est effectuée en téléchargeant le package de signature complète à partir du site portail de sécurité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-126">The signature update is performed by downloading the full signature package from the Microsoft security portal site.</span></span> <span data-ttu-id="cc9ed-127">Cela peut être utilisé comme option de secours si le client rencontre un problème de téléchargement de signature via Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-127">This can be used as a fallback option if the client is experiencing a signature download problem via Microsoft Update.</span></span><br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <span data-ttu-id="cc9ed-128"><dt>**\_option mise à jour \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-128"><dt>**MPUPDATE\_OPTION\_UNC**</dt></span></span> </dl>                   | <span data-ttu-id="cc9ed-129">Effectue une mise à jour de signature à l’aide du téléchargement direct à partir de partages UNC.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-129">Performs signature update using direct download from UNC shares.</span></span><br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <span data-ttu-id="cc9ed-130"><dt>**\_option mise à jour \_ gérée**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-130"><dt>**MPUPDATE\_OPTION\_MANAGED**</dt></span></span> </dl>       | <span data-ttu-id="cc9ed-131">Effectue une mise à jour de signature à l’aide du service managé WSUS.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-131">Performs signature update using the Managed Service WSUS.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <span data-ttu-id="cc9ed-132"><dt>**\_option mise à jour \_ non gérée**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-132"><dt>**MPUPDATE\_OPTION\_UNMANAGED**</dt></span></span> </dl> | <span data-ttu-id="cc9ed-133">Effectue une mise à jour de signature à l’aide du service non managé MU/WU.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-133">Performs signature update using the Unmanaged Service MU/WU.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="cc9ed-134">*pCallbackInfo* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cc9ed-134">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc9ed-135">Type : **PMPCALLBACK \_ info**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-135">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="cc9ed-136">Pointeur vers les informations de rappel utilisées pour alimenter le client avec les modifications de l’état de mise à jour de signature (telles que le début et la fin) et les informations de progression.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-136">A pointer to the callback information used to feed the client with signature update state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="cc9ed-137">Les [**\_ données MPCALLBACK**](mpcallback-data.md) retournées dans la fonction de rappel signalent l’état de mise à jour réel et les informations relatives à la progression.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-137">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual update state and progress-related information.</span></span> <span data-ttu-id="cc9ed-138">La liste suivante répertorie les rappels possibles :</span><span class="sxs-lookup"><span data-stu-id="cc9ed-138">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="cc9ed-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc9ed-139">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="cc9ed-140">Signification</span><span class="sxs-lookup"><span data-stu-id="cc9ed-140">Meaning</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <span data-ttu-id="cc9ed-141"><dt>**MPNOTIFY \_ SIGUPDATE \_ Start**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-141"><dt>**MPNOTIFY\_SIGUPDATE\_START**</dt></span></span> </dl>                                      | <span data-ttu-id="cc9ed-142">L’opération de mise à jour a démarré.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-142">Update operation started.</span></span><br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <span data-ttu-id="cc9ed-143"><dt>**MPNOTIFY \_ SIGUPDATE \_ terminé**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-143"><dt>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</dt></span></span> </dl>                             | <span data-ttu-id="cc9ed-144">Opération de mise à jour terminée.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-144">Update operation completed.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <span data-ttu-id="cc9ed-145"><dt>**début de la \_ recherche MPNOTIFY SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-145"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</dt></span></span> </dl>                | <span data-ttu-id="cc9ed-146">Recherche des mises à jour démarrées.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-146">Search for updates started.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <span data-ttu-id="cc9ed-147"><dt>**recherche de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-147"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</dt></span></span> </dl>       | <span data-ttu-id="cc9ed-148">Recherche des mises à jour terminées.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-148">Search for updates completed.</span></span> <span data-ttu-id="cc9ed-149">Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ed-149">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <span data-ttu-id="cc9ed-150"><dt>**démarrage du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-150"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</dt></span></span> </dl>          | <span data-ttu-id="cc9ed-151">Téléchargement de la mise à jour démarré.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-151">Download for update started.</span></span><br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <span data-ttu-id="cc9ed-152"><dt>**progression du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-152"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</dt></span></span> </dl> | <span data-ttu-id="cc9ed-153">Télécharger les informations de progression.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-153">Download progress information.</span></span> <span data-ttu-id="cc9ed-154">Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ed-154">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <span data-ttu-id="cc9ed-155"><dt>**Téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_ terminé**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-155"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</dt></span></span> </dl> | <span data-ttu-id="cc9ed-156">Téléchargement pour la mise à jour terminée.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-156">Download for update complete.</span></span> <span data-ttu-id="cc9ed-157">Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ed-157">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <span data-ttu-id="cc9ed-158"><dt>**démarrage de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-158"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</dt></span></span> </dl>             | <span data-ttu-id="cc9ed-159">L’installation de la mise à jour a démarré.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-159">Installation of update started.</span></span><br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <span data-ttu-id="cc9ed-160"><dt>**progression de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-160"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="cc9ed-161">Informations de progression de l’installation.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-161">Installation progress information.</span></span> <span data-ttu-id="cc9ed-162">Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ed-162">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <span data-ttu-id="cc9ed-163"><dt>**installation de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-163"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</dt></span></span> </dl>    | <span data-ttu-id="cc9ed-164">Installation de la mise à jour terminée.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-164">Installation of update completed.</span></span> <span data-ttu-id="cc9ed-165">Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ed-165">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <span data-ttu-id="cc9ed-166"><dt>**\_requête MPNOTIFY \_ SIGUPDATE \_ traitée**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-166"><dt>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</dt></span></span> </dl> | <span data-ttu-id="cc9ed-167">Le service anti-programme malveillant a traité une demande de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-167">The antimalware service processed a signature update request.</span></span> <span data-ttu-id="cc9ed-168">L’échec ou la réussite est indiqué par *HRESULT* dans les [**\_ données de MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="cc9ed-168">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <span data-ttu-id="cc9ed-169"><dt>**redémarrage de MPNOTIFY \_ SIGUPDATE \_ \_ requis**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-169"><dt>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</dt></span></span> </dl>       | <span data-ttu-id="cc9ed-170">Nécessite un redémarrage pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-170">Requires reboot to complete the update operation.</span></span> <span data-ttu-id="cc9ed-171">L’échec ou la réussite est indiqué par *HRESULT* dans les [**\_ données de MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="cc9ed-171">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="cc9ed-172"><dt>**\_échec interne \_ MPNOTIFY**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-172"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>                                   | <span data-ttu-id="cc9ed-173">L’opération de mise à jour de signature a rencontré un échec générique.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-173">Signature update operation has encountered a generic failure.</span></span> <span data-ttu-id="cc9ed-174">Le *HRESULT* dans [**les \_ données MPCALLBACK**](mpcallback-data.md) contient le code d’erreur spécifique.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-174">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="cc9ed-175">*phUpdateHandle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc9ed-175">*phUpdateHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc9ed-176">Type : **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-176">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="cc9ed-177">Handle de mise à jour retourné qui identifie l’opération de mise à jour de signature actuellement lancée.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-177">Returned update handle which identifies the currently initiated signature update operation.</span></span> <span data-ttu-id="cc9ed-178">Ce handle peut être utilisé dans les appels de fonction suivants, par exemple, pour contrôler l’opération de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-178">This handle can be used in subsequent function calls, such as to control the signature update operation.</span></span> <span data-ttu-id="cc9ed-179">Le descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ed-179">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc9ed-180">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc9ed-180">Return value</span></span>

<span data-ttu-id="cc9ed-181">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-181">Type: **HRESULT**</span></span>

<span data-ttu-id="cc9ed-182">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-182">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="cc9ed-183">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-183">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="cc9ed-184">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="cc9ed-184">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc9ed-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc9ed-185">Requirements</span></span>



| <span data-ttu-id="cc9ed-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc9ed-186">Requirement</span></span> | <span data-ttu-id="cc9ed-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc9ed-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9ed-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc9ed-188">Minimum supported client</span></span><br/> | <span data-ttu-id="cc9ed-189">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc9ed-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cc9ed-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc9ed-190">Minimum supported server</span></span><br/> | <span data-ttu-id="cc9ed-191">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc9ed-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc9ed-192">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc9ed-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc9ed-193"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-193"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc9ed-194">DLL</span><span class="sxs-lookup"><span data-stu-id="cc9ed-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc9ed-195"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ed-195"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc9ed-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc9ed-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc9ed-197">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-197">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="cc9ed-198">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-198">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="cc9ed-199">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-199">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="cc9ed-200">**\_données MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-200">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="cc9ed-201">**\_données MPSIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="cc9ed-201">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> </dl>

 

 





