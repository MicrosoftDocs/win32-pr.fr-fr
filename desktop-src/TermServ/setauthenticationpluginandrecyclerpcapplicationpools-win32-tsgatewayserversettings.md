---
title: Méthode SetAuthenticationPluginAndRecycleRpcApplicationPools de la classe Win32_TSGatewayServerSettings
description: Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) et recycle les pools d’applications RPC dans IIS.
ms.assetid: cdceaf50-3d0a-4af0-9ad5-fb43760fcf7b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetAuthenticationPluginAndRecycleRpcApplicationPools
- Services Bureau à distance de la méthode SetAuthenticationPluginAndRecycleRpcApplicationPools, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetAuthenticationPluginAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPluginAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b234e04c349d20ea178de12f050190b30193d444
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740717"
---
# <a name="setauthenticationpluginandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="c2340-106">Méthode SetAuthenticationPluginAndRecycleRpcApplicationPools de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="c2340-106">SetAuthenticationPluginAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="c2340-107">Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) et recycle les pools d’applications RPC dans IIS.</span><span class="sxs-lookup"><span data-stu-id="c2340-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

<span data-ttu-id="c2340-108">Cette méthode équivaut à appeler les méthodes [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) et [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="c2340-108">This method is equivalent to calling the [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) and [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) methods in sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2340-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2340-109">Syntax</span></span>


```mof
uint32 SetAuthenticationPluginAndRecycleRpcApplicationPools(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="c2340-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2340-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2340-111">*PluginName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2340-111">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2340-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2340-112">Type: **string**</span></span>

<span data-ttu-id="c2340-113">Nom du plug-in d’authentification</span><span class="sxs-lookup"><span data-stu-id="c2340-113">Name of the authentication plug-in</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2340-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2340-114">Return value</span></span>

<span data-ttu-id="c2340-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2340-115">Type: **uint32**</span></span>

<span data-ttu-id="c2340-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c2340-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c2340-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c2340-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c2340-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c2340-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2340-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c2340-119">Remarks</span></span>

<span data-ttu-id="c2340-120">L’appel de cette méthode entraîne la déconnexion de toutes les connexions existantes.</span><span class="sxs-lookup"><span data-stu-id="c2340-120">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="c2340-121">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c2340-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c2340-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c2340-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c2340-123">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c2340-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c2340-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c2340-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c2340-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c2340-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2340-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2340-126">Requirements</span></span>



| <span data-ttu-id="c2340-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2340-127">Requirement</span></span> | <span data-ttu-id="c2340-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2340-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2340-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2340-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2340-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2340-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c2340-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2340-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2340-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2340-132">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c2340-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c2340-133">Namespace</span></span><br/>                | <span data-ttu-id="c2340-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c2340-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c2340-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c2340-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2340-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2340-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2340-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c2340-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2340-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2340-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c2340-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2340-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2340-140">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="c2340-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="c2340-141">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="c2340-141">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="c2340-142">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="c2340-142">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

