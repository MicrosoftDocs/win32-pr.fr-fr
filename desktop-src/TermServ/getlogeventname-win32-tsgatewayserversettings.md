---
title: Méthode GetLogEventName de la classe Win32_TSGatewayServerSettings
description: Retourne le nom d’événement du journal pour l’index d’événements de journal spécifié.
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetLogEventName
- Services Bureau à distance de la méthode GetLogEventName, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode GetLogEventName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e9c608b7a12d3de48d75ecd5651df94d0267fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511373"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="2b8cb-106">Méthode GetLogEventName de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="2b8cb-106">GetLogEventName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="2b8cb-107">Retourne le nom d’événement du journal pour l’index d’événements de journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-107">Returns the log event name for the specified log event index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b8cb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b8cb-108">Syntax</span></span>


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a><span data-ttu-id="2b8cb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b8cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b8cb-110">*EventIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b8cb-110">*EventIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b8cb-111">Index de l’événement de journal.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-111">Index of the log event.</span></span> <span data-ttu-id="2b8cb-112">La valeur doit être comprise entre zéro et la valeur de la propriété **MaxLogEvents** .</span><span class="sxs-lookup"><span data-stu-id="2b8cb-112">The value must be between zero and the value of the **MaxLogEvents** property.</span></span>

</dd> <dt>

<span data-ttu-id="2b8cb-113">*EventName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2b8cb-113">*EventName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b8cb-114">Nom de l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-114">Name of the specified event.</span></span> <span data-ttu-id="2b8cb-115">La liste suivante affiche les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-115">The following list displays the possible values.</span></span>

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span data-ttu-id="2b8cb-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span></span>


</dt> <dd>

<span data-ttu-id="2b8cb-117">L’utilisateur a réussi à se déconnecter de la ressource.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-117">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span data-ttu-id="2b8cb-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="2b8cb-119">L’utilisateur n’a pas pu se connecter à la ressource.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-119">User failed to connect to the resource.</span></span>

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="2b8cb-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="2b8cb-121">L’utilisateur n’a pas d’autorisation de connexion.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-121">User failed connection authorization.</span></span>

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="2b8cb-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="2b8cb-123">L’utilisateur n’a pas d’autorisation de ressource.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-123">User failed resource authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span data-ttu-id="2b8cb-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="2b8cb-125">L’utilisateur a réussi à se connecter à la ressource.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-125">User successfully connected to the resource.</span></span>

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="2b8cb-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="2b8cb-127">L’utilisateur a réussi à réussir l’autorisation de connexion.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-127">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="2b8cb-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="2b8cb-129">L’utilisateur a réussi à réussir l’autorisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-129">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b8cb-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b8cb-130">Return value</span></span>

<span data-ttu-id="2b8cb-131">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2b8cb-132">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2b8cb-133">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2b8cb-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b8cb-134">Notes</span><span class="sxs-lookup"><span data-stu-id="2b8cb-134">Remarks</span></span>

<span data-ttu-id="2b8cb-135">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2b8cb-136">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2b8cb-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2b8cb-137">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2b8cb-138">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2b8cb-139">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2b8cb-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8cb-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b8cb-140">Requirements</span></span>



| <span data-ttu-id="2b8cb-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b8cb-141">Requirement</span></span> | <span data-ttu-id="2b8cb-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b8cb-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8cb-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b8cb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8cb-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b8cb-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2b8cb-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b8cb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8cb-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b8cb-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2b8cb-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2b8cb-147">Namespace</span></span><br/>                | <span data-ttu-id="2b8cb-148">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2b8cb-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2b8cb-149">MOF</span><span class="sxs-lookup"><span data-stu-id="2b8cb-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b8cb-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b8cb-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b8cb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="2b8cb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b8cb-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b8cb-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2b8cb-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b8cb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8cb-154">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-154">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="2b8cb-155">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-155">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="2b8cb-156">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="2b8cb-156">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 

