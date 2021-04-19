---
title: Méthode BrokenConnection de la classe Win32_TSSessionSetting (Wtsprotocol. h)
description: Définit la propriété BrokenConnectionAction, qui est l’action prise par le serveur si la limite de durée de session est atteinte ou si la connexion est interrompue.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode BrokenConnection
- Services Bureau à distance de la méthode BrokenConnection, classe Win32_TSSessionSetting
- Win32_TSSessionSetting de la classe Services Bureau à distance, méthode BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510749"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="376de-106">Méthode BrokenConnection de la \_ classe Win32 TSSessionSetting</span><span class="sxs-lookup"><span data-stu-id="376de-106">BrokenConnection method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="376de-107">Définit la propriété **BrokenConnectionAction** , qui est l’action prise par le serveur si la limite de durée de session est atteinte ou si la connexion est interrompue.</span><span class="sxs-lookup"><span data-stu-id="376de-107">Sets the **BrokenConnectionAction** property, which is the action the server takes if the session time-limit is reached or if the connection is broken.</span></span>

## <a name="syntax"></a><span data-ttu-id="376de-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="376de-108">Syntax</span></span>


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a><span data-ttu-id="376de-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="376de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="376de-110">*BrokenConnectionAction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="376de-110">*BrokenConnectionAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="376de-111">Action à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="376de-111">The action to take.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="376de-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Déconnecter** (0)</span><span class="sxs-lookup"><span data-stu-id="376de-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="376de-113">L’utilisateur est déconnecté de la session.</span><span class="sxs-lookup"><span data-stu-id="376de-113">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="376de-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span><span class="sxs-lookup"><span data-stu-id="376de-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="376de-115">La session est définitivement supprimée du serveur.</span><span class="sxs-lookup"><span data-stu-id="376de-115">The session is permanently deleted from the server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="376de-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="376de-116">Return value</span></span>

<span data-ttu-id="376de-117">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="376de-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="376de-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="376de-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="376de-119">La méthode retourne une erreur si le paramètre est sous stratégie de groupe contrôle.</span><span class="sxs-lookup"><span data-stu-id="376de-119">The method returns an error if the setting is under Group Policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="376de-120">Notes</span><span class="sxs-lookup"><span data-stu-id="376de-120">Remarks</span></span>

<span data-ttu-id="376de-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="376de-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="376de-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="376de-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="376de-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="376de-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="376de-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="376de-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="376de-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="376de-125">Requirements</span></span>



| <span data-ttu-id="376de-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="376de-126">Requirement</span></span> | <span data-ttu-id="376de-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="376de-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="376de-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="376de-128">Minimum supported client</span></span><br/> | <span data-ttu-id="376de-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="376de-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="376de-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="376de-130">Minimum supported server</span></span><br/> | <span data-ttu-id="376de-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="376de-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="376de-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="376de-132">Namespace</span></span><br/>                | <span data-ttu-id="376de-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="376de-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="376de-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="376de-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="376de-135"><dt>Wtsprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="376de-135"><dt>Wtsprotocol.h</dt></span></span> </dl> |
| <span data-ttu-id="376de-136">MOF</span><span class="sxs-lookup"><span data-stu-id="376de-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="376de-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="376de-137"><dt>TSCfgWmi.mof</dt></span></span> </dl>  |
| <span data-ttu-id="376de-138">DLL</span><span class="sxs-lookup"><span data-stu-id="376de-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="376de-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="376de-139"><dt>TSCfgWmi.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="376de-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="376de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="376de-141">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="376de-141">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

