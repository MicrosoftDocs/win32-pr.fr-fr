---
title: Méthode GetIPAndPort de la classe Win32_TSGatewayServerSettings
description: Obtient l’adresse IP d’écoute et le numéro de port pour le transport spécifié.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetIPAndPort
- Services Bureau à distance de la méthode GetIPAndPort, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317161"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="584cc-106">Méthode GetIPAndPort de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="584cc-106">GetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="584cc-107">Obtient l’adresse IP d’écoute et le numéro de port pour le transport spécifié.</span><span class="sxs-lookup"><span data-stu-id="584cc-107">Obtains the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="584cc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="584cc-108">Syntax</span></span>


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a><span data-ttu-id="584cc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="584cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="584cc-110">*TransportType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="584cc-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="584cc-111">Spécifie le type de transport.</span><span class="sxs-lookup"><span data-stu-id="584cc-111">Specifies the transport type.</span></span> <span data-ttu-id="584cc-112">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="584cc-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="584cc-113">0</span><span class="sxs-lookup"><span data-stu-id="584cc-113">0</span></span>
</dt> <dd>

<span data-ttu-id="584cc-114">Transport RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="584cc-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="584cc-115">1</span><span class="sxs-lookup"><span data-stu-id="584cc-115">1</span></span>
</dt> <dd>

<span data-ttu-id="584cc-116">Transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="584cc-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="584cc-117">2</span><span class="sxs-lookup"><span data-stu-id="584cc-117">2</span></span>
</dt> <dd>

<span data-ttu-id="584cc-118">Transport UDP.</span><span class="sxs-lookup"><span data-stu-id="584cc-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="584cc-119">*Adresse IP* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="584cc-119">*IPAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="584cc-120">Chaîne qui reçoit l’adresse IP d’écoute, sous forme d’octet (par exemple, « 192.168.1.1 »).</span><span class="sxs-lookup"><span data-stu-id="584cc-120">A string that receives the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="584cc-121">*Port* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="584cc-121">*Port* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="584cc-122">Spécifie le numéro de port d’écoute.</span><span class="sxs-lookup"><span data-stu-id="584cc-122">Specifies the listening port number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="584cc-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="584cc-123">Return value</span></span>

<span data-ttu-id="584cc-124">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="584cc-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="584cc-125">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="584cc-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="584cc-126">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="584cc-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="584cc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="584cc-127">Requirements</span></span>



| <span data-ttu-id="584cc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="584cc-128">Requirement</span></span> | <span data-ttu-id="584cc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="584cc-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="584cc-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="584cc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="584cc-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="584cc-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="584cc-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="584cc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="584cc-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="584cc-133">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="584cc-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="584cc-134">Namespace</span></span><br/>                | <span data-ttu-id="584cc-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="584cc-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="584cc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="584cc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="584cc-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="584cc-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="584cc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="584cc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="584cc-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="584cc-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="584cc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="584cc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584cc-141">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="584cc-141">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





