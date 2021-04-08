---
title: Méthode SetSharedSecret de la classe Win32_TSGatewayRADIUSServer
description: Définit la propriété de serveur à la une pour ce protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSharedSecret
- Services Bureau à distance de la méthode SetSharedSecret, classe Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance, méthode SetSharedSecret
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742365"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="3f33c-106">Méthode SetSharedSecret de la \_ classe Win32 TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="3f33c-106">SetSharedSecret method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="3f33c-107">Définit la **propriété de serveur** à la une pour ce protocole RADIUS (Remote Authentication Dial-in User Service) (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="3f33c-107">Sets the **SharedSecret** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f33c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f33c-108">Syntax</span></span>


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="3f33c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f33c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f33c-110">Sous-son  \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f33c-110">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f33c-111">Nouveau secret partagé.</span><span class="sxs-lookup"><span data-stu-id="3f33c-111">New shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f33c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f33c-112">Return value</span></span>

<span data-ttu-id="3f33c-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3f33c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3f33c-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3f33c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3f33c-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3f33c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f33c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3f33c-116">Remarks</span></span>

<span data-ttu-id="3f33c-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3f33c-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3f33c-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3f33c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3f33c-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3f33c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3f33c-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3f33c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3f33c-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3f33c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f33c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f33c-122">Requirements</span></span>



| <span data-ttu-id="3f33c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f33c-123">Requirement</span></span> | <span data-ttu-id="3f33c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f33c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f33c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f33c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3f33c-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f33c-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3f33c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f33c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3f33c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f33c-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3f33c-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3f33c-129">Namespace</span></span><br/>                | <span data-ttu-id="3f33c-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="3f33c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3f33c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3f33c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f33c-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f33c-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f33c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3f33c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f33c-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f33c-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3f33c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f33c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f33c-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="3f33c-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

