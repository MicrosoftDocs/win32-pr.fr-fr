---
title: Méthode IsLogEventEnabled de la classe Win32_TSGatewayServerSettings
description: Indique si le type de journal des événements spécifié est activé.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLogEventEnabled
- Services Bureau à distance de la méthode IsLogEventEnabled, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510986"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="73083-106">Méthode IsLogEventEnabled de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="73083-106">IsLogEventEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="73083-107">Indique si le type de journal des événements spécifié est activé.</span><span class="sxs-lookup"><span data-stu-id="73083-107">Indicates whether the specified event log type is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="73083-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73083-108">Syntax</span></span>


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="73083-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73083-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73083-110">*EventName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73083-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73083-111">Nom du type de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="73083-111">Name of the event log type.</span></span> <span data-ttu-id="73083-112">Cette valeur doit être récupérée à l’aide de la méthode [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="73083-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="73083-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="73083-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="73083-114">L’utilisateur a réussi à se déconnecter de la ressource.</span><span class="sxs-lookup"><span data-stu-id="73083-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="73083-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="73083-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="73083-116">L’utilisateur n’a pas pu se connecter à la ressource.</span><span class="sxs-lookup"><span data-stu-id="73083-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="73083-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="73083-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="73083-118">L’utilisateur n’a pas d’autorisation de connexion.</span><span class="sxs-lookup"><span data-stu-id="73083-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="73083-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="73083-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="73083-120">L’utilisateur n’a pas d’autorisation de ressource.</span><span class="sxs-lookup"><span data-stu-id="73083-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="73083-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="73083-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="73083-122">L’utilisateur a réussi à se connecter à la ressource.</span><span class="sxs-lookup"><span data-stu-id="73083-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="73083-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="73083-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="73083-124">L’utilisateur a réussi à réussir l’autorisation de connexion.</span><span class="sxs-lookup"><span data-stu-id="73083-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="73083-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="73083-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="73083-126">L’utilisateur a réussi à réussir l’autorisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="73083-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="73083-127">*Activé* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="73083-127">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73083-128">Indique si le type de journal des événements spécifié est activé.</span><span class="sxs-lookup"><span data-stu-id="73083-128">Indicates whether the specified event log type is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73083-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73083-129">Return value</span></span>

<span data-ttu-id="73083-130">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="73083-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="73083-131">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="73083-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="73083-132">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="73083-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="73083-133">Notes</span><span class="sxs-lookup"><span data-stu-id="73083-133">Remarks</span></span>

<span data-ttu-id="73083-134">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="73083-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="73083-135">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="73083-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73083-136">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="73083-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73083-137">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="73083-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73083-138">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="73083-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73083-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73083-139">Requirements</span></span>



| <span data-ttu-id="73083-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73083-140">Requirement</span></span> | <span data-ttu-id="73083-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="73083-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73083-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73083-142">Minimum supported client</span></span><br/> | <span data-ttu-id="73083-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="73083-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="73083-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73083-144">Minimum supported server</span></span><br/> | <span data-ttu-id="73083-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73083-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="73083-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="73083-146">Namespace</span></span><br/>                | <span data-ttu-id="73083-147">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="73083-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="73083-148">MOF</span><span class="sxs-lookup"><span data-stu-id="73083-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73083-149"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73083-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="73083-150">DLL</span><span class="sxs-lookup"><span data-stu-id="73083-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73083-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73083-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="73083-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73083-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73083-153">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="73083-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="73083-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="73083-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

