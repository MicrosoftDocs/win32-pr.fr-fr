---
title: Méthode IsTransportEnabled de la classe Win32_TSGatewayServerSettings
description: Détermine si le transport spécifié est activé.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsTransportEnabled
- Services Bureau à distance de la méthode IsTransportEnabled, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode IsTransportEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103521"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="0f070-106">Méthode IsTransportEnabled de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="0f070-106">IsTransportEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="0f070-107">Détermine si le transport spécifié est activé.</span><span class="sxs-lookup"><span data-stu-id="0f070-107">Determines whether the specified transport is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f070-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f070-108">Syntax</span></span>


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="0f070-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f070-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f070-110">*TransportType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f070-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f070-111">Spécifie le type de transport.</span><span class="sxs-lookup"><span data-stu-id="0f070-111">Specifies the transport type.</span></span> <span data-ttu-id="0f070-112">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0f070-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="0f070-113">0</span><span class="sxs-lookup"><span data-stu-id="0f070-113">0</span></span>
</dt> <dd>

<span data-ttu-id="0f070-114">Transport RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="0f070-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="0f070-115">1</span><span class="sxs-lookup"><span data-stu-id="0f070-115">1</span></span>
</dt> <dd>

<span data-ttu-id="0f070-116">Transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="0f070-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="0f070-117">2</span><span class="sxs-lookup"><span data-stu-id="0f070-117">2</span></span>
</dt> <dd>

<span data-ttu-id="0f070-118">Transport UDP.</span><span class="sxs-lookup"><span data-stu-id="0f070-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0f070-119">*Activé* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0f070-119">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f070-120">Valeur **booléenne** qui indique si le transport est activé.</span><span class="sxs-lookup"><span data-stu-id="0f070-120">A **boolean** value that indicates whether the transport is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f070-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f070-121">Return value</span></span>

<span data-ttu-id="0f070-122">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="0f070-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0f070-123">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="0f070-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0f070-124">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0f070-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f070-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f070-125">Requirements</span></span>



| <span data-ttu-id="0f070-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f070-126">Requirement</span></span> | <span data-ttu-id="0f070-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f070-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f070-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f070-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f070-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f070-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0f070-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f070-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f070-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f070-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="0f070-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0f070-132">Namespace</span></span><br/>                | <span data-ttu-id="0f070-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0f070-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0f070-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0f070-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f070-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f070-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f070-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0f070-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f070-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f070-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0f070-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f070-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f070-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="0f070-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





