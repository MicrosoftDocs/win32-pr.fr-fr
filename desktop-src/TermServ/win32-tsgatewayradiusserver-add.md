---
title: Ajouter une méthode de la classe Win32_TSGatewayRADIUSServer
description: Ajoute un nouveau serveur de protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).
ms.assetid: 78f74bb6-8f70-4bc1-8e4d-1670a3ae3f31
ms.tgt_platform: multiple
keywords:
- Ajouter une méthode Services Bureau à distance
- Ajouter une méthode Services Bureau à distance, Win32_TSGatewayRADIUSServer interface
- Win32_TSGatewayRADIUSServer Services Bureau à distance de l’interface, Add, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Add
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6869c55a6704944c34c68af065875cad92e8385c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527577"
---
# <a name="add-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="fba25-106">Ajouter une méthode de la \_ classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="fba25-106">Add method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="fba25-107">Ajoute un nouveau serveur de protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="fba25-107">Adds a new Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba25-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fba25-108">Syntax</span></span>


```mof
uint32 Add(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="fba25-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fba25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba25-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fba25-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba25-111">Nom du serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="fba25-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="fba25-112">Sous-son  \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fba25-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba25-113">Secret partagé pour le serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="fba25-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba25-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fba25-114">Return value</span></span>

<span data-ttu-id="fba25-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="fba25-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fba25-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="fba25-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fba25-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fba25-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fba25-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fba25-118">Remarks</span></span>

<span data-ttu-id="fba25-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fba25-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fba25-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="fba25-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fba25-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fba25-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fba25-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="fba25-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fba25-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fba25-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fba25-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fba25-124">Requirements</span></span>



| <span data-ttu-id="fba25-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fba25-125">Requirement</span></span> | <span data-ttu-id="fba25-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fba25-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba25-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba25-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fba25-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba25-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fba25-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba25-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fba25-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fba25-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fba25-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fba25-131">Namespace</span></span><br/>                | <span data-ttu-id="fba25-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="fba25-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fba25-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fba25-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba25-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba25-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba25-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fba25-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba25-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba25-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fba25-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fba25-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba25-138">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="fba25-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

