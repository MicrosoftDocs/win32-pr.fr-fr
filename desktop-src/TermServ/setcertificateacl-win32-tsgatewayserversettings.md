---
title: Méthode SetCertificateACL de la classe Win32_TSGatewayServerSettings
description: Définit le certificat requis pour accéder au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 274c24bf-4e44-42ea-a109-99d0249c2f78
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetCertificateACL
- Services Bureau à distance de la méthode SetCertificateACL, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetCertificateACL
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificateACL
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7a43e737b39b9bea18ee3925b5c3f55440d2a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033223"
---
# <a name="setcertificateacl-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="d9a62-106">Méthode SetCertificateACL de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="d9a62-106">SetCertificateACL method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="d9a62-107">Définit le certificat requis pour accéder au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="d9a62-107">Sets the certificate that is required to access the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a62-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9a62-108">Syntax</span></span>


```mof
uint32 SetCertificateACL(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="d9a62-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9a62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a62-110">*Certhash* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9a62-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a62-111">Hachage du certificat utilisé par le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d9a62-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a62-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9a62-112">Return value</span></span>

<span data-ttu-id="d9a62-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="d9a62-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d9a62-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d9a62-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d9a62-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d9a62-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a62-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d9a62-116">Remarks</span></span>

<span data-ttu-id="d9a62-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d9a62-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d9a62-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d9a62-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d9a62-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d9a62-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d9a62-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d9a62-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d9a62-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d9a62-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a62-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9a62-122">Requirements</span></span>



| <span data-ttu-id="d9a62-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9a62-123">Requirement</span></span> | <span data-ttu-id="d9a62-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9a62-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a62-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9a62-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a62-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9a62-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d9a62-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9a62-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a62-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9a62-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d9a62-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d9a62-129">Namespace</span></span><br/>                | <span data-ttu-id="d9a62-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d9a62-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d9a62-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d9a62-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9a62-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9a62-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9a62-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d9a62-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9a62-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9a62-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d9a62-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9a62-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a62-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="d9a62-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

