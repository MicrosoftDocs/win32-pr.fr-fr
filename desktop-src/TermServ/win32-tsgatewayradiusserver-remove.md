---
title: Méthode Remove de la classe Win32_TSGatewayRADIUSServer
description: Supprime le serveur de protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) actuel.
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Services Bureau à distance
- Supprimer la méthode Services Bureau à distance, Win32_TSGatewayRADIUSServer interface
- Win32_TSGatewayRADIUSServer Services Bureau à distance de l’interface, Remove, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a91fc4a3ba8bf638dcffd76e3bf3517795674fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317418"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="a57e6-106">Méthode Remove de la \_ classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="a57e6-106">Remove method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="a57e6-107">Supprime le serveur de protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) actuel.</span><span class="sxs-lookup"><span data-stu-id="a57e6-107">Removes the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a57e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a57e6-108">Syntax</span></span>


```mof
uint32 Remove();
```



## <a name="parameters"></a><span data-ttu-id="a57e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a57e6-109">Parameters</span></span>

<span data-ttu-id="a57e6-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a57e6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a57e6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a57e6-111">Return value</span></span>

<span data-ttu-id="a57e6-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="a57e6-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a57e6-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a57e6-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a57e6-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a57e6-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a57e6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a57e6-115">Remarks</span></span>

<span data-ttu-id="a57e6-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a57e6-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a57e6-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="a57e6-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a57e6-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a57e6-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a57e6-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="a57e6-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a57e6-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a57e6-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a57e6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a57e6-121">Requirements</span></span>



| <span data-ttu-id="a57e6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a57e6-122">Requirement</span></span> | <span data-ttu-id="a57e6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a57e6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a57e6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a57e6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a57e6-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a57e6-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a57e6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a57e6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a57e6-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a57e6-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a57e6-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a57e6-128">Namespace</span></span><br/>                | <span data-ttu-id="a57e6-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a57e6-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a57e6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a57e6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a57e6-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a57e6-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a57e6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a57e6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a57e6-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a57e6-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a57e6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a57e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57e6-135">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="a57e6-135">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

