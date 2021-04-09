---
title: Méthode IMsTscAxEvents OnLogonError
description: Appelée lorsqu’une erreur d’ouverture de session ou un autre événement d’ouverture de session se produit.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnLogonError
- Méthode OnLogonError Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnLogonError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742117"
---
# <a name="imstscaxeventsonlogonerror-method"></a><span data-ttu-id="662c1-106">IMsTscAxEvents :: OnLogonError, méthode</span><span class="sxs-lookup"><span data-stu-id="662c1-106">IMsTscAxEvents::OnLogonError method</span></span>

<span data-ttu-id="662c1-107">Appelée lorsqu’une erreur d’ouverture de session ou un autre événement d’ouverture de session se produit.</span><span class="sxs-lookup"><span data-stu-id="662c1-107">Called when a logon error or other logon event occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="662c1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="662c1-108">Syntax</span></span>


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a><span data-ttu-id="662c1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="662c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="662c1-110">*lError* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="662c1-110">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="662c1-111">Code d’erreur d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="662c1-111">The logon error code.</span></span> <span data-ttu-id="662c1-112">Cette liste de codes n’est pas exhaustive.</span><span class="sxs-lookup"><span data-stu-id="662c1-112">This list of codes is not exhaustive.</span></span>

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span data-ttu-id="662c1-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Arbitrage \_ \_ \_ Options de BOSSELAGE du code** (-5 (0xFFFFFFFB))</span><span class="sxs-lookup"><span data-stu-id="662c1-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRATION\_CODE\_BUMP\_OPTIONS** (-5 (0xFFFFFFFB))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-114">Winlogon affiche la boîte de dialogue **conflit de session** .</span><span class="sxs-lookup"><span data-stu-id="662c1-114">Winlogon is displaying the **Session Contention** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span data-ttu-id="662c1-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Arbitrage \_ L' \_ \_ ouverture de session du code continue** (-2 (0xfffffffe))</span><span class="sxs-lookup"><span data-stu-id="662c1-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRATION\_CODE\_CONTINUE\_LOGON** (-2 (0xFFFFFFFE))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-116">Winlogon continue avec le processus d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="662c1-116">Winlogon is continuing with the logon process.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span data-ttu-id="662c1-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Arbitrage \_ \_ \_ Fin** de la poursuite du code (-3 (0xFFFFFFFD))</span><span class="sxs-lookup"><span data-stu-id="662c1-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRATION\_CODE\_CONTINUE\_TERMINATE** (-3 (0xFFFFFFFD))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-118">Winlogon se termine en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="662c1-118">Winlogon is ending silently.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span data-ttu-id="662c1-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Arbitrage \_ \_ \_ Boîte de dialogue code noperm** (-6 (0xFFFFFFFA))</span><span class="sxs-lookup"><span data-stu-id="662c1-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRATION\_CODE\_NOPERM\_DIALOG** (-6 (0xFFFFFFFA))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-120">Winlogon affiche la boîte de dialogue **aucune autorisation** .</span><span class="sxs-lookup"><span data-stu-id="662c1-120">Winlogon is displaying the **No Permissions** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span data-ttu-id="662c1-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Arbitrage \_ \_Boîte de \_ dialogue code refusé** (-7 (0xFFFFFFF9))</span><span class="sxs-lookup"><span data-stu-id="662c1-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRATION\_CODE\_REFUSED\_DIALOG** (-7 (0xFFFFFFF9))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-122">Winlogon affiche la boîte de dialogue **déconnexion refusée** .</span><span class="sxs-lookup"><span data-stu-id="662c1-122">Winlogon is displaying the **Disconnect Refused** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span data-ttu-id="662c1-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Arbitrage \_ \_ \_ Options de rapprochement de code** (-4 (0xFFFFFFFC))</span><span class="sxs-lookup"><span data-stu-id="662c1-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRATION\_CODE\_RECONN\_OPTIONS** (-4 (0xFFFFFFFC))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-124">Winlogon affiche la boîte de dialogue **reconnexion** .</span><span class="sxs-lookup"><span data-stu-id="662c1-124">Winlogon is displaying the **Reconnect** dialog box.</span></span>

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span data-ttu-id="662c1-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Erreur \_ \_Accès au code \_ refusé** (-1 (0xFFFFFFFF))</span><span class="sxs-lookup"><span data-stu-id="662c1-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR\_CODE\_ACCESS\_DENIED** (-1 (0xFFFFFFFF))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-126">L’accès a été refusé à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="662c1-126">The user was denied access.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span data-ttu-id="662c1-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Ouverture de session \_ \_ \_ Mot de passe incorrect en échec** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="662c1-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON\_FAILED\_BAD\_PASSWORD** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-128">L’ouverture de session a échoué car les informations d’identification d’ouverture de session ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="662c1-128">The logon failed because the logon credentials are not valid.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span data-ttu-id="662c1-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Ouverture de session \_ \_Autre échec** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="662c1-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON\_FAILED\_OTHER** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-130">Une autre erreur d’ouverture de session ou de postconnexion s’est produite.</span><span class="sxs-lookup"><span data-stu-id="662c1-130">Another logon or post-logon error occurred.</span></span> <span data-ttu-id="662c1-131">Le client Bureau à distance affiche un écran d’ouverture de session pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="662c1-131">The Remote Desktop client displays a logon screen to the user.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span data-ttu-id="662c1-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Ouverture de session \_ ÉCHEC \_ de la mise à jour du \_ mot de passe** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="662c1-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON\_FAILED\_UPDATE\_PASSWORD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-133">Le mot de passe a expiré.</span><span class="sxs-lookup"><span data-stu-id="662c1-133">The password is expired.</span></span> <span data-ttu-id="662c1-134">L’utilisateur doit mettre à jour son mot de passe pour continuer à se connecter.</span><span class="sxs-lookup"><span data-stu-id="662c1-134">The user must update their password to continue logging on.</span></span>

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span data-ttu-id="662c1-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Ouverture de session \_ AVERTISSEMENT** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="662c1-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON\_WARNING** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-136">Le client Bureau à distance affiche une boîte de dialogue qui contient des informations importantes pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="662c1-136">The Remote Desktop client displays a dialog box that contains important information for the user.</span></span>

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span data-ttu-id="662c1-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**État \_ \_Restriction de compte** (-1073741714 (0xC000006E))</span><span class="sxs-lookup"><span data-stu-id="662c1-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**STATUS\_ACCOUNT\_RESTRICTION** (-1073741714 (0xC000006E))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-138">Le nom d’utilisateur et les informations d’authentification sont valides, mais l’authentification a été bloquée en raison de restrictions sur le compte d’utilisateur, telles que les restrictions de l’heure de la journée.</span><span class="sxs-lookup"><span data-stu-id="662c1-138">The user name and authentication information are valid, but authentication was blocked due to restrictions on the user account, such as time-of-day restrictions.</span></span>

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span data-ttu-id="662c1-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**État \_ \_Échec d’ouverture de session** (-1073741715 (0xC000006D))</span><span class="sxs-lookup"><span data-stu-id="662c1-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**STATUS\_LOGON\_FAILURE** (-1073741715 (0xC000006D))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-140">La tentative d’ouverture de session n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="662c1-140">The attempted logon is not valid.</span></span> <span data-ttu-id="662c1-141">Cela est dû à un nom d’utilisateur incorrect ou à des informations d’authentification incorrectes.</span><span class="sxs-lookup"><span data-stu-id="662c1-141">This is due to either an incorrect user name or incorrect authentication information.</span></span>

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span data-ttu-id="662c1-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**État \_ Le mot de passe \_ doit être \_ modifié** (-1073741276 (0xC0000224))</span><span class="sxs-lookup"><span data-stu-id="662c1-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**STATUS\_PASSWORD\_MUST\_CHANGE** (-1073741276 (0xC0000224))</span></span>


</dt> <dd>

<span data-ttu-id="662c1-143">Le mot de passe a expiré.</span><span class="sxs-lookup"><span data-stu-id="662c1-143">The password is expired.</span></span> <span data-ttu-id="662c1-144">L’utilisateur doit mettre à jour son mot de passe pour continuer à se connecter.</span><span class="sxs-lookup"><span data-stu-id="662c1-144">The user must update their password to continue logging on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="662c1-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="662c1-145">Return value</span></span>

<span data-ttu-id="662c1-146">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="662c1-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="662c1-147">Notes</span><span class="sxs-lookup"><span data-stu-id="662c1-147">Remarks</span></span>

<span data-ttu-id="662c1-148">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant qu’une erreur d’ouverture de session s’est produite.</span><span class="sxs-lookup"><span data-stu-id="662c1-148">Implement this method in your event sink to receive notification that a logon error has occurred.</span></span>

<span data-ttu-id="662c1-149">Cette liste de codes n’est pas exhaustive.</span><span class="sxs-lookup"><span data-stu-id="662c1-149">This list of codes is not exhaustive.</span></span>

## <a name="requirements"></a><span data-ttu-id="662c1-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="662c1-150">Requirements</span></span>



| <span data-ttu-id="662c1-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="662c1-151">Requirement</span></span> | <span data-ttu-id="662c1-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="662c1-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="662c1-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="662c1-153">Minimum supported client</span></span><br/> | <span data-ttu-id="662c1-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="662c1-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="662c1-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="662c1-155">Minimum supported server</span></span><br/> | <span data-ttu-id="662c1-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="662c1-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="662c1-157">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="662c1-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="662c1-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="662c1-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="662c1-159">DLL</span><span class="sxs-lookup"><span data-stu-id="662c1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="662c1-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="662c1-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="662c1-161">IID</span><span class="sxs-lookup"><span data-stu-id="662c1-161">IID</span></span><br/>                      | <span data-ttu-id="662c1-162">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="662c1-162">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="662c1-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="662c1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="662c1-164">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="662c1-164">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





