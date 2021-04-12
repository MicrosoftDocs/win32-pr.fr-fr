---
title: Méthode ExplicitLogon de la classe Win32_TSLogonSetting
description: La méthode ExplicitLogon définit les informations d’identification à utiliser pour l’authentification.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ExplicitLogon
- Services Bureau à distance de la méthode ExplicitLogon, classe Win32_TSLogonSetting
- Win32_TSLogonSetting de la classe Services Bureau à distance, méthode ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384959"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="94a08-106">Méthode ExplicitLogon de la \_ classe Win32 TSLogonSetting</span><span class="sxs-lookup"><span data-stu-id="94a08-106">ExplicitLogon method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="94a08-107">La méthode **ExplicitLogon** définit les informations d’identification à utiliser pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="94a08-107">The **ExplicitLogon** method sets the credentials to use for authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a08-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94a08-108">Syntax</span></span>


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a><span data-ttu-id="94a08-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94a08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94a08-110">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94a08-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a08-111">Informations d’identification d’ouverture de session de nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="94a08-111">The user name logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="94a08-112">*Domaine* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94a08-112">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a08-113">Informations d’identification d’ouverture de session de domaine.</span><span class="sxs-lookup"><span data-stu-id="94a08-113">The domain logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="94a08-114">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94a08-114">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a08-115">Informations d’identification de connexion au mot de passe.</span><span class="sxs-lookup"><span data-stu-id="94a08-115">The password logon credential.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94a08-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94a08-116">Return value</span></span>

<span data-ttu-id="94a08-117">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="94a08-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="94a08-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="94a08-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="94a08-119">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="94a08-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="94a08-120">Notes</span><span class="sxs-lookup"><span data-stu-id="94a08-120">Remarks</span></span>

<span data-ttu-id="94a08-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="94a08-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="94a08-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="94a08-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="94a08-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="94a08-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="94a08-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="94a08-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="94a08-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94a08-125">Requirements</span></span>



| <span data-ttu-id="94a08-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94a08-126">Requirement</span></span> | <span data-ttu-id="94a08-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="94a08-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94a08-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94a08-128">Minimum supported client</span></span><br/> | <span data-ttu-id="94a08-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94a08-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94a08-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94a08-130">Minimum supported server</span></span><br/> | <span data-ttu-id="94a08-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94a08-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94a08-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="94a08-132">Namespace</span></span><br/>                | <span data-ttu-id="94a08-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="94a08-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="94a08-134">MOF</span><span class="sxs-lookup"><span data-stu-id="94a08-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94a08-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94a08-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="94a08-136">DLL</span><span class="sxs-lookup"><span data-stu-id="94a08-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94a08-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94a08-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a08-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94a08-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a08-139">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="94a08-139">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

