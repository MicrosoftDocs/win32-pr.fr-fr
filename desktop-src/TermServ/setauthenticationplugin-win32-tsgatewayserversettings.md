---
title: Méthode SetAuthenticationPlugin de la classe Win32_TSGatewayServerSettings
description: Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetAuthenticationPlugin
- Services Bureau à distance de la méthode SetAuthenticationPlugin, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetAuthenticationPlugin
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b5b332dd288a01f96b0eb0b3a99e7e45269cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743501"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="066b6-106">Méthode SetAuthenticationPlugin de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="066b6-106">SetAuthenticationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="066b6-107">Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="066b6-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="066b6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="066b6-108">Syntax</span></span>


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="066b6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="066b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="066b6-110">*PluginName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="066b6-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066b6-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="066b6-111">Type: **string**</span></span>

<span data-ttu-id="066b6-112">Nom du nouveau plug-in d’authentification actuel.</span><span class="sxs-lookup"><span data-stu-id="066b6-112">The name of the new current authentication plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="066b6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="066b6-113">Return value</span></span>

<span data-ttu-id="066b6-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="066b6-114">Type: **uint32**</span></span>

<span data-ttu-id="066b6-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="066b6-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="066b6-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="066b6-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="066b6-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="066b6-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="066b6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="066b6-118">Remarks</span></span>

<span data-ttu-id="066b6-119">Vous devez appeler la méthode [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) pour autoriser le plug-in d’authentification à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="066b6-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authentication plug-in to work.</span></span>

<span data-ttu-id="066b6-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="066b6-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="066b6-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="066b6-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="066b6-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="066b6-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="066b6-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="066b6-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="066b6-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="066b6-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="066b6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="066b6-125">Requirements</span></span>



| <span data-ttu-id="066b6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="066b6-126">Requirement</span></span> | <span data-ttu-id="066b6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="066b6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="066b6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="066b6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="066b6-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="066b6-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="066b6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="066b6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="066b6-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="066b6-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="066b6-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="066b6-132">Namespace</span></span><br/>                | <span data-ttu-id="066b6-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="066b6-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="066b6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="066b6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="066b6-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="066b6-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="066b6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="066b6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="066b6-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="066b6-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="066b6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="066b6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066b6-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="066b6-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="066b6-140">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="066b6-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

