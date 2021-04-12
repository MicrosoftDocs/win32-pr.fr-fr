---
title: Méthode RefreshCertContext de la classe Win32_TSGatewayServerSettings
description: Actualise le certificat utilisé par le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: caefeb85-1c7a-4868-9ee8-10ab09354595
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RefreshCertContext
- Services Bureau à distance de la méthode RefreshCertContext, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode RefreshCertContext
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RefreshCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b03d77fff9574b0aff577d8ff45b54f57758f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384531"
---
# <a name="refreshcertcontext-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="d6bb2-106">Méthode RefreshCertContext de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="d6bb2-106">RefreshCertContext method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="d6bb2-107">Actualise le certificat utilisé par le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="d6bb2-107">Refreshes the certificate that is used by the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6bb2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6bb2-108">Syntax</span></span>


```mof
uint32 RefreshCertContext(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="d6bb2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6bb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6bb2-110">*Certhash* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6bb2-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bb2-111">Hachage du certificat utilisé par le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d6bb2-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6bb2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6bb2-112">Return value</span></span>

<span data-ttu-id="d6bb2-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="d6bb2-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d6bb2-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d6bb2-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d6bb2-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d6bb2-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d6bb2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d6bb2-116">Remarks</span></span>

<span data-ttu-id="d6bb2-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d6bb2-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d6bb2-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6bb2-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d6bb2-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d6bb2-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d6bb2-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d6bb2-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d6bb2-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d6bb2-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6bb2-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6bb2-122">Requirements</span></span>



| <span data-ttu-id="d6bb2-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6bb2-123">Requirement</span></span> | <span data-ttu-id="d6bb2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bb2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6bb2-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6bb2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d6bb2-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6bb2-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d6bb2-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6bb2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d6bb2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6bb2-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d6bb2-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d6bb2-129">Namespace</span></span><br/>                | <span data-ttu-id="d6bb2-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d6bb2-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d6bb2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d6bb2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6bb2-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6bb2-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6bb2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d6bb2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6bb2-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6bb2-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d6bb2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6bb2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6bb2-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="d6bb2-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

