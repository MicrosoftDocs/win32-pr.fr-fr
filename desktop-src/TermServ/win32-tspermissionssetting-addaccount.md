---
title: Méthode AddAccount de la classe Win32_TSPermissionsSetting (Faxcomex. h)
description: La méthode AddAccount prépare l’ajout d’un compte au terminal avec le jeu d’autorisations spécifié. Vous pouvez ajouter des utilisateurs, des groupes ou des ordinateurs.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddAccount
- Services Bureau à distance de la méthode AddAccount, classe Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de la classe Services Bureau à distance, méthode AddAccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465962"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="763a4-107">Méthode AddAccount de la \_ classe Win32 TSPermissionsSetting</span><span class="sxs-lookup"><span data-stu-id="763a4-107">AddAccount method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="763a4-108">La méthode **AddAccount** prépare l’ajout d’un compte au terminal avec le jeu d’autorisations spécifié.</span><span class="sxs-lookup"><span data-stu-id="763a4-108">The **AddAccount** method prepares to add an account to the terminal with the specified permission set.</span></span> <span data-ttu-id="763a4-109">Vous pouvez ajouter des utilisateurs, des groupes ou des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="763a4-109">You can add users, groups, or computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="763a4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="763a4-110">Syntax</span></span>


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a><span data-ttu-id="763a4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="763a4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="763a4-112">*AccountName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="763a4-112">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="763a4-113">Nom du compte à ajouter au terminal.</span><span class="sxs-lookup"><span data-stu-id="763a4-113">The name of the account to add to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="763a4-114">*PermissionPreSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="763a4-114">*PermissionPreSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="763a4-115">Jeu d’autorisations à associer au compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="763a4-115">The set of permissions to associate with the specified account.</span></span> <span data-ttu-id="763a4-116">Ce paramètre peut avoir une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="763a4-116">This parameter can be any or all of the following values.</span></span> <span data-ttu-id="763a4-117">Pour plus d’informations, consultez [services Bureau à distance autorisations](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="763a4-117">For more information, see [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span data-ttu-id="763a4-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**Station \_ de \_Accès invité** (0)</span><span class="sxs-lookup"><span data-stu-id="763a4-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION\_GUEST\_ACCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="763a4-119">Le compte dispose d’une autorisation d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="763a4-119">The account has Logon permission.</span></span>

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span data-ttu-id="763a4-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**Station \_ de \_Accès utilisateur** (1)</span><span class="sxs-lookup"><span data-stu-id="763a4-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION\_USER\_ACCESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="763a4-121">Le compte dispose des autorisations suivantes : ouverture de session, informations sur la requête, envoi de message et connexion.</span><span class="sxs-lookup"><span data-stu-id="763a4-121">The account has the following permissions: Logon, Query Information, Send Message, and Connect.</span></span>

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span data-ttu-id="763a4-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**Station \_ de TOUT \_ accès** (2)</span><span class="sxs-lookup"><span data-stu-id="763a4-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION\_ALL\_ACCESS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="763a4-123">Le compte dispose de toutes les autorisations de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="763a4-123">The account has all Remote Desktop Services Permissions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="763a4-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="763a4-124">Return value</span></span>

<span data-ttu-id="763a4-125">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="763a4-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="763a4-126">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="763a4-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="763a4-127">Notes</span><span class="sxs-lookup"><span data-stu-id="763a4-127">Remarks</span></span>

<span data-ttu-id="763a4-128">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="763a4-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="763a4-129">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="763a4-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="763a4-130">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="763a4-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="763a4-131">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="763a4-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="763a4-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="763a4-132">Requirements</span></span>



| <span data-ttu-id="763a4-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="763a4-133">Requirement</span></span> | <span data-ttu-id="763a4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="763a4-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="763a4-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="763a4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="763a4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="763a4-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="763a4-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="763a4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="763a4-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="763a4-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="763a4-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="763a4-139">Namespace</span></span><br/>                | <span data-ttu-id="763a4-140">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="763a4-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="763a4-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="763a4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="763a4-142"><dt>Faxcomex. h</dt></span><span class="sxs-lookup"><span data-stu-id="763a4-142"><dt>Faxcomex.h</dt></span></span> </dl>   |
| <span data-ttu-id="763a4-143">MOF</span><span class="sxs-lookup"><span data-stu-id="763a4-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="763a4-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="763a4-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="763a4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="763a4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="763a4-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="763a4-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="763a4-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="763a4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="763a4-148">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="763a4-148">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

