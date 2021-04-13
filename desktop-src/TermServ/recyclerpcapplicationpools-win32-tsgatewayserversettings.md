---
title: Méthode RecycleRpcApplicationPools de la classe Win32_TSGatewayServerSettings
description: Recycle les pools d’applications RPC dans IIS.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RecycleRpcApplicationPools
- Services Bureau à distance de la méthode RecycleRpcApplicationPools, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode RecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465114"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8577f-106">Méthode RecycleRpcApplicationPools de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="8577f-106">RecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8577f-107">Recycle les pools d’applications RPC dans IIS.</span><span class="sxs-lookup"><span data-stu-id="8577f-107">Recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="8577f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8577f-108">Syntax</span></span>


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="8577f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8577f-109">Parameters</span></span>

<span data-ttu-id="8577f-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8577f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8577f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8577f-111">Return value</span></span>

<span data-ttu-id="8577f-112">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8577f-112">Type: **uint32**</span></span>

<span data-ttu-id="8577f-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="8577f-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8577f-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="8577f-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8577f-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8577f-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8577f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8577f-116">Remarks</span></span>

<span data-ttu-id="8577f-117">L’appel de cette méthode entraîne la déconnexion de toutes les connexions existantes.</span><span class="sxs-lookup"><span data-stu-id="8577f-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="8577f-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8577f-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8577f-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="8577f-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8577f-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8577f-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8577f-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="8577f-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8577f-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8577f-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8577f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8577f-123">Requirements</span></span>



| <span data-ttu-id="8577f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8577f-124">Requirement</span></span> | <span data-ttu-id="8577f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8577f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8577f-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8577f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8577f-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8577f-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8577f-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8577f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8577f-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8577f-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="8577f-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8577f-130">Namespace</span></span><br/>                | <span data-ttu-id="8577f-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8577f-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8577f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8577f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8577f-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8577f-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8577f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8577f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8577f-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8577f-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8577f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8577f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8577f-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8577f-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="8577f-138">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="8577f-138">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

