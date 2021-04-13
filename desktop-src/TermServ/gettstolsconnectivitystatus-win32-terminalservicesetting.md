---
title: Méthode GetTStoLSConnectivityStatus de la classe Win32_TerminalServiceSetting
description: Détermine l’état de la connectivité entre Services Bureau à distance et un serveur de licences.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetTStoLSConnectivityStatus
- Services Bureau à distance de la méthode GetTStoLSConnectivityStatus, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465795"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="6352b-106">Méthode GetTStoLSConnectivityStatus de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="6352b-106">GetTStoLSConnectivityStatus method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="6352b-107">Détermine l’état de la connectivité entre Services Bureau à distance et un serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6352b-107">Determines the connectivity status between Remote Desktop Services and a license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6352b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6352b-108">Syntax</span></span>


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6352b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6352b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6352b-110">*Nom du serveur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6352b-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6352b-111">Nom du serveur de licences dont l’état de connectivité doit être vérifié.</span><span class="sxs-lookup"><span data-stu-id="6352b-111">The name of the license server to check the connectivity status of.</span></span>

</dd> <dt>

<span data-ttu-id="6352b-112">*TStoLSConnectivityStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6352b-112">*TStoLSConnectivityStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6352b-113">Valeur qui indique l’état de connectivité du serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6352b-113">A value that indicates the connectivity status of the license server.</span></span> <span data-ttu-id="6352b-114">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6352b-114">This can be one of the following values.</span></span>

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span data-ttu-id="6352b-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ CONNECTable \_ inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6352b-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS\_CONNECTABLE\_UNKNOWN** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-116">Impossible de déterminer l’état de la connectivité.</span><span class="sxs-lookup"><span data-stu-id="6352b-116">The connectivity status cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span data-ttu-id="6352b-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ \_ \_ WS08R2 valide connectable** (1)</span><span class="sxs-lookup"><span data-stu-id="6352b-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS\_CONNECTABLE\_VALID\_WS08R2** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-118">Services Bureau à distance pouvez vous connecter au serveur de licences Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6352b-118">Remote Desktop Services can connect to the Windows Server 2008 R2 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span data-ttu-id="6352b-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ \_ \_ WS08 valide connectable** (2)</span><span class="sxs-lookup"><span data-stu-id="6352b-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS\_CONNECTABLE\_VALID\_WS08** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-120">Services Bureau à distance pouvez vous connecter au serveur de licences Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6352b-120">Remote Desktop Services can connect to the Windows Server 2008 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span data-ttu-id="6352b-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ Incompatibilité \_ beta \_ RTM \_ connectable** (3)</span><span class="sxs-lookup"><span data-stu-id="6352b-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS\_CONNECTABLE\_BETA\_RTM\_MISMATCH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-122">Services Bureau à distance peut se connecter au serveur de licences, mais l’un des serveurs exécute une version bêta du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6352b-122">Remote Desktop Services can connect to the license server, but one of the servers is running a beta version of the operating system.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span data-ttu-id="6352b-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ \_ \_ Version inférieure connectable** (4)</span><span class="sxs-lookup"><span data-stu-id="6352b-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS\_CONNECTABLE\_LOWER\_VERSION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-124">Services Bureau à distance peut se connecter au serveur de licences, mais il existe une incompatibilité entre le serveur de licences et le serveur hôte Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="6352b-124">Remote Desktop Services can connect to the license server, but there is an incompatibility between the license server and the Remote Desktop Services host server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span data-ttu-id="6352b-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ CONNEXION \_ non \_ dans \_ TSCGROUP** (5)</span><span class="sxs-lookup"><span data-stu-id="6352b-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS\_CONNECTABLE\_NOT\_IN\_TSCGROUP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-126">La stratégie de groupe de sécurité est activée dans le serveur de licences, mais Services Bureau à distance ne fait pas partie de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="6352b-126">Security group policy is enabled in license server, but Remote Desktop Services is not a part of the group policy.</span></span>

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span data-ttu-id="6352b-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ NON \_ connectable** (6)</span><span class="sxs-lookup"><span data-stu-id="6352b-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS\_NOT\_CONNECTABLE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-128">Services Bureau à distance ne peut pas se connecter au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6352b-128">Remote Desktop Services cannot connect to the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span data-ttu-id="6352b-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ \_ \_ Validité inconnue connectable** (7)</span><span class="sxs-lookup"><span data-stu-id="6352b-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS\_CONNECTABLE\_UNKNOWN\_VALIDITY** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-130">Le serveur de licences peut être connecté à, mais la validité de la connexion ne peut pas être déterminée.</span><span class="sxs-lookup"><span data-stu-id="6352b-130">The license server can be connected to, but the validity of the connection cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span data-ttu-id="6352b-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ CONNECTable \_ mais \_ accès \_ refusé** (8)</span><span class="sxs-lookup"><span data-stu-id="6352b-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS\_CONNECTABLE\_BUT\_ACCESS\_DENIED** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-132">Services Bureau à distance peut se connecter au serveur de licences, mais le compte d’utilisateur ne dispose pas de privilèges d’administrateur sur le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6352b-132">Remote Desktop Services can connect to the license server, but the user account does not have administrator privileges on the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span data-ttu-id="6352b-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ \_ \_ WS08R2 \_ VDI valide connectable** (9)</span><span class="sxs-lookup"><span data-stu-id="6352b-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS\_CONNECTABLE\_VALID\_WS08R2\_VDI** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-134">Services Bureau à distance pouvez vous connecter au serveur VDI (Virtual Desktop Infrastructure) de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6352b-134">Remote Desktop Services can connect to the Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) server.</span></span>

<span data-ttu-id="6352b-135">**Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6352b-135">**Windows Server 2008 R2:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span data-ttu-id="6352b-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ \_Fonctionnalité connectable \_ non \_ prise en charge** (10)</span><span class="sxs-lookup"><span data-stu-id="6352b-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS\_CONNECTABLE\_FEATURE\_NOT\_SUPPORTED** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-137">La fonctionnalité n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6352b-137">The feature is not supported.</span></span>

<span data-ttu-id="6352b-138">**Windows server 2008 R2 et Windows server 2008 R2 avec SP1 :** Cette valeur n’est pas prise en charge avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6352b-138">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span data-ttu-id="6352b-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ CONNECTable \_ valide \_ ls** (11)</span><span class="sxs-lookup"><span data-stu-id="6352b-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS\_CONNECTABLE\_VALID\_LS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6352b-140">Le serveur de licences est valide.</span><span class="sxs-lookup"><span data-stu-id="6352b-140">The license server is valid.</span></span>

<span data-ttu-id="6352b-141">**Windows server 2008 R2 et Windows server 2008 R2 avec SP1 :** Cette valeur n’est pas prise en charge avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6352b-141">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6352b-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6352b-142">Return value</span></span>

<span data-ttu-id="6352b-143">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="6352b-143">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6352b-144">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6352b-144">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6352b-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6352b-145">Requirements</span></span>



| <span data-ttu-id="6352b-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6352b-146">Requirement</span></span> | <span data-ttu-id="6352b-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="6352b-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6352b-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6352b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6352b-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6352b-149">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6352b-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6352b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6352b-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6352b-151">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6352b-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6352b-152">Namespace</span></span><br/>                | <span data-ttu-id="6352b-153">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="6352b-153">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6352b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="6352b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6352b-155"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6352b-155"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6352b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6352b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6352b-157"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6352b-157"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6352b-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6352b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6352b-159">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6352b-159">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





