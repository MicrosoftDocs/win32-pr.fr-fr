---
title: Méthode SetSslBridging de la classe Win32_TSGatewayServerSettings
description: Définit le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSslBridging
- Services Bureau à distance de la méthode SetSslBridging, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384867"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b4dec-106">Méthode SetSslBridging de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="b4dec-106">SetSslBridging method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b4dec-107">Définit le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="b4dec-107">Sets the type of SSL bridging to be used by the Remote Desktop Gateway (RD Gateway) server.</span></span> <span data-ttu-id="b4dec-108">Cette valeur est stockée dans la propriété **SslBridging** .</span><span class="sxs-lookup"><span data-stu-id="b4dec-108">This value is stored in the **SslBridging** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4dec-109">Lorsque le type de pontage SSL est modifié avec cette méthode, le service de passerelle des services Bureau à distance doit être redémarré pour que cette modification prenne effet.</span><span class="sxs-lookup"><span data-stu-id="b4dec-109">When the SSL bridging type is changed with this method, the RD Gateway service must be restarted to make this change take effect.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b4dec-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4dec-110">Syntax</span></span>


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a><span data-ttu-id="b4dec-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4dec-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4dec-112">*SslBridging* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4dec-112">*SslBridging* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4dec-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4dec-113">Type: **uint32**</span></span>

<span data-ttu-id="b4dec-114">Spécifie la nouvelle valeur de pontage SSL.</span><span class="sxs-lookup"><span data-stu-id="b4dec-114">Specifies the new SSL bridging value.</span></span> <span data-ttu-id="b4dec-115">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4dec-115">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="b4dec-116">0</span><span class="sxs-lookup"><span data-stu-id="b4dec-116">0</span></span>
</dt> <dd>

<span data-ttu-id="b4dec-117">Aucun pontage SSL.</span><span class="sxs-lookup"><span data-stu-id="b4dec-117">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="b4dec-118">1</span><span class="sxs-lookup"><span data-stu-id="b4dec-118">1</span></span>
</dt> <dd>

<span data-ttu-id="b4dec-119">Pontage HTTPs vers HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4dec-119">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="b4dec-120">2</span><span class="sxs-lookup"><span data-stu-id="b4dec-120">2</span></span>
</dt> <dd>

<span data-ttu-id="b4dec-121">Pontage HTTPs vers HTTPs.</span><span class="sxs-lookup"><span data-stu-id="b4dec-121">HTTPS to HTTPS bridging.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4dec-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4dec-122">Return value</span></span>

<span data-ttu-id="b4dec-123">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4dec-123">Type: **uint32**</span></span>

<span data-ttu-id="b4dec-124">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="b4dec-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b4dec-125">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b4dec-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b4dec-126">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b4dec-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4dec-127">Notes</span><span class="sxs-lookup"><span data-stu-id="b4dec-127">Remarks</span></span>

<span data-ttu-id="b4dec-128">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b4dec-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b4dec-129">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b4dec-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b4dec-130">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b4dec-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b4dec-131">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b4dec-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b4dec-132">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b4dec-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4dec-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4dec-133">Requirements</span></span>



| <span data-ttu-id="b4dec-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4dec-134">Requirement</span></span> | <span data-ttu-id="b4dec-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4dec-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4dec-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4dec-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b4dec-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4dec-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b4dec-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4dec-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b4dec-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4dec-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b4dec-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b4dec-140">Namespace</span></span><br/>                | <span data-ttu-id="b4dec-141">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="b4dec-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b4dec-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b4dec-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4dec-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4dec-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4dec-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b4dec-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4dec-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4dec-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b4dec-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4dec-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4dec-147">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b4dec-147">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

