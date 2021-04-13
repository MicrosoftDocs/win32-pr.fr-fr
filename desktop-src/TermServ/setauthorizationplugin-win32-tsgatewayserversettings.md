---
title: Méthode SetAuthorizationPlugin de la classe Win32_TSGatewayServerSettings
description: Définit le plug-in d’autorisation actuel pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: 236c9cca-4efc-433a-8f1f-e3044e0588b3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetAuthorizationPlugin
- Services Bureau à distance de la méthode SetAuthorizationPlugin, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetAuthorizationPlugin
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthorizationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdb3cb07a7c0a30e84245a2d22e383dea168247
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508838"
---
# <a name="setauthorizationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="9692d-106">Méthode SetAuthorizationPlugin de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="9692d-106">SetAuthorizationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="9692d-107">Définit le plug-in d’autorisation actuel pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="9692d-107">Sets the current authorization plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9692d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9692d-108">Syntax</span></span>


```mof
uint32 SetAuthorizationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="9692d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9692d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9692d-110">*PluginName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9692d-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9692d-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9692d-111">Type: **string**</span></span>

<span data-ttu-id="9692d-112">Nom du nouveau plug-in d’autorisation actuel.</span><span class="sxs-lookup"><span data-stu-id="9692d-112">The name of the new current authorization plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9692d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9692d-113">Return value</span></span>

<span data-ttu-id="9692d-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9692d-114">Type: **uint32**</span></span>

<span data-ttu-id="9692d-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="9692d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9692d-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="9692d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9692d-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9692d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9692d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9692d-118">Remarks</span></span>

<span data-ttu-id="9692d-119">Vous devez appeler la méthode [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) pour autoriser le plug-in d’autorisation à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="9692d-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authorization plug-in to work.</span></span>

<span data-ttu-id="9692d-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9692d-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9692d-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9692d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9692d-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9692d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9692d-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9692d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9692d-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9692d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9692d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9692d-125">Requirements</span></span>



| <span data-ttu-id="9692d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9692d-126">Requirement</span></span> | <span data-ttu-id="9692d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9692d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9692d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9692d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9692d-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9692d-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9692d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9692d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9692d-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9692d-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="9692d-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9692d-132">Namespace</span></span><br/>                | <span data-ttu-id="9692d-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="9692d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9692d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9692d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9692d-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9692d-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9692d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9692d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9692d-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9692d-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9692d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9692d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9692d-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="9692d-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="9692d-140">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="9692d-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

