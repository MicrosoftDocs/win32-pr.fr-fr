---
title: Méthode GetProtocolName de la classe Win32_TSGatewayServerSettings
description: Retourne le nom de protocole pour l’index de protocole spécifié.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetProtocolName
- Services Bureau à distance de la méthode GetProtocolName, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode GetProtocolName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104332"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="86a04-106">Méthode GetProtocolName de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="86a04-106">GetProtocolName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="86a04-107">Retourne le nom de protocole pour l’index de protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="86a04-107">Returns the protocol name for the specified protocol index.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a04-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86a04-108">Syntax</span></span>


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="86a04-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86a04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a04-110">*ProtocolId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86a04-110">*ProtocolId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a04-111">Index de l’identificateur de protocole.</span><span class="sxs-lookup"><span data-stu-id="86a04-111">Index of the protocol identifier.</span></span> <span data-ttu-id="86a04-112">La valeur doit être comprise entre zéro et la valeur de la propriété **MaxProtocols** .</span><span class="sxs-lookup"><span data-stu-id="86a04-112">The value must be between zero and the value of the **MaxProtocols** property.</span></span>

</dd> <dt>

<span data-ttu-id="86a04-113">*ProtocolName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86a04-113">*ProtocolName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86a04-114">Retourne le nom du protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="86a04-114">Returns the name of the specified protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a04-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86a04-115">Return value</span></span>

<span data-ttu-id="86a04-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="86a04-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="86a04-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="86a04-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="86a04-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="86a04-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="86a04-119">Notes</span><span class="sxs-lookup"><span data-stu-id="86a04-119">Remarks</span></span>

<span data-ttu-id="86a04-120">Un protocole est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="86a04-120">One protocol is supported.</span></span>

<span data-ttu-id="86a04-121">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="86a04-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="86a04-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="86a04-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86a04-123">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="86a04-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="86a04-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="86a04-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86a04-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="86a04-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="86a04-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86a04-126">Requirements</span></span>



| <span data-ttu-id="86a04-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86a04-127">Requirement</span></span> | <span data-ttu-id="86a04-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="86a04-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86a04-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86a04-129">Minimum supported client</span></span><br/> | <span data-ttu-id="86a04-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="86a04-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="86a04-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86a04-131">Minimum supported server</span></span><br/> | <span data-ttu-id="86a04-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86a04-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="86a04-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="86a04-133">Namespace</span></span><br/>                | <span data-ttu-id="86a04-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="86a04-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="86a04-135">MOF</span><span class="sxs-lookup"><span data-stu-id="86a04-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86a04-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86a04-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="86a04-137">DLL</span><span class="sxs-lookup"><span data-stu-id="86a04-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86a04-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a04-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="86a04-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86a04-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a04-140">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="86a04-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

