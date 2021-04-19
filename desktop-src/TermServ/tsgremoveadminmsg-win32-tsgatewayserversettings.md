---
title: Méthode TSGRemoveAdminMsg de la classe Win32_TSGatewayServerSettings
description: Supprime le message d’administration pour le serveur de passerelle. | Méthode TSGRemoveAdminMsg de la classe Win32_TSGatewayServerSettings
ms.assetid: 36b157de-80ee-46f8-9803-5012cf1d6f5f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TSGRemoveAdminMsg
- Services Bureau à distance de la méthode TSGRemoveAdminMsg, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode TSGRemoveAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba9877b9e8704c92eb482876ab69107e116207b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538301"
---
# <a name="tsgremoveadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="44265-107">Méthode TSGRemoveAdminMsg de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="44265-107">TSGRemoveAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="44265-108">Supprime le message d’administration pour le serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="44265-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="44265-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44265-109">Syntax</span></span>


```mof
uint32 TSGRemoveAdminMsg();
```



## <a name="parameters"></a><span data-ttu-id="44265-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44265-110">Parameters</span></span>

<span data-ttu-id="44265-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="44265-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44265-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44265-112">Return value</span></span>

<span data-ttu-id="44265-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44265-113">Type: **uint32**</span></span>

<span data-ttu-id="44265-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="44265-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="44265-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="44265-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="44265-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="44265-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44265-117">Notes</span><span class="sxs-lookup"><span data-stu-id="44265-117">Remarks</span></span>

<span data-ttu-id="44265-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="44265-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="44265-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="44265-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="44265-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="44265-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44265-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="44265-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="44265-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="44265-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="44265-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44265-123">Requirements</span></span>



| <span data-ttu-id="44265-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44265-124">Requirement</span></span> | <span data-ttu-id="44265-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="44265-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44265-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44265-126">Minimum supported client</span></span><br/> | <span data-ttu-id="44265-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="44265-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="44265-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44265-128">Minimum supported server</span></span><br/> | <span data-ttu-id="44265-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="44265-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="44265-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="44265-130">Namespace</span></span><br/>                | <span data-ttu-id="44265-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="44265-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="44265-132">MOF</span><span class="sxs-lookup"><span data-stu-id="44265-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44265-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44265-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="44265-134">DLL</span><span class="sxs-lookup"><span data-stu-id="44265-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44265-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44265-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="44265-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44265-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44265-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="44265-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

