---
title: Méthode MoveUp de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Déplace la stratégie d’autorisation de connexion Bureau à distance actuelle (RD \ 160 ; CAP) une position dans l’ordre dans lequel RD \ 160 ; Les majuscules sont évaluées.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- Méthode MoveUp Services Bureau à distance
- Méthode MoveUp Services Bureau à distance, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81973261d156328aa1f306c26dd8bd9bdd20511f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466894"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0914d-106">Méthode MoveUp de la \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="0914d-106">MoveUp method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0914d-107">Déplace la stratégie d’autorisation des connexions Bureau à distance en cours (RD CAP) d’une position vers le haut dans l’ordre dans lequel les majuscules Bureau à distance sont évaluées.</span><span class="sxs-lookup"><span data-stu-id="0914d-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position up in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="0914d-108">Cette méthode décrémente la propriété **Order** de la stratégie d’autorisation des connexions aux services Bureau à distance actuelle et incrémente la propriété **Order** de la stratégie d’autorisation des connexions aux services Bureau à distance qui précédait la stratégie Rd.</span><span class="sxs-lookup"><span data-stu-id="0914d-108">This method decrements the **Order** property of the current RD CAP and increments the **Order** property of the RD CAP that preceded the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="0914d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0914d-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="0914d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0914d-110">Parameters</span></span>

<span data-ttu-id="0914d-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0914d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0914d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0914d-112">Return value</span></span>

<span data-ttu-id="0914d-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="0914d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0914d-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="0914d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0914d-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0914d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0914d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0914d-116">Remarks</span></span>

<span data-ttu-id="0914d-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0914d-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0914d-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0914d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0914d-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0914d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0914d-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0914d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0914d-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0914d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0914d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0914d-122">Requirements</span></span>



| <span data-ttu-id="0914d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0914d-123">Requirement</span></span> | <span data-ttu-id="0914d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0914d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0914d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0914d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0914d-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0914d-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0914d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0914d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0914d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0914d-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0914d-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0914d-129">Namespace</span></span><br/>                | <span data-ttu-id="0914d-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0914d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0914d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0914d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0914d-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0914d-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0914d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0914d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0914d-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0914d-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0914d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0914d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0914d-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="0914d-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="0914d-137">**Descendre**</span><span class="sxs-lookup"><span data-stu-id="0914d-137">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

