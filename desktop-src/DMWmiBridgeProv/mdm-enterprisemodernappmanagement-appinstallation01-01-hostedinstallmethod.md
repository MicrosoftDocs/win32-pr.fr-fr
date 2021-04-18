---
title: Méthode HostedInstallMethod de la classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Méthode permettant d’effectuer l’installation d’un package d’application à partir d’un emplacement hébergé, tel qu’un lecteur local, une source de données UNC ou HTTPs. Voir aussi HostedInstall.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Méthode HostedInstallMethod
- Méthode HostedInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, méthode HostedInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511789"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="d8b33-107">Méthode HostedInstallMethod de la \_ classe EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="d8b33-107">HostedInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="d8b33-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d8b33-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d8b33-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d8b33-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d8b33-110">Méthode permettant d’effectuer l’installation d’un package d’application à partir d’un emplacement hébergé, tel qu’un lecteur local, une source de données UNC ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="d8b33-110">Method to perform an install of an app package from a hosted location, such as a local drive, a UNC, or HTTPS data source.</span></span> <span data-ttu-id="d8b33-111">Voir aussi [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="d8b33-111">See also, [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b33-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b33-112">Syntax</span></span>


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="d8b33-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8b33-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b33-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8b33-114">*param* \[in\]</span></span>
<span data-ttu-id="d8b33-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d8b33-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d8b33-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8b33-116">Requirements</span></span>



| <span data-ttu-id="d8b33-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8b33-117">Requirement</span></span> | <span data-ttu-id="d8b33-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8b33-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b33-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b33-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b33-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8b33-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8b33-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b33-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b33-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b33-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d8b33-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8b33-123">Namespace</span></span><br/>                | <span data-ttu-id="d8b33-124">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d8b33-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d8b33-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d8b33-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8b33-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8b33-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8b33-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d8b33-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8b33-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8b33-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b33-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b33-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b33-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="d8b33-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="d8b33-131">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d8b33-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

