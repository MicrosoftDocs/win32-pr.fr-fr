---
title: Méthode SetMaxConnections de la classe Win32_TSGatewayServerSettings
description: Définit les propriétés MaxConnections et UnlimitedConnections, qui contrôlent le nombre maximal de connexions autorisées sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetMaxConnections
- Services Bureau à distance de la méthode SetMaxConnections, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetMaxConnections
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510985"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="842b1-106">Méthode SetMaxConnections de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="842b1-106">SetMaxConnections method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="842b1-107">Définit les propriétés **MaxConnections** et **UnlimitedConnections** , qui contrôlent le nombre maximal de connexions autorisées sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="842b1-107">Sets the **MaxConnections** and **UnlimitedConnections** properties, which control the maximum number of allowed connections to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="842b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="842b1-108">Syntax</span></span>


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a><span data-ttu-id="842b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="842b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="842b1-110">*Connexions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="842b1-110">*Connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842b1-111">Nombre de connexions que ce serveur doit accepter.</span><span class="sxs-lookup"><span data-stu-id="842b1-111">Number of connections that this server should accept.</span></span> <span data-ttu-id="842b1-112">Pour un nombre illimité de connexions, affectez la valeur **true** au paramètre *IsUnlimited* .</span><span class="sxs-lookup"><span data-stu-id="842b1-112">For an unlimited number of connections, set the *IsUnlimited* parameter to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="842b1-113">*IsUnlimited* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="842b1-113">*IsUnlimited* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842b1-114">Si la **valeur est true**, les connexions au service ne sont pas limitées à un nombre spécifique.</span><span class="sxs-lookup"><span data-stu-id="842b1-114">If **True**, connections to the service are not limited to a specific number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="842b1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="842b1-115">Return value</span></span>

<span data-ttu-id="842b1-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="842b1-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="842b1-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="842b1-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="842b1-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="842b1-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="842b1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="842b1-119">Remarks</span></span>

<span data-ttu-id="842b1-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="842b1-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="842b1-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="842b1-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="842b1-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="842b1-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="842b1-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="842b1-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="842b1-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="842b1-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="842b1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="842b1-125">Requirements</span></span>



| <span data-ttu-id="842b1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="842b1-126">Requirement</span></span> | <span data-ttu-id="842b1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="842b1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="842b1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="842b1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="842b1-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="842b1-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="842b1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="842b1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="842b1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="842b1-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="842b1-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="842b1-132">Namespace</span></span><br/>                | <span data-ttu-id="842b1-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="842b1-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="842b1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="842b1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="842b1-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="842b1-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="842b1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="842b1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="842b1-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="842b1-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="842b1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="842b1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842b1-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="842b1-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

