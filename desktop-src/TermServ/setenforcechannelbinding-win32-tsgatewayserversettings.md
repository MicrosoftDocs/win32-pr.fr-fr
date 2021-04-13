---
title: Méthode SetEnforceChannelBinding de la classe Win32_TSGatewayServerSettings
description: Définit la propriété EnforceChannelBinding.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEnforceChannelBinding
- Services Bureau à distance de la méthode SetEnforceChannelBinding, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetEnforceChannelBinding
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b236341f0fdac31f80f7e7d77aa12a4b22eb9731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508741"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="92a3e-106">Méthode SetEnforceChannelBinding de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="92a3e-106">SetEnforceChannelBinding method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="92a3e-107">Définit la propriété **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="92a3e-107">Sets the **EnforceChannelBinding** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a3e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92a3e-108">Syntax</span></span>


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a><span data-ttu-id="92a3e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92a3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a3e-110">*EnforceChannelBinding* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92a3e-110">*EnforceChannelBinding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a3e-111">Spécifie la nouvelle valeur de la propriété **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="92a3e-111">Specifies the new **EnforceChannelBinding** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a3e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92a3e-112">Return value</span></span>

<span data-ttu-id="92a3e-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="92a3e-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="92a3e-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="92a3e-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="92a3e-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="92a3e-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92a3e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92a3e-116">Requirements</span></span>



| <span data-ttu-id="92a3e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92a3e-117">Requirement</span></span> | <span data-ttu-id="92a3e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="92a3e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a3e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a3e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92a3e-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a3e-120">None supported</span></span><br/>                                                                |
| <span data-ttu-id="92a3e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a3e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92a3e-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92a3e-122">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="92a3e-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92a3e-123">Namespace</span></span><br/>                | <span data-ttu-id="92a3e-124">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="92a3e-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="92a3e-125">MOF</span><span class="sxs-lookup"><span data-stu-id="92a3e-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92a3e-126"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92a3e-126"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="92a3e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="92a3e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a3e-128"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a3e-128"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="92a3e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a3e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a3e-130">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="92a3e-130">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





