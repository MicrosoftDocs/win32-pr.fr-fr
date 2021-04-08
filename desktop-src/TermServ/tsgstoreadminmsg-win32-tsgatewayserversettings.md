---
title: Méthode TSGStoreAdminMsg de la classe Win32_TSGatewayServerSettings
description: Met à jour le message d’administration pour le serveur de passerelle.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TSGStoreAdminMsg
- Services Bureau à distance de la méthode TSGStoreAdminMsg, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode TSGStoreAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843693"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="ede6d-106">Méthode TSGStoreAdminMsg de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="ede6d-106">TSGStoreAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="ede6d-107">Met à jour le message d’administration pour le serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="ede6d-107">Updates the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede6d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ede6d-108">Syntax</span></span>


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="ede6d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ede6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede6d-110">*TSGAdmMsg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ede6d-110">*TSGAdmMsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ede6d-111">Type: **string**</span></span>

<span data-ttu-id="ede6d-112">Texte du message administratif.</span><span class="sxs-lookup"><span data-stu-id="ede6d-112">The administrative message text.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-113">*MsgStartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ede6d-113">*MsgStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-114">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ede6d-114">Type: **string**</span></span>

<span data-ttu-id="ede6d-115">Heure de début du message d’administration.</span><span class="sxs-lookup"><span data-stu-id="ede6d-115">The administrative message start time.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-116">*MsgEndTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ede6d-116">*MsgEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-117">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ede6d-117">Type: **string**</span></span>

<span data-ttu-id="ede6d-118">Heure de fin du message d’administration.</span><span class="sxs-lookup"><span data-stu-id="ede6d-118">The administrative message end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede6d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ede6d-119">Return value</span></span>

<span data-ttu-id="ede6d-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ede6d-120">Type: **uint32**</span></span>

<span data-ttu-id="ede6d-121">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="ede6d-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ede6d-122">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ede6d-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ede6d-123">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ede6d-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ede6d-124">Remarks</span></span>

<span data-ttu-id="ede6d-125">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ede6d-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ede6d-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ede6d-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ede6d-127">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ede6d-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ede6d-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ede6d-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ede6d-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ede6d-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ede6d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ede6d-130">Requirements</span></span>



| <span data-ttu-id="ede6d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ede6d-131">Requirement</span></span> | <span data-ttu-id="ede6d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ede6d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ede6d-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ede6d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ede6d-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ede6d-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ede6d-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ede6d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ede6d-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ede6d-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="ede6d-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ede6d-137">Namespace</span></span><br/>                | <span data-ttu-id="ede6d-138">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="ede6d-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ede6d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ede6d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ede6d-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ede6d-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ede6d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ede6d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ede6d-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ede6d-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ede6d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ede6d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede6d-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="ede6d-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

