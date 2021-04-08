---
title: Méthode disconnect de la classe Win32_TSGatewayConnection
description: Déconnecte la connexion du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 8c424e58-aa89-4ec6-acea-5b571d3f4c21
ms.tgt_platform: multiple
keywords:
- Méthode Disconnect Services Bureau à distance
- Méthode Disconnect Services Bureau à distance, classe Win32_TSGatewayConnection
- Win32_TSGatewayConnection de la classe Services Bureau à distance, méthode Disconnect
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.Disconnect
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53101e5ca3529c5033adc918f1f9ad11a3b45f7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740029"
---
# <a name="disconnect-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="49145-106">Méthode disconnect de la \_ classe TSGatewayConnection Win32</span><span class="sxs-lookup"><span data-stu-id="49145-106">Disconnect method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="49145-107">Déconnecte la connexion du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="49145-107">Disconnects the connection from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="49145-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49145-108">Syntax</span></span>


```mof
uint32 Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="49145-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49145-109">Parameters</span></span>

<span data-ttu-id="49145-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="49145-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49145-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49145-111">Return value</span></span>

<span data-ttu-id="49145-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="49145-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="49145-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="49145-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="49145-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="49145-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49145-115">Notes</span><span class="sxs-lookup"><span data-stu-id="49145-115">Remarks</span></span>

<span data-ttu-id="49145-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="49145-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="49145-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="49145-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="49145-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="49145-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="49145-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="49145-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="49145-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="49145-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="49145-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49145-121">Requirements</span></span>



| <span data-ttu-id="49145-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49145-122">Requirement</span></span> | <span data-ttu-id="49145-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="49145-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="49145-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49145-124">Minimum supported client</span></span><br/> | <span data-ttu-id="49145-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="49145-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="49145-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49145-126">Minimum supported server</span></span><br/> | <span data-ttu-id="49145-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49145-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="49145-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49145-128">Namespace</span></span><br/>                | <span data-ttu-id="49145-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="49145-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="49145-130">MOF</span><span class="sxs-lookup"><span data-stu-id="49145-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49145-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49145-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="49145-132">DLL</span><span class="sxs-lookup"><span data-stu-id="49145-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49145-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49145-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="49145-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49145-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49145-135">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="49145-135">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

