---
title: MoveDown, méthode de la classe Win32_TSGatewayRADIUSServer
description: Déplace ce serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) d’une position vers le dessous dans l’ordre de priorité.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- MoveDown, méthode Services Bureau à distance
- MoveDown, méthode Services Bureau à distance, classe Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance, méthode MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b652eb5e9cfc36f0d41e14d9953b295d35e660be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508522"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="99b3a-106">MoveDown, méthode de la \_ classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="99b3a-106">MoveDown method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="99b3a-107">Déplace ce serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) d’une position vers le dessous dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="99b3a-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position down in the priority order.</span></span> <span data-ttu-id="99b3a-108">Cette méthode incrémente la propriété **Priority** du serveur RADIUS actuel et décrémente la propriété **Priority** du serveur RADIUS qui suit le serveur RADIUS actuel.</span><span class="sxs-lookup"><span data-stu-id="99b3a-108">This method increments the **Priority** property of the current RADIUS server and decrements the **Priority** property of the RADIUS server that follows the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b3a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99b3a-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="99b3a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b3a-110">Parameters</span></span>

<span data-ttu-id="99b3a-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="99b3a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99b3a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99b3a-112">Return value</span></span>

<span data-ttu-id="99b3a-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="99b3a-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="99b3a-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="99b3a-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="99b3a-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="99b3a-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99b3a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="99b3a-116">Remarks</span></span>

<span data-ttu-id="99b3a-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="99b3a-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="99b3a-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="99b3a-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="99b3a-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="99b3a-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="99b3a-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="99b3a-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="99b3a-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="99b3a-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="99b3a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99b3a-122">Requirements</span></span>



| <span data-ttu-id="99b3a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99b3a-123">Requirement</span></span> | <span data-ttu-id="99b3a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="99b3a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b3a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99b3a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="99b3a-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="99b3a-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="99b3a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99b3a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="99b3a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99b3a-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="99b3a-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="99b3a-129">Namespace</span></span><br/>                | <span data-ttu-id="99b3a-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="99b3a-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="99b3a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="99b3a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99b3a-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99b3a-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="99b3a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="99b3a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99b3a-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b3a-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="99b3a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99b3a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b3a-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="99b3a-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

