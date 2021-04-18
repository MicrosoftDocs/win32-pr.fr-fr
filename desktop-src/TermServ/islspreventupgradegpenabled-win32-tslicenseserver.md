---
title: Méthode IsLSPreventUpgradeGPEnabled de la classe Win32_TSLicenseServer
description: Récupère les valeur indiquant si \ 0034 ; empêcher la mise à niveau de licence \ 0034 ; le paramètre de stratégie de groupe est activé sur le serveur de licences Bureau à distance.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLSPreventUpgradeGPEnabled
- Services Bureau à distance de la méthode IsLSPreventUpgradeGPEnabled, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509330"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="41210-106">Méthode IsLSPreventUpgradeGPEnabled de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="41210-106">IsLSPreventUpgradeGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="41210-107">Récupère si le paramètre de stratégie de groupe « empêcher la mise à niveau de licence » est activé sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="41210-107">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="41210-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41210-108">Syntax</span></span>


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="41210-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41210-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41210-110">*Activé* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="41210-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41210-111">Valeur booléenne qui indique si le paramètre de stratégie « empêcher la mise à niveau de licence » est activé.</span><span class="sxs-lookup"><span data-stu-id="41210-111">Boolean value that indicates whether the "prevent license upgrade" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41210-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41210-112">Return value</span></span>

<span data-ttu-id="41210-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="41210-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="41210-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="41210-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="41210-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="41210-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41210-116">Notes</span><span class="sxs-lookup"><span data-stu-id="41210-116">Remarks</span></span>

<span data-ttu-id="41210-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="41210-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="41210-118">Si le paramètre de stratégie « empêcher la mise à niveau de licence » est activé, le serveur de licences émet une licence d’accès client aux services Bureau à distance temporaire au client uniquement si une licence d’accès client aux services Bureau à distance appropriée pour le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="41210-118">If the "prevent license upgrade" policy setting is enabled, the license server will only issue a temporary RDS CAL to the client if an appropriate RDS CAL for the Remote Desktop Session Host (RD Session Host) server is not available.</span></span>

<span data-ttu-id="41210-119">Le paramètre de stratégie se trouve dans le nœud suivant de l’éditeur d’une stratégie de groupe locale :</span><span class="sxs-lookup"><span data-stu-id="41210-119">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="41210-120">Configuration de l’ordinateur \\ modèles d’administration \\ composants Windows \\ Gestionnaire de \\ licences TS TS</span><span class="sxs-lookup"><span data-stu-id="41210-120">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="41210-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="41210-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="41210-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="41210-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="41210-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="41210-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="41210-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="41210-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="41210-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41210-125">Requirements</span></span>



| <span data-ttu-id="41210-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41210-126">Requirement</span></span> | <span data-ttu-id="41210-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="41210-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="41210-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41210-128">Minimum supported client</span></span><br/> | <span data-ttu-id="41210-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="41210-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="41210-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41210-130">Minimum supported server</span></span><br/> | <span data-ttu-id="41210-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41210-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="41210-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="41210-132">Namespace</span></span><br/>                | <span data-ttu-id="41210-133">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="41210-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="41210-134">MOF</span><span class="sxs-lookup"><span data-stu-id="41210-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41210-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41210-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="41210-136">DLL</span><span class="sxs-lookup"><span data-stu-id="41210-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41210-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41210-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41210-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41210-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41210-139">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="41210-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

