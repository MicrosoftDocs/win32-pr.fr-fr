---
title: Méthode UpgradeEditionWithProductKeyMethod de la classe MDM_WindowsLicensing
description: Entre une clé de produit pour une mise à niveau d’édition des appareils Windows 10 Desktop. Voir aussi UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Méthode UpgradeEditionWithProductKeyMethod
- Méthode UpgradeEditionWithProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, méthode UpgradeEditionWithProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466191"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="7072d-107">Méthode UpgradeEditionWithProductKeyMethod de la \_ classe MDM WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="7072d-107">UpgradeEditionWithProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="7072d-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7072d-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7072d-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7072d-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7072d-110">Entre une clé de produit pour une mise à niveau d’édition des appareils Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="7072d-110">Enters a product key for an edition upgrade of Windows 10 desktop devices.</span></span> <span data-ttu-id="7072d-111">Voir aussi [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="7072d-111">See also, [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="7072d-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7072d-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="7072d-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7072d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7072d-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7072d-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7072d-115">Clé de produit.</span><span class="sxs-lookup"><span data-stu-id="7072d-115">The product key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7072d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7072d-116">Requirements</span></span>



| <span data-ttu-id="7072d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7072d-117">Requirement</span></span> | <span data-ttu-id="7072d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7072d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7072d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7072d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7072d-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7072d-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7072d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7072d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7072d-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7072d-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7072d-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7072d-123">Namespace</span></span><br/>                | <span data-ttu-id="7072d-124">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="7072d-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7072d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7072d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7072d-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7072d-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7072d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7072d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7072d-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7072d-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7072d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7072d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7072d-130">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="7072d-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="7072d-131">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="7072d-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

