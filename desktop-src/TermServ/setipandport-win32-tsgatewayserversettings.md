---
title: Méthode SetIPAndPort de la classe Win32_TSGatewayServerSettings
description: Définit l’adresse IP d’écoute et le numéro de port pour le transport spécifié.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetIPAndPort
- Services Bureau à distance de la méthode SetIPAndPort, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508514"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="97af9-106">Méthode SetIPAndPort de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="97af9-106">SetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="97af9-107">Définit l’adresse IP d’écoute et le numéro de port pour le transport spécifié.</span><span class="sxs-lookup"><span data-stu-id="97af9-107">Sets the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="97af9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97af9-108">Syntax</span></span>


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a><span data-ttu-id="97af9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97af9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97af9-110">*TransportType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97af9-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97af9-111">Spécifie le type de transport.</span><span class="sxs-lookup"><span data-stu-id="97af9-111">Specifies the transport type.</span></span> <span data-ttu-id="97af9-112">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="97af9-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="97af9-113">0</span><span class="sxs-lookup"><span data-stu-id="97af9-113">0</span></span>
</dt> <dd>

<span data-ttu-id="97af9-114">Transport RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="97af9-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="97af9-115">1</span><span class="sxs-lookup"><span data-stu-id="97af9-115">1</span></span>
</dt> <dd>

<span data-ttu-id="97af9-116">Transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="97af9-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="97af9-117">2</span><span class="sxs-lookup"><span data-stu-id="97af9-117">2</span></span>
</dt> <dd>

<span data-ttu-id="97af9-118">Transport UDP.</span><span class="sxs-lookup"><span data-stu-id="97af9-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="97af9-119">*Adresse IP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97af9-119">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97af9-120">Spécifie l’adresse IP d’écoute, sous forme d’octet (par exemple, « 192.168.1.1 »).</span><span class="sxs-lookup"><span data-stu-id="97af9-120">Specifies the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="97af9-121">*Port* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97af9-121">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97af9-122">Spécifie le numéro de port d’écoute.</span><span class="sxs-lookup"><span data-stu-id="97af9-122">Specifies the listening port number.</span></span>

</dd> <dt>

<span data-ttu-id="97af9-123">*OverrideExisting* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97af9-123">*OverrideExisting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97af9-124">Indique s’il faut remplacer la liaison de port/adresse IP existante pour HTTP.</span><span class="sxs-lookup"><span data-stu-id="97af9-124">Indicates whether to override the existing IP/Port binding for HTTP.</span></span> <span data-ttu-id="97af9-125">Ce paramètre est utilisé uniquement si le paramètre *TransportType* contient 0 (RPC sur http) ou 1 (http).</span><span class="sxs-lookup"><span data-stu-id="97af9-125">This parameter is only used if the *TransportType* parameter contains 0 (RPC over HTTP) or 1 (HTTP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97af9-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97af9-126">Return value</span></span>

<span data-ttu-id="97af9-127">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="97af9-127">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="97af9-128">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="97af9-128">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="97af9-129">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="97af9-129">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97af9-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97af9-130">Requirements</span></span>



| <span data-ttu-id="97af9-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97af9-131">Requirement</span></span> | <span data-ttu-id="97af9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="97af9-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97af9-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97af9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="97af9-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97af9-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="97af9-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97af9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="97af9-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97af9-136">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="97af9-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97af9-137">Namespace</span></span><br/>                | <span data-ttu-id="97af9-138">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="97af9-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="97af9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="97af9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97af9-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97af9-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="97af9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="97af9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97af9-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97af9-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="97af9-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97af9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97af9-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="97af9-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





