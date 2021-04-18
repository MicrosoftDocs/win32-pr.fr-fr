---
title: Méthode RemovePackageMethod de la classe MDM_EnterpriseModernAppManagement_AppManagement01
description: Méthode de suppression des packages. Voir aussi RemovePackage.
ms.assetid: 0f48fd9c-5a3f-48e5-a954-e937e79af049
keywords:
- Méthode RemovePackageMethod
- Méthode RemovePackageMethod, classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, méthode RemovePackageMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.RemovePackageMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2cdeb2c1a8dfaebdde73e52b2910da180b638c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511788"
---
# <a name="removepackagemethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="c68f1-107">Méthode RemovePackageMethod de la \_ \_ classe AppManagement01 MDM EnterpriseModernAppManagement</span><span class="sxs-lookup"><span data-stu-id="c68f1-107">RemovePackageMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="c68f1-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c68f1-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c68f1-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c68f1-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c68f1-110">Méthode de suppression des packages.</span><span class="sxs-lookup"><span data-stu-id="c68f1-110">Method for removing packages.</span></span> <span data-ttu-id="c68f1-111">Voir aussi [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="c68f1-111">See also [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="c68f1-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c68f1-112">Syntax</span></span>


```mof
uint32 RemovePackageMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="c68f1-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c68f1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68f1-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c68f1-114">*param* \[in\]</span></span>
<span data-ttu-id="c68f1-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c68f1-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c68f1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c68f1-116">Requirements</span></span>



| <span data-ttu-id="c68f1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c68f1-117">Requirement</span></span> | <span data-ttu-id="c68f1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c68f1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68f1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c68f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c68f1-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c68f1-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c68f1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c68f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c68f1-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c68f1-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c68f1-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c68f1-123">Namespace</span></span><br/>                | <span data-ttu-id="c68f1-124">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c68f1-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c68f1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c68f1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c68f1-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c68f1-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c68f1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c68f1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c68f1-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c68f1-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68f1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c68f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68f1-130">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01**</span><span class="sxs-lookup"><span data-stu-id="c68f1-130">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> </dl>

 

