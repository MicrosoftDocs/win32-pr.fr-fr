---
title: Méthode RestoreDefaults de la classe Win32_TSPermissionsSetting (Netfw. h)
description: Restaure les valeurs de jeu d’autorisations par défaut pour le terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RestoreDefaults
- Services Bureau à distance de la méthode RestoreDefaults, classe Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de la classe Services Bureau à distance, méthode RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843389"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="0573e-106">Méthode RestoreDefaults de la \_ classe Win32 TSPermissionsSetting</span><span class="sxs-lookup"><span data-stu-id="0573e-106">RestoreDefaults method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="0573e-107">La méthode **RestoreDefaults** restaure les valeurs de jeu d’autorisations par défaut pour le terminal.</span><span class="sxs-lookup"><span data-stu-id="0573e-107">The **RestoreDefaults** method restores the default permission set values for the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="0573e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0573e-108">Syntax</span></span>


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a><span data-ttu-id="0573e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0573e-109">Parameters</span></span>

<span data-ttu-id="0573e-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0573e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0573e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0573e-111">Return value</span></span>

<span data-ttu-id="0573e-112">Retourne une réussite en cas de réussite, sinon échec.</span><span class="sxs-lookup"><span data-stu-id="0573e-112">Returns Success on success, otherwise Failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0573e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0573e-113">Remarks</span></span>

<span data-ttu-id="0573e-114">Les autorisations par défaut sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0573e-114">Default permissions are the following:</span></span>

-   <span data-ttu-id="0573e-115">Les comptes administrateurs, système et Bureau à distance Assistant aide disposent de toutes les [autorisations services Bureau à distance](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0573e-115">The Administrators, System, and Remote Desktop Help Assistant accounts have all [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>
-   <span data-ttu-id="0573e-116">Le compte Bureau à distance Users dispose de l’autorisation Logon, Connect, Query information et Send message.</span><span class="sxs-lookup"><span data-stu-id="0573e-116">The Remote Desktop Users account has Logon, Connect, Query Information, and Send Message permission.</span></span>
-   <span data-ttu-id="0573e-117">Les comptes service local et service réseau disposent des informations de requête et de l’autorisation Envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="0573e-117">The Local Service and Network Service accounts have Query Information, and Send Message permission.</span></span>

<span data-ttu-id="0573e-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0573e-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0573e-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0573e-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0573e-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0573e-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0573e-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0573e-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0573e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0573e-122">Requirements</span></span>



| <span data-ttu-id="0573e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0573e-123">Requirement</span></span> | <span data-ttu-id="0573e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0573e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0573e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0573e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0573e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0573e-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0573e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0573e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0573e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0573e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0573e-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0573e-129">Namespace</span></span><br/>                | <span data-ttu-id="0573e-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0573e-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0573e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0573e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0573e-132"><dt>Netfw. h</dt></span><span class="sxs-lookup"><span data-stu-id="0573e-132"><dt>Netfw.h</dt></span></span> </dl>      |
| <span data-ttu-id="0573e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0573e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0573e-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0573e-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0573e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0573e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0573e-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0573e-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0573e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0573e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0573e-138">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0573e-138">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

