---
title: Méthode UpdateScanMethod de la classe MDM_EnterpriseModernAppManagement_AppManagement01
description: Méthode de démarrage de l’analyse Windows Update. Voir aussi UpdateScan.
ms.assetid: 61d17072-0fe5-4d5b-8e9e-fed536883ac9
keywords:
- Méthode UpdateScanMethod
- Méthode UpdateScanMethod, classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, méthode UpdateScanMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.UpdateScanMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6cb5b744243b78f737ea44fbc27ef40708c6f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510555"
---
# <a name="updatescanmethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="c13c7-107">Méthode UpdateScanMethod de la \_ \_ classe AppManagement01 MDM EnterpriseModernAppManagement</span><span class="sxs-lookup"><span data-stu-id="c13c7-107">UpdateScanMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="c13c7-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c13c7-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c13c7-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c13c7-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c13c7-110">Méthode de démarrage de l’analyse Windows Update.</span><span class="sxs-lookup"><span data-stu-id="c13c7-110">Method for starting the Windows Update scan.</span></span> <span data-ttu-id="c13c7-111">Voir aussi [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="c13c7-111">See also, [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="c13c7-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c13c7-112">Syntax</span></span>


```mof
uint32 UpdateScanMethod();
```



## <a name="parameters"></a><span data-ttu-id="c13c7-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c13c7-113">Parameters</span></span>

<span data-ttu-id="c13c7-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c13c7-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c13c7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c13c7-115">Requirements</span></span>



| <span data-ttu-id="c13c7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c13c7-116">Requirement</span></span> | <span data-ttu-id="c13c7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c13c7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c13c7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c13c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c13c7-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c13c7-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c13c7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c13c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c13c7-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c13c7-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c13c7-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c13c7-122">Namespace</span></span><br/>                | <span data-ttu-id="c13c7-123">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c13c7-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c13c7-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c13c7-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c13c7-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c13c7-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c13c7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c13c7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c13c7-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c13c7-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c13c7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c13c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13c7-129">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01**</span><span class="sxs-lookup"><span data-stu-id="c13c7-129">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> <dt>

[<span data-ttu-id="c13c7-130">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="c13c7-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

