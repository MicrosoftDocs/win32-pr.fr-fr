---
title: Méthode EnableAllowOnlySDRServers de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Utilisé pour basculer la propriété AllowOnlySDRServers.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableAllowOnlySDRServers
- Services Bureau à distance de la méthode EnableAllowOnlySDRServers, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode EnableAllowOnlySDRServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741253"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="77066-106">Méthode EnableAllowOnlySDRServers de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="77066-106">EnableAllowOnlySDRServers method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="77066-107">Utilisé pour basculer la propriété **AllowOnlySDRServers** .</span><span class="sxs-lookup"><span data-stu-id="77066-107">Used to toggle the **AllowOnlySDRServers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="77066-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77066-108">Syntax</span></span>


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a><span data-ttu-id="77066-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77066-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77066-110">*AllowOnlySDRServers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77066-110">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77066-111">Si la valeur est **true**, les connexions sont autorisées uniquement pour sécuriser les serveurs RDS de redirection des appareils (SDR).</span><span class="sxs-lookup"><span data-stu-id="77066-111">If set to **True**, connections will be allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="77066-112">Si la valeur est **false**, les connexions seront autorisées à des serveurs RDS plus anciens.</span><span class="sxs-lookup"><span data-stu-id="77066-112">If set to **False**, connections will be allowed to older RDS servers also</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77066-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77066-113">Return value</span></span>

<span data-ttu-id="77066-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="77066-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="77066-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="77066-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="77066-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="77066-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77066-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77066-117">Requirements</span></span>



| <span data-ttu-id="77066-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77066-118">Requirement</span></span> | <span data-ttu-id="77066-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="77066-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77066-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77066-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77066-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="77066-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="77066-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77066-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77066-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77066-123">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="77066-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77066-124">Namespace</span></span><br/>                | <span data-ttu-id="77066-125">RACINE \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="77066-125">ROOT\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="77066-126">MOF</span><span class="sxs-lookup"><span data-stu-id="77066-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77066-127"><dt>TsGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77066-127"><dt>TsGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="77066-128">DLL</span><span class="sxs-lookup"><span data-stu-id="77066-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77066-129"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77066-129"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="77066-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77066-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77066-131">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="77066-131">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





