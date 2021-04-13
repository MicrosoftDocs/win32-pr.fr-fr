---
title: Méthode MoveUp de la classe Win32_TSGatewayRADIUSServer
description: Déplace ce serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) d’une position vers le haut dans l’ordre de priorité.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- Méthode MoveUp Services Bureau à distance
- Méthode MoveUp Services Bureau à distance, classe Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance, méthode MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509342"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="72854-106">Méthode MoveUp de la \_ classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="72854-106">MoveUp method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="72854-107">Déplace ce serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) d’une position vers le haut dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="72854-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position up in the priority order.</span></span> <span data-ttu-id="72854-108">Cette méthode décrémente la propriété **Priority** du serveur RADIUS actuel et incrémente la propriété **Priority** du serveur RADIUS qui précède le serveur RADIUS actuel.</span><span class="sxs-lookup"><span data-stu-id="72854-108">This method decrements the **Priority** property of the current RADIUS server and increments the **Priority** property of the RADIUS server that precedes the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="72854-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72854-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="72854-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72854-110">Parameters</span></span>

<span data-ttu-id="72854-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="72854-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72854-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72854-112">Return value</span></span>

<span data-ttu-id="72854-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="72854-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="72854-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="72854-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="72854-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="72854-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="72854-116">Notes</span><span class="sxs-lookup"><span data-stu-id="72854-116">Remarks</span></span>

<span data-ttu-id="72854-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="72854-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="72854-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="72854-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="72854-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="72854-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="72854-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="72854-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="72854-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="72854-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="72854-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72854-122">Requirements</span></span>



| <span data-ttu-id="72854-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72854-123">Requirement</span></span> | <span data-ttu-id="72854-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="72854-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72854-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72854-125">Minimum supported client</span></span><br/> | <span data-ttu-id="72854-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="72854-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="72854-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72854-127">Minimum supported server</span></span><br/> | <span data-ttu-id="72854-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72854-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="72854-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="72854-129">Namespace</span></span><br/>                | <span data-ttu-id="72854-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="72854-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="72854-131">MOF</span><span class="sxs-lookup"><span data-stu-id="72854-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72854-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72854-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="72854-133">DLL</span><span class="sxs-lookup"><span data-stu-id="72854-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72854-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72854-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="72854-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72854-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72854-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="72854-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

