---
title: Méthode CheckApplicabilityMethod de la classe MDM_WindowsLicensing
description: Vérifie si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit Windows 10 pour les appareils de bureau. Voir aussi CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Méthode CheckApplicabilityMethod
- Méthode CheckApplicabilityMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, méthode CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104941"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="3477f-107">Méthode CheckApplicabilityMethod de la \_ classe MDM WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="3477f-107">CheckApplicabilityMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="3477f-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="3477f-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3477f-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="3477f-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3477f-110">Vérifie si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit Windows 10 pour les appareils de bureau.</span><span class="sxs-lookup"><span data-stu-id="3477f-110">Checks if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span> <span data-ttu-id="3477f-111">Voir aussi [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="3477f-111">See also, [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="3477f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3477f-112">Syntax</span></span>


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="3477f-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3477f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3477f-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3477f-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3477f-115">Clé de produit.</span><span class="sxs-lookup"><span data-stu-id="3477f-115">The product key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3477f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3477f-116">Return value</span></span>

<span data-ttu-id="3477f-117">TRUE ou FALSE</span><span class="sxs-lookup"><span data-stu-id="3477f-117">TRUE or FALSE</span></span>

## <a name="requirements"></a><span data-ttu-id="3477f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3477f-118">Requirements</span></span>



| <span data-ttu-id="3477f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3477f-119">Requirement</span></span> | <span data-ttu-id="3477f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3477f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3477f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3477f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3477f-122">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3477f-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3477f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3477f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3477f-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3477f-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3477f-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3477f-125">Namespace</span></span><br/>                | <span data-ttu-id="3477f-126">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3477f-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3477f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="3477f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3477f-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3477f-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3477f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3477f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3477f-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3477f-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3477f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3477f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3477f-132">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="3477f-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="3477f-133">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="3477f-133">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

