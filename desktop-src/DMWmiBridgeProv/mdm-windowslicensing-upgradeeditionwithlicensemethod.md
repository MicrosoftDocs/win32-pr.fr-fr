---
title: Méthode UpgradeEditionWithLicenseMethod de la classe MDM_WindowsLicensing
description: Méthode pour fournir une licence pour une mise à niveau d’édition des appareils Windows 10 mobile. Voir aussi UpgradeEditionWithLicense.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- Méthode UpgradeEditionWithLicenseMethod
- Méthode UpgradeEditionWithLicenseMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, méthode UpgradeEditionWithLicenseMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336ee4128aa520ecd463c3607254526c7c3dc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942515"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="a4815-107">Méthode UpgradeEditionWithLicenseMethod de la \_ classe MDM WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="a4815-107">UpgradeEditionWithLicenseMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="a4815-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a4815-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a4815-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a4815-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a4815-110">Méthode pour fournir une licence pour une mise à niveau d’édition des appareils Windows 10 mobile.</span><span class="sxs-lookup"><span data-stu-id="a4815-110">Method for providing a license for an edition upgrade of Windows 10 mobile devices.</span></span> <span data-ttu-id="a4815-111">Voir aussi [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="a4815-111">See also, [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4815-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4815-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="a4815-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4815-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4815-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4815-114">*param* \[in\]</span></span>
<span data-ttu-id="a4815-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a4815-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a4815-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4815-116">Requirements</span></span>



| <span data-ttu-id="a4815-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4815-117">Requirement</span></span> | <span data-ttu-id="a4815-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4815-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4815-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4815-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a4815-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4815-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4815-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4815-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a4815-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4815-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a4815-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4815-123">Namespace</span></span><br/>                | <span data-ttu-id="a4815-124">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a4815-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a4815-125">MOF</span><span class="sxs-lookup"><span data-stu-id="a4815-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4815-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4815-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4815-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a4815-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4815-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4815-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4815-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4815-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4815-130">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="a4815-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="a4815-131">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="a4815-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

