---
title: Méthode DisconnectUser de la classe Win32_TSGatewayConnection (Tsgauthenticationengine. h)
description: Déconnecte toutes les connexions de l’utilisateur spécifié du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisconnectUser
- Services Bureau à distance de la méthode DisconnectUser, classe Win32_TSGatewayConnection
- Win32_TSGatewayConnection de la classe Services Bureau à distance, méthode DisconnectUser
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742149"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="0faf4-106">Méthode DisconnectUser de la \_ classe Win32 TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0faf4-106">DisconnectUser method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="0faf4-107">Déconnecte toutes les connexions de l’utilisateur spécifié du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="0faf4-107">Disconnects all connections of the specified user from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0faf4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0faf4-108">Syntax</span></span>


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="0faf4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0faf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0faf4-110">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0faf4-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faf4-111">Nom d’utilisateur, au format \* domaine \* **\\** _nom d'_ utilisateur, dont les connexions doivent être déconnectées.</span><span class="sxs-lookup"><span data-stu-id="0faf4-111">The user name, in \*Domain\***\\**_UserName_ format, whose connections are to be disconnected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0faf4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0faf4-112">Return value</span></span>

<span data-ttu-id="0faf4-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="0faf4-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0faf4-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="0faf4-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0faf4-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0faf4-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0faf4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0faf4-116">Remarks</span></span>

<span data-ttu-id="0faf4-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0faf4-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0faf4-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0faf4-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0faf4-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0faf4-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0faf4-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0faf4-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0faf4-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0faf4-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0faf4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0faf4-122">Requirements</span></span>



| <span data-ttu-id="0faf4-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0faf4-123">Requirement</span></span> | <span data-ttu-id="0faf4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0faf4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0faf4-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0faf4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0faf4-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0faf4-126">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="0faf4-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0faf4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0faf4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0faf4-128">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="0faf4-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0faf4-129">Namespace</span></span><br/>                | <span data-ttu-id="0faf4-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0faf4-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                             |
| <span data-ttu-id="0faf4-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0faf4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0faf4-132"><dt>Tsgauthenticationengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="0faf4-132"><dt>Tsgauthenticationengine.h</dt></span></span> </dl> |
| <span data-ttu-id="0faf4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0faf4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0faf4-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0faf4-134"><dt>TSGateway.mof</dt></span></span> </dl>             |
| <span data-ttu-id="0faf4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0faf4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0faf4-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0faf4-136"><dt>AagWmi.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="0faf4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0faf4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0faf4-138">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="0faf4-138">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

