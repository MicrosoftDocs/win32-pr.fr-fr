---
title: Méthode AddLicenseMethod de la classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Méthode d’ajout d’une licence. Voir aussi AddLicense.
ms.assetid: 325d284d-10ac-4786-8b04-8184ac43b53f
keywords:
- Méthode AddLicenseMethod
- Méthode AddLicenseMethod, classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, méthode AddLicenseMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.AddLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f104f4e74d0200cc9d00b9f116232aa5308738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542863"
---
# <a name="addlicensemethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="585db-107">Méthode AddLicenseMethod de la \_ classe EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="585db-107">AddLicenseMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="585db-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="585db-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="585db-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="585db-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="585db-110">Méthode d’ajout d’une licence.</span><span class="sxs-lookup"><span data-stu-id="585db-110">Method for adding license.</span></span> <span data-ttu-id="585db-111">Voir aussi [AddLicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="585db-111">See also, [AddLicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="585db-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="585db-112">Syntax</span></span>


```mof
uint32 AddLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="585db-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="585db-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="585db-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="585db-114">*param* \[in\]</span></span>
<span data-ttu-id="585db-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="585db-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="585db-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="585db-116">Requirements</span></span>



| <span data-ttu-id="585db-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="585db-117">Requirement</span></span> | <span data-ttu-id="585db-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="585db-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="585db-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="585db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="585db-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="585db-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="585db-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="585db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="585db-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="585db-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="585db-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="585db-123">Namespace</span></span><br/>                | <span data-ttu-id="585db-124">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="585db-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="585db-125">MOF</span><span class="sxs-lookup"><span data-stu-id="585db-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="585db-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="585db-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="585db-127">DLL</span><span class="sxs-lookup"><span data-stu-id="585db-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="585db-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="585db-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="585db-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="585db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="585db-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="585db-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="585db-131">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="585db-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

