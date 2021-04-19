---
title: Méthode SetPromptForPassword de la classe Win32_TSLogonSetting
description: La méthode SetPromptForPassword définit la propriété PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetPromptForPassword
- Services Bureau à distance de la méthode SetPromptForPassword, classe Win32_TSLogonSetting
- Win32_TSLogonSetting de la classe Services Bureau à distance, méthode SetPromptForPassword
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536077"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="1a827-106">Méthode SetPromptForPassword de la \_ classe Win32 TSLogonSetting</span><span class="sxs-lookup"><span data-stu-id="1a827-106">SetPromptForPassword method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="1a827-107">La méthode **SetPromptForPassword** définit la propriété **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="1a827-107">The **SetPromptForPassword** method sets the **PromptForPassword** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a827-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a827-108">Syntax</span></span>


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a><span data-ttu-id="1a827-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a827-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a827-110">*PromptForPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a827-110">*PromptForPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a827-111">Indicateur de désactivation ou d’activation de la propriété **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="1a827-111">Flag disabling or enabling the **PromptForPassword** property.</span></span>

<dt>

<span data-ttu-id="1a827-112">0</span><span class="sxs-lookup"><span data-stu-id="1a827-112">0</span></span>
</dt> <dd>

<span data-ttu-id="1a827-113">Désactive l’invite de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1a827-113">Disables password-prompting.</span></span>

</dd> <dt>

<span data-ttu-id="1a827-114">1</span><span class="sxs-lookup"><span data-stu-id="1a827-114">1</span></span>
</dt> <dd>

<span data-ttu-id="1a827-115">Active l’invite de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1a827-115">Enables password-prompting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a827-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a827-116">Return value</span></span>

<span data-ttu-id="1a827-117">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1a827-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1a827-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1a827-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1a827-119">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1a827-119">The method returns an error if the setting is under group policy control.</span></span>

<dl> <dt>

<span data-ttu-id="1a827-120">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="1a827-120">**FALSE** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a827-121">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="1a827-121">**TRUE** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1a827-122">Notes</span><span class="sxs-lookup"><span data-stu-id="1a827-122">Remarks</span></span>

<span data-ttu-id="1a827-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1a827-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1a827-124">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1a827-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1a827-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1a827-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1a827-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1a827-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a827-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a827-127">Requirements</span></span>



| <span data-ttu-id="1a827-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a827-128">Requirement</span></span> | <span data-ttu-id="1a827-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a827-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a827-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a827-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1a827-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a827-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a827-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a827-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1a827-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a827-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a827-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1a827-134">Namespace</span></span><br/>                | <span data-ttu-id="1a827-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="1a827-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1a827-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1a827-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a827-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a827-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a827-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1a827-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a827-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a827-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a827-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a827-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a827-141">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1a827-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

