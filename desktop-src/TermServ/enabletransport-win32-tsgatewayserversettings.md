---
title: Méthode EnableTransport de la classe Win32_TSGatewayServerSettings
description: Active ou désactive le transport spécifié.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableTransport
- Services Bureau à distance de la méthode EnableTransport, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnableTransport
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515683"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="83b49-106">Méthode EnableTransport de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="83b49-106">EnableTransport method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="83b49-107">Active ou désactive le transport spécifié.</span><span class="sxs-lookup"><span data-stu-id="83b49-107">Enables or disables the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b49-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83b49-108">Syntax</span></span>


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a><span data-ttu-id="83b49-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83b49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b49-110">*TransportType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83b49-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b49-111">Spécifie le type de transport.</span><span class="sxs-lookup"><span data-stu-id="83b49-111">Specifies the transport type.</span></span> <span data-ttu-id="83b49-112">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="83b49-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="83b49-113">0</span><span class="sxs-lookup"><span data-stu-id="83b49-113">0</span></span>
</dt> <dd>

<span data-ttu-id="83b49-114">Transport RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="83b49-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="83b49-115">1</span><span class="sxs-lookup"><span data-stu-id="83b49-115">1</span></span>
</dt> <dd>

<span data-ttu-id="83b49-116">Transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="83b49-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="83b49-117">2</span><span class="sxs-lookup"><span data-stu-id="83b49-117">2</span></span>
</dt> <dd>

<span data-ttu-id="83b49-118">Transport UDP.</span><span class="sxs-lookup"><span data-stu-id="83b49-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83b49-119">*Activer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83b49-119">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b49-120">Spécifie si le transport est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="83b49-120">Specifies if the transport is enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83b49-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83b49-121">Return value</span></span>

<span data-ttu-id="83b49-122">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="83b49-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="83b49-123">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="83b49-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="83b49-124">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="83b49-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83b49-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83b49-125">Requirements</span></span>



| <span data-ttu-id="83b49-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83b49-126">Requirement</span></span> | <span data-ttu-id="83b49-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="83b49-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83b49-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83b49-128">Minimum supported client</span></span><br/> | <span data-ttu-id="83b49-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="83b49-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="83b49-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83b49-130">Minimum supported server</span></span><br/> | <span data-ttu-id="83b49-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83b49-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="83b49-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83b49-132">Namespace</span></span><br/>                | <span data-ttu-id="83b49-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="83b49-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="83b49-134">MOF</span><span class="sxs-lookup"><span data-stu-id="83b49-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83b49-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83b49-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="83b49-136">DLL</span><span class="sxs-lookup"><span data-stu-id="83b49-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83b49-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83b49-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="83b49-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83b49-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b49-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="83b49-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





