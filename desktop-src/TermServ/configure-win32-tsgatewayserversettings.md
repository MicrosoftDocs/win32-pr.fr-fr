---
title: Configurer la méthode de la classe Win32_TSGatewayServerSettings
description: Configure les paramètres IIS et RPC requis par le service de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Configurer la méthode Services Bureau à distance
- Configurez la méthode Services Bureau à distance, Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, configurer la méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1880e1a9811c8aab2660993c6c8ab05061163e1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032527"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="e4344-106">Configurer la méthode de la \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="e4344-106">Configure method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e4344-107">Configure les paramètres IIS et RPC requis par le service de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="e4344-107">Configures the IIS and RPC settings required by the Remote Desktop Gateway (RD Gateway) service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4344-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4344-108">Syntax</span></span>


```mof
uint32 Configure();
```



## <a name="parameters"></a><span data-ttu-id="e4344-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4344-109">Parameters</span></span>

<span data-ttu-id="e4344-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4344-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4344-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4344-111">Return value</span></span>

<span data-ttu-id="e4344-112">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4344-112">Type: **uint32**</span></span>

<span data-ttu-id="e4344-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e4344-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e4344-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e4344-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e4344-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4344-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4344-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e4344-116">Remarks</span></span>

<span data-ttu-id="e4344-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e4344-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e4344-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e4344-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e4344-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e4344-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e4344-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e4344-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e4344-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e4344-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4344-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4344-122">Requirements</span></span>



| <span data-ttu-id="e4344-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4344-123">Requirement</span></span> | <span data-ttu-id="e4344-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4344-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4344-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4344-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e4344-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4344-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e4344-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4344-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e4344-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4344-128">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="e4344-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e4344-129">Namespace</span></span><br/>                | <span data-ttu-id="e4344-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e4344-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e4344-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e4344-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4344-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4344-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4344-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e4344-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4344-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4344-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e4344-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4344-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4344-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="e4344-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

