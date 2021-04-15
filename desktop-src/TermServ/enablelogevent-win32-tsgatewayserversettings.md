---
title: Méthode EnableLogEvent de la classe Win32_TSGatewayServerSettings
description: Active ou désactive la journalisation du type d’événement spécifié.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableLogEvent
- Services Bureau à distance de la méthode EnableLogEvent, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnableLogEvent
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467042"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="e7d01-106">Méthode EnableLogEvent de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="e7d01-106">EnableLogEvent method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e7d01-107">Active ou désactive la journalisation du type d’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="e7d01-107">Enables or disables logging of the specified event type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d01-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7d01-108">Syntax</span></span>


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="e7d01-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7d01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d01-110">*EventName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7d01-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-111">Nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e7d01-111">Name of the event.</span></span> <span data-ttu-id="e7d01-112">Cette valeur doit être récupérée à l’aide de la méthode [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d01-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="e7d01-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="e7d01-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-114">L’utilisateur a réussi à se déconnecter de la ressource.</span><span class="sxs-lookup"><span data-stu-id="e7d01-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e7d01-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="e7d01-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-116">L’utilisateur n’a pas pu se connecter à la ressource.</span><span class="sxs-lookup"><span data-stu-id="e7d01-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e7d01-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="e7d01-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-118">L’utilisateur n’a pas d’autorisation de connexion.</span><span class="sxs-lookup"><span data-stu-id="e7d01-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="e7d01-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="e7d01-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-120">L’utilisateur n’a pas d’autorisation de ressource.</span><span class="sxs-lookup"><span data-stu-id="e7d01-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="e7d01-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="e7d01-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-122">L’utilisateur a réussi à se connecter à la ressource.</span><span class="sxs-lookup"><span data-stu-id="e7d01-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e7d01-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="e7d01-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-124">L’utilisateur a réussi à réussir l’autorisation de connexion.</span><span class="sxs-lookup"><span data-stu-id="e7d01-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="e7d01-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="e7d01-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-126">L’utilisateur a réussi à réussir l’autorisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="e7d01-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e7d01-127">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7d01-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d01-128">Spécifie si l’événement doit être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="e7d01-128">Specifies whether the event should be enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d01-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7d01-129">Return value</span></span>

<span data-ttu-id="e7d01-130">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e7d01-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e7d01-131">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e7d01-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e7d01-132">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e7d01-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d01-133">Notes</span><span class="sxs-lookup"><span data-stu-id="e7d01-133">Remarks</span></span>

<span data-ttu-id="e7d01-134">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e7d01-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e7d01-135">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e7d01-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e7d01-136">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e7d01-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e7d01-137">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e7d01-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e7d01-138">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e7d01-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d01-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7d01-139">Requirements</span></span>



| <span data-ttu-id="e7d01-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7d01-140">Requirement</span></span> | <span data-ttu-id="e7d01-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7d01-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d01-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d01-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d01-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d01-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e7d01-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d01-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d01-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7d01-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e7d01-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7d01-146">Namespace</span></span><br/>                | <span data-ttu-id="e7d01-147">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e7d01-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e7d01-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e7d01-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7d01-149"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7d01-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7d01-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e7d01-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7d01-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7d01-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e7d01-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7d01-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d01-153">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="e7d01-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="e7d01-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="e7d01-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

