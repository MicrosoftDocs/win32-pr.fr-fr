---
title: Méthode GetLicenseFromStoreMethod de la classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Méthode permettant d’obtenir une licence du magasin. Voir aussi GetLicenseFromStore.
ms.assetid: 4cf8a979-60c1-4ec1-968e-5a90cc671ebf
keywords:
- Méthode GetLicenseFromStoreMethod
- Méthode GetLicenseFromStoreMethod, classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, méthode GetLicenseFromStoreMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.GetLicenseFromStoreMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8751546bfb57e5c9bf34db97ee6b59dd7e1f580
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104974"
---
# <a name="getlicensefromstoremethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="d259c-107">Méthode GetLicenseFromStoreMethod de la \_ classe EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="d259c-107">GetLicenseFromStoreMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="d259c-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d259c-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d259c-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d259c-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d259c-110">Méthode permettant d’obtenir une licence du magasin.</span><span class="sxs-lookup"><span data-stu-id="d259c-110">Method for getting a license from the store.</span></span> <span data-ttu-id="d259c-111">Voir aussi [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="d259c-111">See also, [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="d259c-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d259c-112">Syntax</span></span>


```mof
uint32 GetLicenseFromStoreMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="d259c-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d259c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d259c-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d259c-114">*param* \[in\]</span></span>
<span data-ttu-id="d259c-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d259c-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d259c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d259c-116">Requirements</span></span>



| <span data-ttu-id="d259c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d259c-117">Requirement</span></span> | <span data-ttu-id="d259c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d259c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d259c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d259c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d259c-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d259c-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d259c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d259c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d259c-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d259c-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d259c-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d259c-123">Namespace</span></span><br/>                | <span data-ttu-id="d259c-124">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d259c-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d259c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d259c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d259c-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d259c-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d259c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d259c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d259c-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d259c-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d259c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d259c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d259c-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="d259c-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="d259c-131">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d259c-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

