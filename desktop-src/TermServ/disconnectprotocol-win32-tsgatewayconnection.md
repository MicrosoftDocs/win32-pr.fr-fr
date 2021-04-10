---
title: Méthode DisconnectProtocol de la classe Win32_TSGatewayConnection
description: Déconnecte toutes les connexions du protocole spécifié à partir du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisconnectProtocol
- Services Bureau à distance de la méthode DisconnectProtocol, classe Win32_TSGatewayConnection
- Win32_TSGatewayConnection de la classe Services Bureau à distance, méthode DisconnectProtocol
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317306"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="9f542-106">Méthode DisconnectProtocol de la \_ classe Win32 TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9f542-106">DisconnectProtocol method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="9f542-107">Déconnecte toutes les connexions du protocole spécifié à partir du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="9f542-107">Disconnects all connections of the specified protocol from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f542-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f542-108">Syntax</span></span>


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="9f542-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f542-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f542-110">*ProtocolName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f542-110">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f542-111">Nom de protocole pour une connexion spécifique.</span><span class="sxs-lookup"><span data-stu-id="9f542-111">The protocol name for a specific connection.</span></span> <span data-ttu-id="9f542-112">Cela peut être récupéré à partir de la propriété **ProtocolName** de la classe **Win32 \_ TSGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="9f542-112">This can be retrieved from the **ProtocolName** property of the **Win32\_TSGatewayConnection** class.</span></span>

<dt>

<span data-ttu-id="9f542-113">TS</span><span class="sxs-lookup"><span data-stu-id="9f542-113">"TS"</span></span>
</dt> <dd>

<span data-ttu-id="9f542-114">Protocole du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9f542-114">The protocol for the RD Gateway server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f542-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f542-115">Return value</span></span>

<span data-ttu-id="9f542-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="9f542-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9f542-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="9f542-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9f542-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9f542-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f542-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9f542-119">Remarks</span></span>

<span data-ttu-id="9f542-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9f542-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9f542-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9f542-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9f542-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9f542-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9f542-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9f542-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9f542-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9f542-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f542-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f542-125">Requirements</span></span>



| <span data-ttu-id="9f542-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f542-126">Requirement</span></span> | <span data-ttu-id="9f542-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f542-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f542-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f542-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f542-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f542-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9f542-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f542-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f542-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f542-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9f542-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9f542-132">Namespace</span></span><br/>                | <span data-ttu-id="9f542-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="9f542-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9f542-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9f542-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f542-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f542-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f542-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9f542-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f542-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f542-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9f542-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f542-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f542-139">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="9f542-139">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

