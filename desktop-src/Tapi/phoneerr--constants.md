---
description: Il s’agit de la liste des codes d’erreur que l’implémentation peut retourner lors de l’appel d’opérations sur des appareils téléphoniques. Consultez les descriptions des fonctions individuelles pour déterminer lequel de ces codes d’erreur chaque fonction peut retourner.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Constantes PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541788"
---
# <a name="phoneerr_-constants"></a><span data-ttu-id="5a13a-104">\_Constantes PHONEERR</span><span class="sxs-lookup"><span data-stu-id="5a13a-104">PHONEERR\_ Constants</span></span>

<span data-ttu-id="5a13a-105">Il s’agit de la liste des codes d’erreur que l’implémentation peut retourner lors de l’appel d’opérations sur des appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="5a13a-105">This is the list of error codes that the implementation can return when invoking operations on phone devices.</span></span> <span data-ttu-id="5a13a-106">Consultez les descriptions des fonctions individuelles pour déterminer lequel de ces codes d’erreur chaque fonction peut retourner.</span><span class="sxs-lookup"><span data-stu-id="5a13a-106">Consult the individual function descriptions to determine which of these error codes each function can return.</span></span>

<dl> <dt>

<span data-ttu-id="5a13a-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ allouée**</span><span class="sxs-lookup"><span data-stu-id="5a13a-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-108">La ressource spécifiée est déjà allouée.</span><span class="sxs-lookup"><span data-stu-id="5a13a-108">The specified resource is already allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR \_ BADDEVICEID**</span><span class="sxs-lookup"><span data-stu-id="5a13a-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-110">L’identificateur d’appareil spécifié n’est pas valide ou est hors limites.</span><span class="sxs-lookup"><span data-stu-id="5a13a-110">The specified device identifier is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ déconnecté**</span><span class="sxs-lookup"><span data-stu-id="5a13a-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-112">L’appel a été déconnecté.</span><span class="sxs-lookup"><span data-stu-id="5a13a-112">The call was disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR \_ INCOMPATIBLEAPIVERSION**</span><span class="sxs-lookup"><span data-stu-id="5a13a-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-114">L’application a demandé une version ou une plage de versions d’API qui ne peut pas être prise en charge par l’implémentation de l’API de téléphonie ou le fournisseur de services correspondant.</span><span class="sxs-lookup"><span data-stu-id="5a13a-114">The application requested an API version or version range that cannot be supported by the Telephony API implementation or the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR \_ INCOMPATIBLEEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="5a13a-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-116">L’application a demandé une version d’extension ou une plage de versions qui ne peut pas être prise en charge par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="5a13a-116">The application requested an extension version or version range that cannot be supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR \_ INIFILECORRUPT**</span><span class="sxs-lookup"><span data-stu-id="5a13a-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-118">En raison d’incohérences internes ou de problèmes de mise en forme dans le fichier Telephon.ini, il est impossible de les lire et de les comprendre correctement par l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="5a13a-118">Because of internal inconsistencies or formatting problems in the Telephon.ini file, it cannot be read and understood properly by TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR \_ Inuse**</span><span class="sxs-lookup"><span data-stu-id="5a13a-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-120">L’appareil est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5a13a-120">The device is currently in use.</span></span> <span data-ttu-id="5a13a-121">L’appareil ne peut pas être configuré.</span><span class="sxs-lookup"><span data-stu-id="5a13a-121">The device cannot be configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR \_ INVALAPPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-123">Le handle d’utilisation ou le descripteur d’enregistrement spécifié de l’application n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-123">The application's specified usage handle or registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR \_ INVALAPPNAME**</span><span class="sxs-lookup"><span data-stu-id="5a13a-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-125">Le nom d’application spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-125">The specified application name is invalid.</span></span> <span data-ttu-id="5a13a-126">Si un nom d’application est spécifié par l’application, il est supposé que la chaîne ne contient pas de caractères non affichables et qu’elle se termine par un caractère **null**.</span><span class="sxs-lookup"><span data-stu-id="5a13a-126">If an application name is specified by the application, it is assumed that the string does not contain any nondisplayable characters and is **NULL**-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR \_ INVALBUTTONLAMPID**</span><span class="sxs-lookup"><span data-stu-id="5a13a-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR\_INVALBUTTONLAMPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-128">L’identificateur de bouton/lampe spécifié est hors limites ou n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-128">The specified button/lamp identifier is out of range or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR \_ INVALBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR\_INVALBUTTONMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-130">Le paramètre de mode du bouton n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-130">The button mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR \_ INVALBUTTONSTATE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR\_INVALBUTTONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-132">Le paramètre États du bouton n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-132">The button states parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR \_ INVALDATAID**</span><span class="sxs-lookup"><span data-stu-id="5a13a-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR\_INVALDATAID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-134">L’identificateur de données spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-134">The specified data identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR \_ INVALDEVICECLASS**</span><span class="sxs-lookup"><span data-stu-id="5a13a-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-136">Le téléphone spécifié ne prend pas en charge la classe d’appareil indiquée.</span><span class="sxs-lookup"><span data-stu-id="5a13a-136">The specified phone does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR \_ INVALEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="5a13a-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-138">Le numéro de version de l’extension du fournisseur de services n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-138">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR \_ INVALHOOKSWITCHDEV**</span><span class="sxs-lookup"><span data-stu-id="5a13a-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR\_INVALHOOKSWITCHDEV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-140">Le paramètre d’appareil hookswitch n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-140">The hookswitch device parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR \_ INVALHOOKSWITCHMODE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR\_INVALHOOKSWITCHMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-142">Le paramètre de mode hookswitch n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-142">The hookswitch mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR \_ INVALLAMPMODE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR\_INVALLAMPMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-144">Le paramètre de mode de lampe spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-144">The specified lamp mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR \_ INVALPARAM**</span><span class="sxs-lookup"><span data-stu-id="5a13a-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-146">Un paramètre, tel qu’une valeur de ligne ou de colonne ou un handle de fenêtre, n’est pas valide ou est hors limites.</span><span class="sxs-lookup"><span data-stu-id="5a13a-146">A parameter, such as a row or column value or a window handle, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR \_ INVALPHONEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR\_INVALPHONEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-148">Le handle d’appareil spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-148">The specified device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR \_ INVALPHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR\_INVALPHONESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-150">L’appareil téléphonique n’est pas dans un état valide pour l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="5a13a-150">The phone device is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR \_ INVALPOINTER**</span><span class="sxs-lookup"><span data-stu-id="5a13a-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-152">Un ou plusieurs des paramètres de pointeur spécifiés ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5a13a-152">One or more of the specified pointer parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR \_ INVALPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR\_INVALPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-154">Le paramètre *dwPrivilege* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-154">The *dwPrivilege* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR \_ INVALRINGMODE**</span><span class="sxs-lookup"><span data-stu-id="5a13a-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR\_INVALRINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-156">Le paramètre de mode Ring n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5a13a-156">The ring mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ NOdevice**</span><span class="sxs-lookup"><span data-stu-id="5a13a-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-158">L’identificateur de périphérique spécifié, qui était précédemment valide, n’est plus accepté, car l’appareil associé a été supprimé du système depuis que l’interface TAPI a été initialisée pour la dernière fois, ou endommagée d’une façon qui n’a pas été détectée lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="5a13a-158">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized or is corrupt in a way that was not detected at initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NOdriver**</span><span class="sxs-lookup"><span data-stu-id="5a13a-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-160">Le fournisseur de services téléphoniques de l’appareil spécifié a détecté que l’un de ses composants est manquant ou endommagé d’une manière qui n’a pas été détectée au moment de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="5a13a-160">The telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="5a13a-161">L’utilisateur doit être invité à utiliser le panneau de configuration de la téléphonie pour corriger le problème.</span><span class="sxs-lookup"><span data-stu-id="5a13a-161">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="5a13a-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-163">Mémoire insuffisante pour terminer l’opération demandée, ou impossible d’allouer ou de verrouiller la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5a13a-163">Insufficient memory to complete the requested operation, or unable to allocate or lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR \_**</span><span class="sxs-lookup"><span data-stu-id="5a13a-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-165">L’application ne dispose pas de privilèges de propriétaire sur le périphérique téléphonique spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a13a-165">The application does not have owner privilege to the specified phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR \_ OPERATIONFAILED**</span><span class="sxs-lookup"><span data-stu-id="5a13a-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-167">L’opération a échoué pour une raison non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5a13a-167">The operation failed for an unspecified reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR \_ OPERATIONUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="5a13a-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-169">L’opération n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5a13a-169">The operation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**Réinit PHONEERR \_**</span><span class="sxs-lookup"><span data-stu-id="5a13a-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-171">Si la réinitialisation TAPI a été demandée, par exemple suite à l’ajout ou à la suppression d’un fournisseur de services de téléphonie, les demandes [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) ou [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) sont rejetées avec cette erreur jusqu’à ce que la dernière application arrête son utilisation de l’API (à l’aide de [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), et que les applications soient de nouveau autorisées à appeler **phoneInitialize** ou **phoneInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="5a13a-171">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) or [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **phoneInitialize** or **phoneInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR \_ REQUESTOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="5a13a-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-173">Le nombre maximal de demandes de téléphone en suspens a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="5a13a-173">The maximum number of outstanding phone requests has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR \_ RESOURCEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="5a13a-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-175">L’opération ne peut pas être effectuée en raison d’un surengagement de ressources.</span><span class="sxs-lookup"><span data-stu-id="5a13a-175">The operation cannot be completed because of resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR \_ STRUCTURETOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="5a13a-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-177">La structure des majuscules de téléphone spécifiée est trop petite.</span><span class="sxs-lookup"><span data-stu-id="5a13a-177">The specified phone caps structure is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a13a-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR \_ non initialisé**</span><span class="sxs-lookup"><span data-stu-id="5a13a-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a13a-179">L’opération a été appelée avant toute application appelée [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="5a13a-179">The operation was invoked before any application called [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a13a-180">Notes</span><span class="sxs-lookup"><span data-stu-id="5a13a-180">Remarks</span></span>

<span data-ttu-id="5a13a-181">Les valeurs 0xC0000000 à 0xFFFFFFFF sont disponibles pour les extensions spécifiques à l’appareil ; les valeurs 0x80000000 à 0xBFFFFFFF sont réservées ; et 0x00000000 à 0x7FFFFFFF sont utilisés en tant qu’identificateurs de demande.</span><span class="sxs-lookup"><span data-stu-id="5a13a-181">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions; the values 0x80000000 through 0xBFFFFFFF are reserved; and 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="5a13a-182">Si une application obtient une erreur indiquant qu’elle n’est pas spécifiquement gérée (par exemple, une erreur définie par une extension spécifique à l’appareil), elle doit traiter l’erreur comme un \_ OPERATIONFAILED PHONEERR (pour une raison non spécifiée).</span><span class="sxs-lookup"><span data-stu-id="5a13a-182">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a PHONEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a13a-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a13a-183">Requirements</span></span>



| <span data-ttu-id="5a13a-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a13a-184">Requirement</span></span> | <span data-ttu-id="5a13a-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a13a-185">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5a13a-186">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5a13a-186">TAPI version</span></span><br/> | <span data-ttu-id="5a13a-187">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5a13a-187">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5a13a-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a13a-188">Header</span></span><br/>       | <dl> <span data-ttu-id="5a13a-189"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a13a-189"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a13a-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a13a-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a13a-191">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="5a13a-191">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="5a13a-192">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="5a13a-192">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="5a13a-193">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="5a13a-193">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="5a13a-194">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="5a13a-194">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




