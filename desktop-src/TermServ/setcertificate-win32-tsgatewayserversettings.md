---
title: Méthode SetCertificate de la classe Win32_TSGatewayServerSettings
description: Définit le hachage de certificat pour la liaison HTTPs sur le port 443 dans IIS.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetCertificate
- Services Bureau à distance de la méthode SetCertificate, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1da7e3abcca671b0c8bf70461c77d56e68cf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105847"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b7162-106">Méthode SetCertificate de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="b7162-106">SetCertificate method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b7162-107">Définit le hachage de certificat pour la liaison HTTPs sur le port 443 dans IIS.</span><span class="sxs-lookup"><span data-stu-id="b7162-107">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7162-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7162-108">Syntax</span></span>


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="b7162-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7162-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7162-110">*Certhash* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7162-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7162-111">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b7162-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="b7162-112">Nouveau hachage du certificat.</span><span class="sxs-lookup"><span data-stu-id="b7162-112">The new certificate hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7162-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7162-113">Return value</span></span>

<span data-ttu-id="b7162-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7162-114">Type: **uint32**</span></span>

<span data-ttu-id="b7162-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="b7162-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b7162-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b7162-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b7162-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b7162-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7162-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7162-118">Remarks</span></span>

<span data-ttu-id="b7162-119">Une fois que le hachage de certificat a été défini avec cette méthode, vous devez appeler la méthode [**configure**](configure-win32-tsgatewayserversettings.md) pour terminer le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="b7162-119">After the certificate hash has been set with this method, you must call the [**Configure**](configure-win32-tsgatewayserversettings.md) method to complete the configuration process.</span></span>

<span data-ttu-id="b7162-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b7162-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b7162-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b7162-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b7162-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b7162-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b7162-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b7162-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b7162-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b7162-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7162-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7162-125">Requirements</span></span>



| <span data-ttu-id="b7162-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7162-126">Requirement</span></span> | <span data-ttu-id="b7162-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7162-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7162-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7162-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b7162-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7162-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b7162-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7162-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b7162-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7162-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b7162-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7162-132">Namespace</span></span><br/>                | <span data-ttu-id="b7162-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="b7162-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b7162-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b7162-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7162-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7162-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7162-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b7162-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7162-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7162-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b7162-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7162-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7162-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b7162-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

